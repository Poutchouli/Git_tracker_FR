# Rapport d'Audit de l'Activité Git (Git Tracker)

Un outil simple et interactif fonctionnant entièrement dans le navigateur pour analyser, visualiser et auditer l'activité d'un dépôt Git. Il permet de générer des rapports détaillés sur les habitudes de travail (commits pendant les heures de travail vs hors heures de travail) et d'exporter ces données au format image (PNG).

## 🚀 Fonctionnalités principales

- **Analyse des logs Git** : Importez facilement l'historique de vos commits via un simple copier-coller.
- **Configuration personnalisée** :
  - Définition des horaires de travail (début et fin).
  - Définition des horaires de pause déjeuner.
  - Définition des horaires de nuit.
  - Exclusion de dates spécifiques (jours fériés, congés, etc.).
  - Ajustement des seuils d'inactivité (session max) distincts pour le jour et la nuit.
- **Visualisation de données avancée** :
  - Répartition des commits par jour de la semaine (jour vs nuit).
  - Ratio des commits effectués pendant les heures de travail vs hors plage horaire (en volume et en temps estimé).
  - Courbe d'évolution de l'activité au fil du temps.
- **Calcul du temps de développement** : Estimation du temps passé à coder en fonction de la fréquence et de l'espacement des commits.
- **Exportation Image** : Générez un rapport propre et professionnel au format PNG en un seul clic.

## 🛠️ Technologies utilisées

Ce projet est une application "Single Page" (SPA) contenue dans un seul fichier HTML, utilisant des bibliothèques chargées via CDN :

- **React 18** (Interface utilisateur)
- **Tailwind CSS** (Stylisation rapide et responsive)
- **Recharts** (Génération des graphiques interactifs)
- **Lucide Icons** (Icônes de l'interface)
- **html2canvas** (Génération et exportation du rapport en image)
- **Babel** (Transpilation du JSX à la volée dans le navigateur)

## 📋 Comment l'utiliser ?

1. **Ouvrir l'application** :
   Double-cliquez simplement sur le fichier `index.html` pour l'ouvrir dans votre navigateur web moderne préféré (Chrome, Firefox, Edge, Safari). *Une connexion internet est requise lors de l'ouverture pour charger les bibliothèques CDN.*

2. **Récupérer les logs Git** :
   Ouvrez un terminal, placez-vous dans le dossier de votre projet Git, et exécutez la commande suivante :
   ```bash
   git log --date=local --pretty=format:"%h %ad %s"
   ```

3. **Générer le rapport** :
   - Copiez le résultat de la commande précédente.
   - Collez-le dans la zone de texte prévue à cet effet dans l'application.
   - Cliquez sur "Générer le Rapport".

4. **Personnaliser et Exporter** :
   - Naviguez dans l'onglet "Configuration" pour ajuster vos horaires et jours de congés.
   - Consultez l'onglet "Rapport" pour voir les graphiques et statistiques.
   - Cliquez sur le bouton d'exportation pour télécharger votre rapport en image PNG.

## 📦 Installation

**Aucune installation n'est requise.** 
Le projet ne nécessite pas de serveur Node.js, de base de données ou de processus de build complexe. Tout le code logique, le style et la structure sont regroupés dans le fichier `index.html`.

## 🔒 Confidentialité

Toutes les analyses sont effectuées **localement dans votre navigateur**. Aucune donnée de vos logs Git n'est envoyée vers un serveur externe.
