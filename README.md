# CI/CD Pipeline — Enterprise Project (v0.1.1 / 5.1)

## 🎯 Objectif
Mettre en place un **pipeline CI/CD automatisé** pour une application web simple, en utilisant **GitHub Actions**.  
Le pipeline exécute automatiquement les étapes suivantes :  
1. **Build** : Compilation et préparation de l’application.  
2. **Test** : Exécution des tests pour valider le code.  
3. **Déploiement** : Déploiement automatique sur **GitHub Pages**.

---

## 📁 Structure du projet

- .github/
  - workflows/
    - main.yaml        # Pipeline CI/CD (build, test, deploy)
- docs/
  - architecture.md    # Description du projet et de l’architecture
  - repartition.md     # Répartition des tâches de l’équipe
  - outils.md          # Outils et environnements utilisés
  - captures/          # Captures ou logs du prototype
- src/                 # Code source de l’application
- package.json
- package-lock.json
- build/               # Résultat du build (automatique)
- README.md
