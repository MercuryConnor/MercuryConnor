<div align="center">

# Mrityunjay Chauhan

**ML / AI Engineer · Data Analyst · Full-Stack Builder**

*I turn raw data into production systems — statistical models, deep learning pipelines,<br>and intelligent backends that ship and scale.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mrityunjay-chauhan-5b1813265/)
[![Medium](https://img.shields.io/badge/Medium-000000?style=flat&logo=medium&logoColor=white)](https://medium.com/@mrityunjaychauhan0102)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat&logo=leetcode&logoColor=white)](https://leetcode.com/u/mrityunjaychauhan/)
[![CodeChef](https://img.shields.io/badge/CodeChef-5B4638?style=flat&logo=codechef&logoColor=white)](https://www.codechef.com/users/mrityunjay2202)
![Profile views](https://komarev.com/ghpvc/?username=MercuryConnor&style=flat&color=blue)

</div>

---

## About

- 🎓 CS Graduate with a focus on **Machine Learning, Deep Learning, and Applied Analytics**
- 🏗️ I build end-to-end: from research notebooks to deployed APIs and live dashboards
- 🔬 Projects span **sports analytics, medical AI, NLP, federated learning, and climate tech**
- 📍 Based in India · Open to **ML Engineering, Data Science, and Analyst roles** globally
- 📝 Occasional writer on [Medium](https://medium.com/@mrityunjaychauhan0102) — model write-ups, project post-mortems

---


## Projects
 
### [PneuScan](https://github.com/MercuryConnor/PneuScan) &nbsp; ![Live](https://img.shields.io/badge/Live-46E3B7?style=flat-square&logoColor=black)
*AI-powered pneumonia detection from chest X-rays — MobileNetV2 transfer learning, full-stack deployment*
 
- Engineered a **MobileNetV2 transfer learning pipeline** for binary chest X-ray classification, achieving **94.1% validation accuracy** and **F1 score of 94.5%** on a 5,863-image Kaggle medical imaging dataset
- Reduced model footprint by **73%** (45 MB → 12 MB vs. custom CNN baseline) while improving accuracy by **6 percentage points** through ImageNet pretraining and domain-specific fine-tuning on labelled X-rays
- Deployed a production Flask REST API on Render and React frontend on Vercel, delivering **~200 ms per-image inference** at zero infrastructure cost across both free-tier cloud platforms
- Validated on a 624-image held-out test split — achieved **96% precision and 93% recall** on the pneumonia class, prioritising recall to minimise clinically costly missed diagnoses
- **Tech Stack:** `Python` `TensorFlow 2.x` `Keras` `MobileNetV2` `OpenCV` `Flask` `React` `Axios` `Vercel` `Render`
---
 
### [WC26 Dixon-Coles Engine](https://github.com/MercuryConnor/wc26-dixon-coles-engine) &nbsp; ![Research](https://img.shields.io/badge/Research-8B5CF6?style=flat-square)
*Statistical match prediction engine for the 2026 FIFA World Cup — Dixon-Coles Poisson model + Monte Carlo simulation*
 
- Modelled match outcome probabilities for all **48 teams** in the 2026 FIFA World Cup by fitting a Dixon-Coles corrected bivariate Poisson goal model to historical international match data
- Implemented **time-decay weighting** across training fixtures to down-sample older results and prioritise recent team form, improving predictive calibration on recency-sensitive tournament brackets
- Ran **Monte Carlo tournament simulations** to compute group-stage qualification rates, knockout-round win probabilities, and outright championship likelihoods across the entire 48-team bracket
- Automated the full pipeline — raw data ingestion → MLE parameter estimation → match simulation → ranked probability report — with zero manual steps between data input and final output
- **Tech Stack:** `Python` `SciPy` `NumPy` `pandas` `Matplotlib` `Poisson Distribution` `Monte Carlo Simulation`
---
 
### [MarketMind AI](https://github.com/MercuryConnor/marketmind-ai) &nbsp; ![In Dev](https://img.shields.io/badge/In_Dev-F59E0B?style=flat-square)
*Agentic AI platform for real-time competitor monitoring and market intelligence*
 
- Architected an **agentic AI system** that autonomously monitors competitor websites, detects live pricing changes, and surfaces structured market intelligence without manual analyst intervention
- Built a semantic change-detection pipeline that computes diffs between periodic page snapshots and triggers prioritised alerts the moment strategically significant competitor signals are detected
- Designed an **LLM-powered natural language query interface** that converts plain business questions into automated data-retrieval and analysis workflows, eliminating repetitive manual research overhead
- Integrated a RESTful API backend enabling structured intelligence outputs to be consumed downstream by BI dashboards (Grafana, Power BI) for real-time executive-level reporting
- **Tech Stack:** `Python` `FastAPI` `LangChain` `OpenAI API` `BeautifulSoup` `PostgreSQL` `Celery` `Docker`
---
 
### [AlphaTrack](https://github.com/MercuryConnor/AlphaTrack) &nbsp; ![Live](https://img.shields.io/badge/Live-46E3B7?style=flat-square&logoColor=black)
*Live quantitative stock dashboard with SMA crossover strategy, backtesting engine, and performance attribution*
 
- Built a full-stack quantitative trading dashboard featuring configurable SMA crossover strategy signals, interactive buy/sell visualisation, and real-time performance attribution across any equity
- Backtested RELIANCE.NS (Jan–Dec 2023) with a 20/50-day SMA strategy, generating **+18.4% total return vs. +14.2% buy-and-hold**, with a **63.6% win rate** across 11 signal-triggered trades
- Quantified downside risk with a **max drawdown of -7.1%**, enabling data-driven comparison between active strategy and passive benchmark in a single unified dashboard view
- Integrated yfinance for live and historical OHLCV retrieval across any NSE, BSE, or global ticker symbol — zero code changes required to switch between equities
- **Tech Stack:** `Python` `Streamlit` `yfinance` `pandas` `NumPy` `Matplotlib` `Plotly`
---
 
### [Federated Learning Simulation Platform](https://github.com/MercuryConnor/Federated-Learning-Simulation-Platform) &nbsp; ![Research](https://img.shields.io/badge/Research-8B5CF6?style=flat-square)
*Privacy-preserving distributed ML simulation — FedAvg vs. centralised baseline on heterogeneous client partitions*
 
- Simulated multi-client **FedAvg federated training** across non-IID partitions of a 10,000-sample synthetic binary classification dataset with 20 features, and benchmarked directly against a centralised baseline
- Centralised model achieved **96.93% accuracy (loss: 0.1166)**; federated global model achieved **91.53% accuracy (loss: 0.2429)** — precisely quantifying the **5.4 percentage-point privacy-utility trade-off**
- Applied **Dirichlet distribution (α = 0.5)** for non-IID client data partitioning across a 65% / 20% / 15% train-validation-test split, simulating realistic data heterogeneity across federated clients
- Containerised the full experimental environment with Docker for fully reproducible results; modular architecture supports plug-and-play substitution of aggregation strategies (FedAvg, FedProx)
- **Tech Stack:** `Python 3.10` `TensorFlow 2.14.1` `TensorFlow Federated 0.73.0` `NumPy 1.26.4` `scikit-learn 1.3.2` `Matplotlib 3.8.2` `Seaborn 0.13.2` `Docker` `Jupyter`
---
 
### [StayMetrics — Hotel Performance Analytics](https://github.com/MercuryConnor/StayMetrics) &nbsp; ![In Dev](https://img.shields.io/badge/In_Dev-F59E0B?style=flat-square)
*Hospitality BI framework modelling ₹67.2M in gross bookings across 6 Indian cities — Power BI ready*
 
- Engineered a hospitality data generation and analytics framework producing **~47,500 booking transactions** across 25–30 hotels in 6 Indian cities (Metro, Tourist, Tier-2) over **274 days** (Jun 2024 – Feb 2025)
- Modelled **₹67.2M gross revenue** with a platform commission of **₹11.8M** (avg 17.5%, range 10–27%) and partner payouts of **₹55.4M**; refund liability tracked at **~₹2.5M** across 6,500 cancellations
- Simulated realistic operational KPIs — **52% avg occupancy**, **₹738 RevPAR**, **₹1,415 avg ADR**, **1.35-night avg stay** — with Budget properties at 70–85% and Premium at 35–50% occupancy
- Built composite Poisson demand models with empirically calibrated multipliers: **weekend +18%**, **peak tourist season +25%**, **monsoon −18%**, and property-type adjustments ranging **±40%** by segment
- Produced 4 normalised, star-schema CSV tables (hotel_master, booking_data, cancellation_data, revenue_payments) with DAX-ready KPI definitions for direct Power BI dimensional model import
- **Tech Stack:** `Python` `NumPy` `pandas` `Power BI` `DAX` `Matplotlib` `Seaborn` `Poisson Distribution`
---
 
### [Retail Demand Forecasting](https://github.com/MercuryConnor/Retail-Demand-Forecasting) &nbsp; ![Research](https://img.shields.io/badge/Research-8B5CF6?style=flat-square)
*Scalable big-data ML forecasting pipeline on Walmart multi-store sales — PySpark + XGBoost + Prophet*
 
- Architected a **scalable forecasting pipeline using PySpark 4.0.0** to process Walmart multi-store, multi-department weekly sales data with distributed computation, handling the full dataset without memory constraints
- Integrated **12 external feature dimensions** — Temperature, Fuel Price, MarkDown1–5 (promotional spend), CPI, Unemployment, IsHoliday, and store Type/Size metadata — to enrich raw sales history with macroeconomic and operational signals
- Engineered time-based features (lag variables, rolling averages, holiday flags) and merged 4 heterogeneous data sources (train, features, stores, test) into a single unified, model-ready schema via distributed Spark joins
- Benchmarked **XGBoost 3.0.2** (gradient boosting) against **Prophet 1.1.7** (additive time-series decomposition) on RMSE and MAE, targeting weekly sales prediction at store × department granularity
- **Tech Stack:** `Python` `PySpark 4.0.0` `pandas 2.3.1` `XGBoost 3.0.2` `Prophet 1.1.7` `scikit-learn 1.7.1` `Matplotlib 3.10.3` `Seaborn 0.13.2` `Jupyter`
---
 
### [Climate AI: Forest Monitoring](https://github.com/MercuryConnor/climate-ai-forest-monitoring) &nbsp; ![Research](https://img.shields.io/badge/Research-8B5CF6?style=flat-square)
*Satellite imagery + computer vision pipeline for deforestation detection and climate-driven canopy loss modelling*
 
- Developed a **computer vision pipeline for satellite-based forest cover change detection**, processing multi-temporal remote sensing imagery to identify, localise, and quantify deforestation events over time
- Applied image segmentation and temporal differencing on consecutive satellite snapshots to flag canopy loss events and produce land-cover area-change estimates across monitored geographic extents
- Trained a **CNN-based land-cover classifier** to distinguish forested, degraded, and non-forested regions at scale, enabling automated attribution of change events to climate or anthropogenic drivers
- Built a geospatial preprocessing workflow integrating raw satellite band data with deep learning inference to produce interpretable, analysis-ready environmental monitoring outputs for conservation decisions
- **Tech Stack:** `Python` `TensorFlow` `Keras` `OpenCV` `NumPy` `pandas` `Matplotlib` `Jupyter` `scikit-learn`
---
 
### [DMARS — Domain Marketplace Backend](https://github.com/MercuryConnor/dmars-domain-marketplace-backend) &nbsp; ![In Dev](https://img.shields.io/badge/In_Dev-F59E0B?style=flat-square)
*Production-grade RESTful marketplace backend with explainable ML-style ranking engine — 12 endpoints, 5 phases*
 
- Architected a **production-grade RESTful API** across 12 documented endpoints in 3 router groups — domain CRUD (5), marketplace analytics (3), and recommendations (2) — with full Swagger/OpenAPI auto-documentation
- Built a **4-component deterministic ranking engine** scoring all unsold domain listings 0–100: keyword relevance (30 pts), engagement CTR (25 pts), price competitiveness within category (25 pts), and conversion signal (15 pts) with sold/high-interest bonuses
- Implemented **3 on-demand analytics endpoints** computing live marketplace KPIs — global conversion rates, category-level pricing trends, and demand indicators — via SQL aggregation with zero derived metrics stored, ensuring always-accurate reporting
- Designed across **5 clean architectural layers** (ORM models → Pydantic schemas → CRUD → analytics → recommendation API), enabling independent testing, extension, and replacement at each layer without cross-layer side effects
- **Tech Stack:** `Python` `FastAPI` `SQLAlchemy` `SQLite` `Pydantic` `pandas` `Streamlit` `Matplotlib` `Uvicorn`
---

## Tech Stack

### AI · Machine Learning · Data Science
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat&logo=keras&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6600?style=flat&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)

### Data · Analytics · Visualisation
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3776AB?style=flat&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

### Backend · APIs · Infrastructure
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

### Frontend · Dashboards
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)

### Deployment
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat&logo=render&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)

---

# 📊 GitHub Stats:
![](https://github-readme-stats.shion.dev/api?username=MercuryConnor&theme=shadow_green&hide_border=false&include_all_commits=true&count_private=true)<br/>
![](https://streak-stats.demolab.com/?user=MercuryConnor&theme=shadow_green&hide_border=false)<br/>
![](https://github-readme-stats.shion.dev/api/top-langs/?username=MercuryConnor&theme=shadow_green&hide_border=false&include_all_commits=true&count_private=true&layout=compact)


<div align="center">
  <i>Always open to conversations about ML research, analytics challenges, or interesting data problems.</i><br><br>
  <a href="https://www.linkedin.com/in/mrityunjay-chauhan-5b1813265/">
    <img src="https://img.shields.io/badge/Let's_connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
</div>
