## Étapes principales du pipeline


### 1️⃣ Build

Vérifie le code avec actions/checkout

Installe les dépendances via npm ci

Compile le projet avec npm run build

Génère un artefact (./build) pour déploiement

### 2️⃣ Test

Exécute npm test -- --passWithNoTests

Vérifie que le build est correct avant déploiement

### 3️⃣ Déploiement

Utilise actions/deploy-pages@v4

Déploie automatiquement le dossier build/ sur GitHub Pages

Accessible via :
https://aminebarkati.github.io/CI-CD-GDG-Task