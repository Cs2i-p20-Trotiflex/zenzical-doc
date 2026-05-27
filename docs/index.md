Le Perceptron Simple en Rust

documentation de l'implémentation d'un **perceptron simple** (neurone artificiel unique) conçu en Rust. Ce modèle est capable de classer des données linéairement séparables (comme les portes logiques ET/OU).

---

##  Fonctionnement Théorique

Un perceptron prend plusieurs entrées ($x_1, x_2, \dots, x_n$), leur applique des poids ($w_1, w_2, \dots, w_n$), ajoute un biais ($b$), puis passe le tout dans une fonction d'activation (ici, la fonction échelon ou *Heaviside*)



La formule mathématique de la somme pondérée $z$ est :

$$z = \sum_{i=1}^{n} w_i x_i + b$$

La sortie prédite $\hat{y}$ est déterminée par la fonction d'activation :

$$\hat{y} = f(z) = \begin{cases} 1 & \text{si } z \geq 0 \\ 0 & \text{si } z < 0 \end{cases}$$

---

##  Architecture du Code en Rust

Le projet est structuré autour d'une structure `Perceptron` qui gère les poids, le biais et le taux d'apprentissage (*learning rate*).

### 1. La Structure du Perceptron

```rust
pub struct Perceptron {
    pub weights: Vec<f32>,
    pub bias: f32,
    pub learning_rate: f32,
}
