# 🔥 BurnoutGuard AI - Guide de Déploiement & Analyse Bien-être

> **Intelligence Artificielle au service de la santé mentale en milieu professionnel.**

Ce projet est une application web PWA (Progressive Web App) qui utilise un modèle de **Machine Learning** (Régression Logistique) pour évaluer le risque de burnout chez les employés. Ce guide vous accompagne pour une installation manuelle parfaite sur Windows, macOS ou Linux.

---

## 🏗️ 1. Architecture & Fonctionnement

L'application suit une logique simple mais robuste :
1.  **Collecte** : Formulaire interactif sur les conditions de travail.
2.  **Analyse** : Le modèle `burnout_model5.pkl` traite les données normalisées par `scaler5.pkl`.
3.  **Restitution** : Dashboard dynamique avec recommandations personnalisées et plan d'action sur 4 semaines.

---

## 🚀 2. Installation Manuelle Détaillée

### 2.1. Prérequis
- **Python 3.12** recommandé (les modèles `.pkl` sont sensibles à la version de Python).
- **Navigateur moderne** (Chrome, Edge ou Firefox).

### 2.2. Configuration de l'environnement (Pas à pas)

1.  **Clonage du projet** :
    ```bash
    git clone https://github.com/iamsamahaziz/BurnoutTracker.git
    cd BurnoutTracker
    ```

2.  **Création de l'environnement virtuel (VENV)** :
    *   **Sur Windows :**
        ```bash
        python -m venv venv
        .\venv\Scripts\activate
        ```
    *   **Sur macOS/Linux :**
        ```bash
        python3 -m venv venv
        source venv/bin/activate
        ```

3.  **Installation des dépendances** :
    ```bash
    pip install --upgrade pip
    pip install -r requirements.txt
    ```

### 2.3. Lancement du serveur FlasK
```bash
python app.py
```
*L'application sera accessible sur `http://localhost:5000`.*

---

## 📊 3. Guide d'Utilisation des Fonctionnalités

### 🧪 L'Évaluation Burnout
- Remplissez les champs honnêtement.
- **Stress Level** : Notez de 1 (Détendu) à 10 (Épuisé).
- **Work Hours** : Entrez votre moyenne hebdomadaire réelle (ex: 48).

### ✨ Exercice de Respiration (Box Breathing)
Un module interactif est disponible dans le dashboard pour aider à réduire le cortisol instantanément via la méthode **4-7-8**.

### 😊 Mood Tracker heatmap
L'application enregistre localement vos humeurs dans `mood_data.json` pour afficher une carte thermique (heatmap) de votre moral sur les 30 derniers jours.

---

## 🛠️ 4. Dépannage (Troubleshooting)

- **Erreur "Model not found"** : Vérifiez que `burnout_model5.pkl` est bien à la racine du projet.
- **Erreur de version Python** : Si le site crash au chargement du modèle, assurez-vous d'utiliser la même version de Python que celle utilisée pour l'entraînement (3.12).
- **Local Storage** : Si les graphiques ne s'affichent pas, vérifiez que votre navigateur autorise les scripts locaux.

---
**Auteur** : Samah AZIZ
**Projet** : Wellness & Data Science - 2026
