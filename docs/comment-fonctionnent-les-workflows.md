# Comment fonctionnent les workflows GitHub ?

Les workflows GitHub fonctionnent grâce à des fichiers YAML qui décrivent :

- les événements déclencheurs (`on:`),
- les jobs à exécuter (`jobs:`),
- les étapes de chaque job (`steps:`),
- les actions ou commandes à lancer.

Un job s'exécute sur un runner (machine virtuelle ou conteneur) et chaque étape peut utiliser une action GitHub existante ou exécuter une commande shell.

Par exemple, un workflow peut commencer par vérifier le dépôt avec `actions/checkout`, installer les dépendances, lancer les tests, puis publier un résultat ou déployer le projet.
