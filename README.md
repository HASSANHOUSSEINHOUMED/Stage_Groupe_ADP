# Projets Data Analyst/Scientist - Groupe ADP

Ce repository contient une collection de scripts et notebooks Python développés durant mon stage au sein du Groupe ADP (Aéroports de Paris) de décembre 2023 à juin 2024.

## Présentation

Durant ce stage en tant que Data Analyst/Scientist, j'ai travaillé sur plusieurs projets impliquant du data engineering, de la visualisation de données et de l'analyse de données avec des techniques d'intelligence artificielle.

> **Note** : Ce repository ne contient que les scripts et le code source. Les données d'entreprise et informations confidentielles ont été retirées pour respecter la confidentialité du Groupe ADP.

## Contenu du Repository

### 1. Data Engineering

- **`Function_Staging_API_v0_8.ipynb`** : Script pour l'extraction de données via API avec gestion des tokens d'authentification, pagination et suivi des échecs. Utilise PySpark pour stocker les métadonnées dans Hive.

- **`Recuperation_donnee_Big_Query.ipynb`** : Script pour extraire des données de Google BigQuery et les enregistrer localement avec possibilité de filtrer par date.

- **`Skytrax_finale.ipynb`** : Script complet d'ETL pour le traitement des données d'enquêtes Skytrax, comprenant l'extraction depuis des fichiers Excel, la transformation avec Pandas et PySpark, et le chargement dans différentes tables Hive (raw, exploitation, reporting).

### 2. Data Cleaning & Preprocessing

- **`Decoder_le_fichier_mal_encoder.ipynb`** : Utilitaire pour corriger les problèmes d'encodage dans les fichiers CSV en utilisant la bibliothèque ftfy.

### 3. Data Collection

- **`Scrapping_fruncfurt.ipynb`** : Script de web scraping pour collecter des données de produits depuis les sites d'aéroports (Frankfurt et Dubai Duty Free), implémenté en Python et en R.

### 4. Intelligence Artificielle & NLP

- **`Classification_NLP_POI_Magasin.ipynb`** : Modèle d'analyse NLP pour la classification et l'analyse de sentiment des commentaires clients sur les points d'intérêt commerciaux. Implémente plusieurs approches avancées :
  - Détection de langue et traduction automatique
  - Modélisation de sujets avec BERTopic
  - Analyse de sentiment avec RoBERTa
  - Classification zero-shot avec BART
  - Classification supervisée avec SetFit (single-label et multi-label)
  - Analyse de sentiment basée sur les aspects (ABSA) avec DeBERTa
  - Optimisation d'hyperparamètres avec Optuna et suivi des expériences avec MLflow

## Technologies Utilisées

- **Langages** : Python, SQL, R
- **Frameworks/Bibliothèques** : 
  - PySpark
  - Pandas
  - BeautifulSoup
  - Requests
  - RSelenium
  - Databricks
  - Transformers (Hugging Face)
  - PyTorch
  - BERTopic
  - BERT, RoBERTa, DeBERTa
  - SetFit
  - Optuna
  - MLflow
- **Stockage de données** : Hive, BigQuery
- **APIs** : REST APIs avec authentification OAuth

## Compétences Développées

- Ingestion de données via API et web scraping
- ETL (Extract, Transform, Load) avec PySpark
- Automatisation des flux de données
- Intégration des données dans un entrepôt de données (Hive)
- Nettoyage et préparation des données
- Transformation de données pour analyse et reporting
- NLP avancé (classification de texte, analyse de sentiment)
- Optimisation d'hyperparamètres et suivi d'expériences ML
- Développement de modèles pour l'analyse d'e-réputation
- Classification multi-label et analyse de sentiment basée sur les aspects

## Contact

Pour plus d'informations sur ces projets ou pour discuter de collaborations professionnelles, n'hésitez pas à me contacter sur LinkedIn.

---

*Note : Ce repository contient uniquement du code et ne comprend aucune donnée appartenant au Groupe ADP. Tous les identifiants, secrets et informations sensibles ont été retirés.*
