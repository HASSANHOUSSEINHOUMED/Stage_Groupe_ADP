# 📊 Stage Groupe ADP - Data Analyst Projects

**Entreprise** : Groupe ADP (Aéroports de Paris)  
**Poste** : Data Analyst  
**Période** : Décembre 2023 - Juin 2024 (6 mois)  
**Type** : Stage de fin d'études

Collection de **scripts et notebooks Python** développés lors d'un stage opérationnel en **Data Engineering, Data Visualization et Intelligence Artificielle** pour supporter le pilotage stratégique et opérationnel d'une infrastructure aéroportuaire majeure.

⚠️ **Confidentialité** : Ce repository contient uniquement le code source. Toutes les données d'entreprise, identifiants, secrets et informations sensibles ont été retirés pour respecter la confidentialité du Groupe ADP.

---

## 👤 Mon Rôle : Data Analyst - 6 Mois d'Impact

En tant que **Data Analyst**, j'ai participé à une **infrastructure data complète** pour le Groupe ADP :

### 🎯 Responsabilités

✅ **Ingestion & intégration** - ETL multi-sources (APIs, BigQuery, fichiers Excel)  
✅ **Data Engineering production** - PySpark, Hive, pipelines automatisés  
✅ **Nettoyage & préparation** - Encodages, formatage, validation qualité  
✅ **Web Scraping** - Collecte data dynamique (BeautifulSoup, Selenium)  
✅ **NLP avancé** - Classification texte, sentiment analysis, topic modeling  
✅ **Analytics métier** - Analyse e-réputation, support décisions opérationnelles  

### 💡 Valeur Ajoutée

- Automatisation de **3 pipelines critiques**
- Implémentation de **7+ modèles NLP** pour analyse clients
- Support à la **direction** via insights data-driven
- Réduction des processus manuels : **40%+ gains de temps**

---

## 🔄 Flux de Données Complet (ADP)
```
Sources Externes
    ├─ APIs REST (authentification OAuth)
    ├─ Google BigQuery (connexion cloud)
    ├─ Fichiers Excel/CSV
    └─ Web Scraping (duty-free catalogues)
    
    ↓ [DATA INGESTION - My ETL Pipelines]
    
Staging Layer (Raw Data)
    ├─ Function_Staging_API
    ├─ Recuperation_BigQuery
    └─ Skytrax_Pipeline
    
    ↓ [DATA CLEANING - Preprocessing]
    
Processing Layer (Clean Data)
    ├─ Decoder_Encodage
    ├─ Validation qualité
    └─ Transformation Pandas/PySpark
    
    ↓ [HIVE WAREHOUSE]
    
Exploitation Layer (3 tables)
    ├─ Raw (données brutes)
    ├─ Processed (données nettoyées)
    └─ Reporting (prête pour BI)
    
    ↓ [DATA ANALYTICS & NLP]
    
Insights Layer
    ├─ Topic Modeling (BERTopic)
    ├─ Sentiment Analysis (RoBERTa)
    ├─ Classification (SetFit)
    └─ E-Reputation Dashboard
```

---

## 📂 Projets Implémentés

### **1️⃣ Data Engineering & ETL**

#### `Function_Staging_API_v0_8.ipynb` 🔌
**Objectif** : Pipeline d'extraction API REST production-ready

**Fonctionnalités** :
- ✅ Authentification OAuth + gestion tokens JWT
- ✅ Pagination automatique (cursors + offsets)
- ✅ Gestion des erreurs et retry logic (exponential backoff)
- ✅ Sauvegarde métadonnées dans Hive via PySpark
- ✅ Logging structuré + monitoring

**Impact** : Automatisation extraction quotidienne, zéro intervention manuelle

**Stack** : ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Requests](https://img.shields.io/badge/Requests-FFD43B?style=flat-square) ![PySpark](https://img.shields.io/badge/PySpark-FF6B6B?style=flat-square) ![Hive](https://img.shields.io/badge/Hive-FDEE21?style=flat-square)

---

#### `Recuperation_donnee_Big_Query.ipynb` ☁️
**Objectif** : Extraction optimisée depuis Google BigQuery

**Fonctionnalités** :
- ✅ Authentification service account (credentials JSON)
- ✅ Requêtes SQL paramétrées + filtrage efficace
- ✅ Partitionnement par date/année
- ✅ Compression Parquet (50%+ réduction taille)
- ✅ Incremental load (delta)

**Impact** : Accès centralisé aux données cloud, performances améliorées

**Stack** : ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![BigQuery](https://img.shields.io/badge/Google%20BigQuery-4285F4?style=flat-square&logo=google-cloud&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)

---

#### `Skytrax_finale.ipynb` ✈️
**Objectif** : Pipeline ETL complet pour enquêtes Skytrax (satisfaction clients aéroportuaires)

**Architecture 3-tiers** :

| Tiers | Description | Tables Hive |
|-------|-------------|------------|
| **Raw** | Données brutes Excel | `skytrax_raw` |
| **Processing** | Transformations Pandas + PySpark | `skytrax_processed` |
| **Reporting** | Prête pour dashboards | `skytrax_reporting` |

**Transformations appliquées** :
- ✅ Nettoyage encodages (UTF-8)
- ✅ Parsing dates multiformats
- ✅ Normalisation colonnes
- ✅ Validation règles métier
- ✅ Déduplications intelligentes

**Impact** : Données Skytrax intégrées au warehouse, qualité contrôlée

**Stack** : ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![PySpark](https://img.shields.io/badge/PySpark-FF6B6B?style=flat-square) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![Hive](https://img.shields.io/badge/Hive-FDEE21?style=flat-square)

---

### **2️⃣ Data Cleaning & Data Quality**

#### `Decoder_le_fichier_mal_encoder.ipynb` 🔧
**Objectif** : Correction des problèmes d'encodage fichiers

**Problème** : Fichiers CSV/Excel avec encodage corrompu (caractères spéciaux incorrects)

**Solution Implémentée** :
- ✅ Détection automatique encodage (chardet)
- ✅ Correction avec `ftfy` (Unicode fix)
- ✅ Validation post-correction
- ✅ Sauvegarde format UTF-8 standard

**Impact** : Récupération de **100% des données** sans perte

**Stack** : ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![ftfy](https://img.shields.io/badge/ftfy-Encoding-blue?style=flat-square) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)

---

### **3️⃣ Data Collection - Web Scraping**

#### `Scrapping_frankfurt.ipynb` 🕷️
**Objectif** : Collecte automatique catalogues duty-free (aéroports)

**Cibles Scrapées** :
- Frankfurt Duty Free (Lufthansa Group)
- Dubai Duty Free (complémentaire)

**Données Collectées** :
- 500+ produits par magasin
- Prix actuels (EUR, AED)
- Disponibilités stock
- Catégories (parfums, cosmétiques, alcools)

**Techniques** :

| Technologie | Cas d'usage |
|-----------|-----------|
| **BeautifulSoup** | Parsing HTML statique (Python) |
| **RSelenium** | JavaScript-heavy sites (R) |
| **Requests** | Requêtes HTTP directes |
| **Proxy rotation** | Éviter blocages |

**Impact** : Enrichissement catalogue produits, analyse compétitive

**Stack** : ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4-blue?style=flat-square) ![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white) ![RSelenium](https://img.shields.io/badge/R-Selenium-276DC3?style=flat-square) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)

---

### **4️⃣ Machine Learning & NLP Avancé** 🤖

#### `Classification_NLP_POI_Magasin.ipynb` 🏆 **PROJET PHARE**

**Contexte** : Analyse complète d'e-réputation multi-facettes sur **10k+ commentaires clients** (avis magasins/restaurants aéroportuaires)

**Objectif Métier** : Comprendre sentiment clients par Point of Interest (POI), identifier axes d'amélioration, tracker satisfaction temps réel

### 🧠 Architecture NLP - 7+ Modèles Implémentés

| Composant | Modèle | Technologie | Résultat |
|-----------|--------|-------------|----------|
| **Détection Langue** | langdetect | Python library | Multi-lingual support (15+ langues) |
| **Traduction Auto** | Google Translate API | Cloud API | Normalisation en anglais |
| **Topic Modeling** | BERTopic | Hugging Face | 12 topics majeurs découverts |
| **Sentiment Analysis** | RoBERTa | Transformers | Classification 3-way (pos/neg/neu) |
| **Zero-Shot** | BART | HF | Catégorisation sans données labélisées |
| **Classification Supervisée** | SetFit | Few-shot learning | Single-label + multi-label (Accuracy 92%) |
| **Aspect-Based Sentiment** | DeBERTa + ABSA | Advanced NLP | Sentiments par aspect spécifique |
| **Hyperparamètres** | Optuna | AutoML | Tuning automatique (Bayesian optimization) |
| **Experiment Tracking** | MLflow | ML Ops | Suivi 50+ runs, comparaison modèles |

### 📊 Résultats NLP

| Métrique | Valeur |
|----------|--------|
| **Commentaires traités** | 10,000+ |
| **Langues détectées** | 15+ |
| **Topics extraits** | 12 thèmes majeurs |
| **Accuracy classification** | 92% (SetFit) |
| **Modèles testés** | 7+ architectures |
| **Runs MLflow** | 50+ expériences |

### 💼 Insights Métier Générés

- ✅ **Satisfaction par POI** : Restaurants (7.2/10) > Magasins (6.8/10) > Services (6.2/10)
- ✅ **Top complaints** : Attente (23%), Propreté (18%), Personnel (15%)
- ✅ **Opportunités** : Améliorer temps d'attente → +2 points satisfaction
- ✅ **Monitoring** : Dashboard temps réel des sentiments

### 🛠️ Tech Stack NLP

![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square) ![Transformers](https://img.shields.io/badge/Transformers-orange?style=flat-square) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![BERTopic](https://img.shields.io/badge/BERTopic-4-blue?style=flat-square) ![SetFit](https://img.shields.io/badge/SetFit-blue?style=flat-square) ![Optuna](https://img.shields.io/badge/Optuna-blue?style=flat-square) ![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square)

---

## 🛠️ Stack Technique Complète

### **Data Engineering**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-FF6B6B?style=flat-square)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)

### **APIs & Data Collection**
![Requests](https://img.shields.io/badge/Requests-FFD43B?style=flat-square)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4-blue?style=flat-square)
![RSelenium](https://img.shields.io/badge/R-Selenium-276DC3?style=flat-square)

### **Cloud & Storage**
![BigQuery](https://img.shields.io/badge/Google%20BigQuery-4285F4?style=flat-square&logo=google-cloud&logoColor=white)
![Hive](https://img.shields.io/badge/Apache%20Hive-FDEE21?style=flat-square)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square)

### **NLP & Machine Learning**
![HuggingFace](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square)
![Transformers](https://img.shields.io/badge/Transformers-orange?style=flat-square)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![BERTopic](https://img.shields.io/badge/BERTopic-4-blue?style=flat-square)
![SetFit](https://img.shields.io/badge/SetFit-blue?style=flat-square)
![Optuna](https://img.shields.io/badge/Optuna-blue?style=flat-square)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square)

### **Autres Tools**
![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white)
![ftfy](https://img.shields.io/badge/ftfy-Encoding-blue?style=flat-square)

---

## 📊 Résultats & Impact Business

| Domaine | Réalisation | Impact |
|---------|-------------|--------|
| **ETL Automation** | 3 pipelines production-ready | Réduit 40%+ temps intégration manuelle |
| **Data Cleaning** | Correction encodages problématiques | 100% données récupérées |
| **Web Scraping** | 2 sources externes intégrées | Enrichissement catalogue produits |
| **NLP Models** | 7+ modèles testés, 92% accuracy | Analyse e-réputation complète |
| **Business Insights** | 12 topics + satisfaction par POI | Support pilotage direction |
| **Warehouse** | 3-tier Hive architecture | Foundation pour dashboards BI |

---

## 🎓 Compétences Démontrées

- ✅ **Data Engineering** - ETL, pipelines, PySpark, Hive
- ✅ **API Integration** - OAuth, pagination, gestion erreurs
- ✅ **Cloud Data** - BigQuery, Databricks, connexions cloud
- ✅ **Web Scraping** - BeautifulSoup, Selenium (Python & R)
- ✅ **Data Cleaning** - Encodages, validation, formatage
- ✅ **NLP Avancé** - Transformers, BERTopic, SetFit, ABSA
- ✅ **ML Ops** - Optuna hypertuning, MLflow experiment tracking
- ✅ **Business Analytics** - Insights clients, support décisions
- ✅ **SQL & Hive** - Requêtes complexes, optimisation

---

## 👤 Auteur

**Hassan HOUSSEIN HOUMED**  
📚 Mastèr 2 Ingénierie Mathématiques et Biostatistique - Université Paris Cité
💼 Data Analyst - Groupe ADP (7 mois, Décembre 2023 - Juin 2024)  
📧 hassan.houssein.houmed@gmail.com  
🐙 GitHub : https://github.com/HASSANHOUSSEINHOUMED

---

<div align="center">

**Dernière mise à jour** : Décembre 2025  
**Confidentialité** : Aucune donnée sensible du Groupe ADP n'est incluse ✅

</div>
