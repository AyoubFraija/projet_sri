# Moteur de Recherche en Droit Commercial

Ce projet est un moteur de recherche spécialisé dans le domaine du droit commercial, conçu pour permettre une recherche efficace et pertinente dans un corpus de documents juridiques.

## 🚀 Fonctionnalités

- **Recherche Multi-mode** :
  - Recherche par mots-clés (TF-IDF)
  - Recherche sémantique (BERT)
  - Recherche hybride (combinaison des deux approches)
- **Interface utilisateur intuitive** avec Streamlit
- **API REST** avec FastAPI
- **Traitement avancé du texte juridique** avec spaCy
- **Indexation automatique** des documents PDF
- **Visualisation des résultats** avec aperçu du contenu

## 🛠️ Technologies Utilisées

- **Backend** :
  - FastAPI (API REST)
  - Whoosh (Moteur d'indexation)
  - spaCy (NLP)
  - Sentence Transformers (BERT)
  - PyPDF2 (Lecture PDF)

- **Frontend** :
  - Streamlit
  - Requests

## 📋 Prérequis

- Python 3.8+
- pip (gestionnaire de paquets Python)

## 🔧 Installation

1. Clonez le repository :
```bash
git clone https://github.com/GithubMarbouh/projet-sri.git
cd projet-sri
```

2. Installez les dépendances :
```bash
pip install -r requirements.txt
```

3. Téléchargez le modèle spaCy pour le français :
```bash
python -m spacy download fr_core_news_md
```

4. Placez vos documents PDF dans le dossier `data/raw/`

## 🚀 Démarrage

1. Lancez l'API FastAPI :
```bash
uvicorn app.main:app --reload
```

2. Dans un autre terminal, lancez l'interface Streamlit :
```bash
streamlit run frontend/streamlit_app.py
```

3. Accédez à :
   - Interface utilisateur : http://localhost:8501
   - Documentation API : http://localhost:8000/docs

## 📁 Structure du Projet

```
projet-sri/
├── app/
│   ├── __init__.py
│   ├── main.py          # Configuration FastAPI
│   ├── indexer.py       # Logique d'indexation
│   └── search.py        # Logique de recherche
├── data/
│   ├── raw/            # Documents PDF source
│   └── processed/      # Documents traités
├── frontend/
│   └── streamlit_app.py # Interface utilisateur
├── requirements.txt     # Dépendances
└── README.md           # Ce fichier
```

## 🔍 Utilisation

1. **Indexation** :
   - Placez vos documents PDF dans le dossier `data/raw/`
   - Cliquez sur "Réindexer les documents" dans l'interface

2. **Recherche** :
   - Choisissez le type de recherche (mots-clés, sémantique, hybride)
   - Entrez votre requête
   - Consultez les résultats avec leur score de pertinence

## 📊 Évaluation

Le système utilise plusieurs métriques pour évaluer la pertinence des résultats :
- Précision
- Rappel
- F1-Score




