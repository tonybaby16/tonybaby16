# Hi, I'm Tony 👋

Data & Analytics Leader · Hands-on Builder

I'm a hands-on Data & Analytics leader with over a decade of experience turning data strategy into measurable business outcomes — across SaaS, Smart Building, and Healthcare tech environments. I've led the full spectrum: standing up data engineering foundations, scaling 0→1 analytics products, building BI capabilities, and growing high-performing teams.

During the day I set data vision and partner with Engineering, Product, and Business to make it real. Outside of work, I stay sharp by building the projects you see below — production pipelines, live dashboards, and ML models, all from scratch.

- 🔭 **Specialties:** Data Engineering · Data Strategy · BI · ML Modelling · Scaling 0→1 SaaS data products
- ✍️ **Writing** about career & work at [careeradvisor.substack.com](https://careeradvisor.substack.com)
- 🔗 **Connect** on [LinkedIn](https://www.linkedin.com/in/totonybaby/)

---

## 🛠 Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?style=flat&logo=googlebigquery&logoColor=white)
![Google Cloud](https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-02569B?style=flat&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

---

## 🚀 Featured Projects

### 🗄️ Data Engineering — [SEC Insider Trading Pipeline](https://github.com/tonybaby16/sec-insider-report)

[![Pipeline](https://github.com/tonybaby16/sec-insider-report/actions/workflows/pipeline.yml/badge.svg)](https://github.com/tonybaby16/sec-insider-report/actions)
[![Live App](https://img.shields.io/badge/Live%20App-Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)](https://sec-insider-report.streamlit.app)

A production-grade, end-to-end data pipeline that ingests SEC EDGAR Form 4 insider trading filings (60,000–80,000 XML documents per quarter), models them through a multi-layer data warehouse, and surfaces insights through an interactive dashboard.

**Architecture:** `SEC EDGAR → Apache Spark → GCS (Data Lake) → BigQuery → dbt → Streamlit`

| Layer | Tool | Purpose |
|---|---|---|
| Ingestion | Apache Spark | Parse & extract Form 4 XML filings with rate limiting & retry logic |
| Storage | Google Cloud Storage | Immutable Parquet data lake, partitioned by quarter |
| Warehouse | BigQuery | 4-layer architecture: raw → staging → intermediate → marts |
| Transformation | dbt Core | SQL models + 28 schema tests across all layers |
| Orchestration | GitHub Actions | Monthly scheduled pipeline — ingest → load → transform → test |
| Infrastructure | Terraform | All GCP resources provisioned as code |
| Dashboard | Streamlit | KPI metrics, insider leaderboards, company sentiment |

> **Questions it answers:** Who are the most active insider sellers? Which companies have the highest buy/sell imbalance? What is net insider sentiment by ticker?

---

### 📊 Data Analysis — [SEC S-1 Filing Tracker](https://github.com/tonybaby16/02-sec-s1-analysis)

[![Live Chart](https://img.shields.io/badge/Live%20Chart-GitHub%20Pages-222222?style=flat&logo=github&logoColor=white)](https://tonybaby16.github.io/02-sec-s1-analysis/)

A data analysis project that tracks S-1 IPO filing trends with the SEC from 1994 to present. The pipeline runs daily at 8am ET and publishes updated visualisations automatically.

**Pipeline:** `SEC EDGAR submissions.zip → Extract CIK JSONs → Process filings → Monthly counts CSV → Visualise`

**Key features:**
- Historical trend lines: current year activity vs. 1994-to-prior-year monthly averages
- Year-over-year bar chart comparisons
- Fully automated with GitHub Actions — zero manual refresh required

---

### 🤖 Machine Learning — [ASHRAE Energy Consumption Predictor](https://github.com/tonybaby16/05-energyML)

[![Live App](https://img.shields.io/badge/Live%20App-Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)](https://energyml.streamlit.app)

An end-to-end ML project that forecasts energy consumption for commercial buildings (education, office, etc.) using historical meter readings, weather data, and building metadata — from the ASHRAE Great Energy Predictor III dataset.

**Model:** LightGBM · **Validation RMSLE:** ~0.66 · **Training Time:** < 5 mins

**Key techniques:**
- **Cyclical time encoding** — Sine/Cosine transformation of hour and month so the model understands Hour 23 is adjacent to Hour 0
- **Weather lag features** — 3h and 24h rolling temperature averages to capture building thermal inertia
- **Log-transform target** — `log1p(energy)` to handle skewed distribution and reduce outlier influence
- **Time-series split validation** — Train on Jan–Sep, validate on Oct–Dec to prevent data leakage

**MLOps structure:** modularised feature engineering (`features.py`), a model factory supporting LightGBM / XGBoost / CatBoost (`models.py`), and a Streamlit app for live scenario simulation.

---

## 📂 All Projects

| Project | Domain | Stack | Live |
|---|---|---|---|
| [sec-insider-report](https://github.com/tonybaby16/sec-insider-report) | Data Engineering | Spark · dbt · BigQuery · Terraform | [▶ App](https://sec-insider-report.streamlit.app) |
| [02-sec-s1-analysis](https://github.com/tonybaby16/02-sec-s1-analysis) | Data Analysis | Python · GitHub Actions · GitHub Pages | [▶ Chart](https://tonybaby16.github.io/02-sec-s1-analysis/) |
| [05-energyML](https://github.com/tonybaby16/05-energyML) | Machine Learning | LightGBM · scikit-learn · Streamlit | [▶ App](https://energyml.streamlit.app) |
