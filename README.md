🚀 CI/CD Pipeline — Enterprise Project (Version 0.1.1 / 5.1)
🎯 Objectif

Mettre en place un pipeline CI/CD automatisé pour une application web simple, en utilisant GitHub Actions.
Ce pipeline exécute les étapes de build, test et déploiement automatique sur GitHub Pages.
🧩 Structure du projet
├── .github/
│   └── workflows/
│       └── main.yaml        # Pipeline CI/CD (build, test, deploy)
├── docs/
│   ├── architecture.md      # Description du projet et de l’architecture
│   ├── repartition.md       # Répartition des tâches de l’équipe
│   ├── outils.md            # Outils et environnements utilisés
│   └── captures/            # Captures ou logs du prototype
├── src/                     # Code source de l’application
├── package.json
├── package-lock.json
├── build/                   # Résultat du build (automatique)
└── README.md

⚙️ Étapes principales du pipeline
1️⃣ Build

Vérifie le code avec actions/checkout

Installe les dépendances via npm ci

Compile le projet avec npm run build

Génère un artefact (./build) pour déploiement

2️⃣ Test

Exécute npm test -- --passWithNoTests

Vérifie que le build est correct avant déploiement

3️⃣ Déploiement

Utilise actions/deploy-pages@v4

Déploie automatiquement le dossier build/ sur GitHub Pages

Accessible via :
https://<username>.github.io/<repo-name>/

🧠 Fichier principal du pipeline
.github/workflows/main.yaml
