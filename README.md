# 📊 Stage Groupe ADP - Data Analyst Projects

---

## 📌 Contexte

**Entreprise** : Groupe ADP (Aéroports de Paris)  
**Poste** : Data Analyst 

**Période** : Décembre 2023 - Juin 2024  
**Type** : Stage de fin d'études  

Collection de **scripts et notebooks Python** développés lors d'un stage opérationnel en Data Engineering, Data Visualization et Intelligence Artificielle pour supporter le pilotage stratégique et opérationnel d'une infrastructure aéroportuaire majeure.

⚠️ **Confidentialité** : Ce repository contient uniquement le code source. Toutes les données d'entreprise, identifiants, secrets et informations sensibles ont été retirés pour respecter la confidentialité du Groupe ADP.

---

## 🎯 Mon Rôle & Contributions

En tant que **Data Analyst**, j'ai participé à :

✅ **Ingestion & intégration de données** - ETL multi-sources (APIs, BigQuery, fichiers)  
✅ **Data Engineering production** - PySpark, Hive, automatisation pipelines  
✅ **Nettoyage & préparation** - Gestion d'encodages, formatage, transformation  
✅ **Web Scraping** - Collecte data via BeautifulSoup et Selenium  
✅ **NLP avancé** - Classification texte, sentiment analysis, topic modeling  
✅ **Insights métier** - Analyse d'e-réputation, support décisions opérationnelles  

**Impact** : Automatisation de processus critiques, amélioration de la prise de décision data-driven, et fourniture d'insights actionnables aux équipes opérationnelles et direction.

---

## 📂 Projets Implémentés

### 1️⃣ **Data Engineering**

#### `Function_Staging_API_v0_8.ipynb`
- **Objectif** : Extraction de données via API REST
- **Fonctionnalités** : 
  - Authentification OAuth + gestion des tokens
  - Pagination automatique
  - Gestion des erreurs et retry logic
  - Stockage des métadonnées dans Hive via PySpark
- **Stack** : Python, PySpark, Requests, Hive

#### `Recuperation_donnee_Big_Query.ipynb`
- **Objectif** : Extraction depuis Google BigQuery
- **Fonctionnalités** :
  - Connexion BigQuery authentifiée
  - Filtrage par date et paramètres
  - Sauvegarde locale optimisée
- **Stack** : Python, Google BigQuery, Pandas

#### `Skytrax_finale.ipynb`
- **Objectif** : Pipeline ETL complet pour enquêtes Skytrax
- **Fonctionnalités** :
  - Extraction depuis Excel + fichiers structurés
  - Transformation multi-étape (Pandas + PySpark)
  - Chargement dans 3 tables Hive (raw → exploitation → reporting)
  - Validation qualité données
- **Stack** : Python, PySpark, Pandas, Hive, Excel

---

### 2️⃣ **Data Cleaning & Preprocessing**

#### `Decoder_le_fichier_mal_encoder.ipynb`
- **Objectif** : Correction des problèmes d'encodage de fichiers
- **Problème résolu** : Fichiers CSV avec encodage corrompu
- **Solution** : Détection + correction automatique avec `ftfy`
- **Impact** : Données récupérables sans perte

---

### 3️⃣ **Data Collection (Web Scraping)**

#### `Scrapping_fruncfurt.ipynb`
- **Objectif** : Collecte de données de catalogues aéroportuaires
- **Cibles** : Frankfurt Duty Free, Dubai Duty Free
- **Méthode** : Web scraping avec BeautifulSoup (Python) et RSelenium (R)
- **Données** : Prix, produits, disponibilité
- **Stack** : Python, BeautifulSoup, RSelenium, Pandas

---

### 4️⃣ **Intelligence Artificielle & NLP Avancé**

#### `Classification_NLP_POI_Magasin.ipynb` 🔥
**Projet phare** : Analyse d'e-réputation multi-facettes sur commentaires clients

**Modèles & Techniques Implémentées** :

| Composant | Technologie | Objectif |
|-----------|-------------|----------|
| **Détection Langue** | langdetect | Identifier langue commentaires (multi-lingual) |
| **Traduction Auto** | Google Translate API | Normaliser en anglais |
| **Topic Modeling** | BERTopic | Découvrir thèmes majeurs |
| **Sentiment Analysis** | RoBERTa | Classification polarité (positif/négatif/neutre) |
| **Zero-Shot Classification** | BART | Catégoriser sans données labélisées |
| **Classification Supervisée** | SetFit | Single-label + multi-label classification |
| **Aspect-Based Sentiment** | DeBERTa + ABSA | Sentiments par aspect spécifique |
| **Hyperparamètres** | Optuna | Optimisation automatique |
| **Tracking Expériences** | MLflow | Suivi reproductibilité & comparaison modèles |

**Valeur Métier** : Comprendre les opinions clients par point d'intérêt commercial, identifier axes d'amélioration, tracker satisfaction temps réel.

---

## 🛠️ Stack Technique

### **Data Engineering**
- ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
- ![PySpark](https://img.shields.io/badge/PySpark-FF6B6B?style=flat-square)
- ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
- ![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)

### **APIs & Data Collection**
- ![Requests](https://img.shields.io/badge/Requests-FFD43B?style=flat-square)
- ![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4-blue?style=flat-square)
- ![RSelenium](https://img.shields.io/badge/R-Selenium-276DC3?style=flat-square)

### **Cloud & Storage**
- ![Google BigQuery](https://img.shields.io/badge/Google%20BigQuery-4285F4?style=flat-square&logo=google-cloud&logoColor=white)
- ![Hive](https://img.shields.io/badge/Apache%20Hive-FDEE21?style=flat-square)
- ![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square)

### **NLP & Machine Learning**
- ![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square)
- ![Transformers](https://img.shields.io/badge/Transformers-orange?style=flat-square)
- ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
- ![BERTopic](https://img.shields.io/badge/BERTopic-4-blue?style=flat-square)
- ![SetFit](https://img.shields.io/badge/SetFit-blue?style=flat-square)
- ![Optuna](https://img.shields.io/badge/Optuna-blue?style=flat-square)
- ![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square)

### **Autres Outils**
- ![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white)
- ![ftfy](https://img.shields.io/badge/ftfy-Encoding-blue?style=flat-square)

---

## 📊 Résultats & Impact

| Domaine | Réalisation | Impact |
|---------|-------------|--------|
| **ETL Automation** | 3 pipelines de données production-ready | Réduit temps d'intégration manuels |
| **Data Cleaning** | Correction encodages problématiques | Données récupérées sans perte |
| **Web Scraping** | 2 sources externes intégrées | Enrichissement données catalogues |
| **NLP Models** | 7+ modèles NLP avancés | Analyse e-réputation complète |
| **Decision Support** | Insights métier actionnables | Support pilotage direction |

---

## 🎓 Compétences Développées

- ✅ **Data Engineering** - ETL, pipelines, PySpark
- ✅ **API Integration** - Authentification OAuth, pagination, gestion erreurs
- ✅ **Big Data** - Hive, BigQuery, Databricks
- ✅ **Web Scraping** - BeautifulSoup, Selenium (Python & R)
- ✅ **Data Cleaning** - Gestion encodages, formatage, validation
- ✅ **NLP Avancé** - Transformers, BERTopic, SetFit, ABSA
- ✅ **ML Ops** - Optuna hyperparameter tuning, MLflow tracking
- ✅ **Business Analytics** - Insights clients, support décisions

---

## 👤 Auteur

**Hassan HOUSSEIN HOUMED**  
📚 Master 2 Ingénierie Mathématiques & Biostatistique - Université Paris Cité  
💼 Data Analyst - Groupe ADP  
📧 hassan.houssein.houmed@gmail.com  
🐙 GitHub : https://github.com/HASSANHOUSSEINHOUMED

---

**Dernière mise à jour** : Décembre 2025  
**Confidentialité** : Aucune donnée sensible du Groupe ADP n'est incluse ✅
