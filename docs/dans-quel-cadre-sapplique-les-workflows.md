# Dans quel cadre s'appliquent les workflows GitHub ?

Les workflows GitHub s'appliquent dans les projets où on souhaite automatiser des tâches liées au développement et au déploiement. Ils sont utiles dès que on a besoin de :

- vérifier le code automatiquement à chaque push ou pull request,
- exécuter des tests unitaires et d'intégration,
- construire des artefacts ou des sites statiques,
- déployer une application vers un environnement de staging ou de production.

Concrètement, un workflow GitHub s'exécute à partir d'un fichier YAML placé dans `.github/workflows/`. Il est déclenché par des événements GitHub (push, pull_request, schedule, workflow_dispatch, etc.).
