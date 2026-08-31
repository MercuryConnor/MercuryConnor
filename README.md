<div align="center">

# Mrityunjay Chauhan

**ML / AI Engineer · Data Analyst · Full-Stack Builder**

*I turn raw data into production systems — statistical models, deep learning pipelines,<br>
and intelligent backends that ship and scale.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mrityunjay-chauhan-5b1813265/)
[![Medium](https://img.shields.io/badge/Medium-000000?style=flat&logo=medium&logoColor=white)](https://medium.com/@mrityunjaychauhan0102)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat&logo=leetcode&logoColor=white)](https://leetcode.com/u/mrityunjaychauhan/)
[![CodeChef](https://img.shields.io/badge/CodeChef-5B4638?style=flat&logo=codechef&logoColor=white)](https://www.codechef.com/users/mrityunjay2202)
![Profile views](https://komarev.com/ghpvc/?username=MercuryConnor&style=flat&color=blue)

</div>

---

## About

- 🎓 CS Graduate with a focus on **Machine Learning, Deep Learning, and Applied Analytics**
- 🏗️ I build end-to-end: from research notebooks to deployed APIs, intelligent backends, and live dashboards
- 🤖 Increasingly focused on **AI engineering, RAG systems, agentic workflows, and production LLM applications**
- 🔬 Projects span **AI engineering, sports analytics, medical AI, NLP, quantitative finance, federated learning, and climate tech**
- 📍 Based in India · Open to **ML Engineering, AI Engineering, Data Science, and Analyst roles** globally
- 📝 Occasional writer on [Medium](https://medium.com/@mrityunjaychauhan0102) — model write-ups, project post-mortems, and engineering lessons

---

# Featured AI Engineering Project

### [Lenny Growth Assistant](https://github.com/MercuryConnor/lenny-growth-assistant) &nbsp; ![FDE](https://img.shields.io/badge/FDE_Take--Home-2563EB?style=flat-square)

*Grounded AI workspace for turning Lenny's Podcast conversations into product and growth answers, reusable writing, and interactive artifacts.*

**The problem**

Product and growth teams have access to hours of expert conversations, but finding the right idea at the right moment is slow. A useful assistant needs to do more than generate plausible PM advice. It needs to retrieve relevant source material, preserve conversational context, show where an answer came from, and turn that knowledge into something reusable.

The additional challenge was operational: the system needed to be reproducible for another engineer, including a local Ollama demo and an external transcript corpus that was not available on the developer's machine.

**The methodology**

- Built a full-stack **RAG system** using PostgreSQL + pgvector for semantic retrieval over Lenny's Podcast transcripts
- Designed an ingestion pipeline that parses, chunks, embeds, and stores transcript content using `nomic-embed-text`
- Implemented explicit **LLM provider routing** across local Ollama, Anthropic, and Gemini
- Added skill-based agent routing for **grounded Q&A, Ship 30 for 30 essays, and HTML artifact generation**
- Persisted sessions, messages, and generated artifacts using PostgreSQL
- Built a sandboxed artifact viewer allowing generated HTML/CSS/JS to be rendered directly inside the application
- Designed the transcript dependency as an explicit, reproducible external data source rather than relying on a private local corpus
- Added API tests and a documented UI test plan for validating the core workflow

**Engineering decisions**

The most useful part of the project was not the happy path. It was debugging the system under real constraints:

- Containerized Ollama caused memory pressure and OOM failures → moved Ollama to the host while keeping application services containerized
- Failed ingestion could leave transcripts partially processed → changed ingestion to use transactional/idempotent processing
- Initial LLM abstraction added unnecessary complexity → simplified provider boundaries and made routing explicit
- Transcript data existed only on the developer machine → added documented corpus acquisition and ingestion instructions
- Documentation described architectural layers that did not exist → rewrote the architecture documentation against the actual implementation

**Outcome**

The result is a single workflow where a user can ask a product question, retrieve supporting podcast context, inspect the sources behind the answer, turn the response into a structured essay, or generate a live HTML artifact without leaving the application.

More importantly, the project is designed as a **handoff**, not just a demo: another engineer can understand the architecture, acquire the external corpus, run the stack, test the API, and inspect the reasoning behind the major engineering trade-offs.

**Tech Stack:** `Python` `FastAPI` `PostgreSQL` `pgvector` `Next.js` `React` `TypeScript` `Docker` `Ollama` `Gemini` `Anthropic` `LangChain` `RAG`

🎥 **[Demo walkthrough](https://youtube.com/playlist?list=PLPP3E0ihdblc&si=jZA87H7PTDMOezQD)** ·
📐 **[Architecture](https://github.com/MercuryConnor/lenny-growth-assistant/blob/main/docs/architecture.md)** ·
🧪 **[Tests](https://github.com/MercuryConnor/lenny-growth-assistant/tree/main/backend/tests)**

---

## Other Projects

### [PneuScan](https://github.com/MercuryConnor/PneuScan) &nbsp; ![Live](https://img.shields.io/badge/Live-46E3B7?style=flat-square&logoColor=black)

*AI-powered pneumonia detection from chest X-rays — MobileNetV2 transfer learning, full-stack deployment*

- Engineered a **MobileNetV2 transfer learning pipeline** for binary chest X-ray classification, achieving **94.1% validation accuracy** and **F1 score of 94.5%** on a 5,863-image Kaggle medical imaging dataset
- Reduced model footprint by **73%** (45 MB → 12 MB vs. custom CNN baseline) while improving accuracy by **6 percentage points** through ImageNet pretraining and domain-specific fine-tuning on labelled X-rays
- Deployed a production Flask REST API on Render and React frontend on Vercel, delivering **~200 ms per-image inference** at zero infrastructure cost across both free-tier cloud platforms
- Validated on a 624-image held-out test split — achieved **96% precision and 93% recall** on the pneumonia class, prioritising recall to minimise clinically costly missed diagnoses
- **Tech Stack:** `Python` `TensorFlow 2.x` `Keras` `MobileNetV2` `OpenCV` `Flask` `React` `Axios` `Vercel` `Render`

---

### [MarketMind AI](https://github.com/MercuryConnor/marketmind-ai) &nbsp; ![In Dev](https://img.shields.io/badge/In_Dev-F59E0B?style=flat-square)

*Agentic AI platform for real-time competitor monitoring and market intelligence*

- Architected an **agentic AI system** that autonomously monitors competitor websites, detects live pricing changes, and surfaces structured market intelligence without manual analyst intervention
- Built a semantic change-detection pipeline that computes diffs between periodic page snapshots and triggers prioritised alerts when strategically significant competitor signals are detected
- Designed an **LLM-powered natural language query interface** that converts plain business questions into automated data-retrieval and analysis workflows, eliminating repetitive manual research overhead
- Integrated a RESTful API backend enabling structured intelligence outputs to be consumed downstream by BI dashboards for real-time executive-level reporting
- **Tech Stack:** `Python` `FastAPI` `LangChain` `OpenAI API` `BeautifulSoup` `PostgreSQL` `Celery` `Docker`

---

### [WC26 Dixon-Coles Engine](https://github.com/MercuryConnor/wc26-dixon-coles-engine) &nbsp; ![Research](https://img.shields.io/badge/Research-8B5CF6?style=flat-square)

*Statistical match prediction engine for the 2026 FIFA World Cup — Dixon-Coles Poisson model + Monte Carlo simulation*

- Modelled match outcome probabilities for all **48 teams** in the 2026 FIFA World Cup by fitting a Dixon-Coles corrected bivariate Poisson goal model to historical international match data
- Implemented **time-decay weighting** across training fixtures to down-sample older results and prioritise recent team form
- Ran **Monte Carlo tournament simulations** to compute group-stage qualification rates, knockout-round win probabilities, and outright championship likelihoods across the entire 48-team bracket
- Automated the full pipeline — raw data ingestion → MLE parameter estimation → match simulation → ranked probability report
- **Tech Stack:** `Python` `SciPy` `NumPy` `pandas` `Matplotlib` `Poisson Distribution` `Monte Carlo Simulation`

---

### [AlphaTrack](https://github.com/MercuryConnor/AlphaTrack) &nbsp; ![Live](https://img.shields.io/badge/Live-46E3B7?style=flat-square&logoColor=black)

*Live quantitative stock dashboard with SMA crossover strategy, backtesting engine, and performance attribution*

- Built a full-stack quantitative trading dashboard featuring configurable SMA crossover strategy signals, interactive buy/sell visualisation, and real-time performance attribution across any equity
- Backtested RELIANCE.NS (Jan–Dec 2023) with a 20/50-day SMA strategy, generating **+18.4% total return vs. +14.2% buy-and-hold**, with a **63.6% win rate** across 11 signal-triggered trades
- Quantified downside risk with a **max drawdown of -7.1%**, enabling data-driven comparison between active strategy and passive benchmark
- Integrated yfinance for live and historical OHLCV retrieval across NSE, BSE, and global ticker symbols
- **Tech Stack:** `Python` `Streamlit` `yfinance` `pandas` `NumPy` `Matplotlib` `Plotly`

---

### [Federated Learning Simulation Platform](https://github.com/MercuryConnor/Federated-Learning-Simulation-Platform) &nbsp; ![Research](https://img.shields.io/badge/Research-8B5CF6?style=flat-square)

*Privacy-preserving distributed ML simulation — FedAvg vs. centralised baseline on heterogeneous client partitions*

- Simulated multi-client **FedAvg federated training** across non-IID partitions of a 10,000-sample synthetic binary classification dataset with 20 features
- Centralised model achieved **96.93% accuracy**; federated global model achieved **91.53% accuracy**, quantifying the **5.4 percentage-point privacy-utility trade-off**
- Applied **Dirichlet distribution (α = 0.5)** for non-IID client data partitioning
- Containerised the experimental environment with Docker for reproducible results
- **Tech Stack:** `Python 3.10` `TensorFlow 2.14.1` `TensorFlow Federated 0.73.0` `NumPy` `scikit-learn` `Docker` `Jupyter`

---

### [StayMetrics — Hotel Performance Analytics](https://github.com/MercuryConnor/StayMetrics) &nbsp; ![In Dev](https://img.shields.io/badge/In_Dev-F59E0B?style=flat-square)

*Hospitality BI framework modelling ₹67.2M in gross bookings across 6 Indian cities — Power BI ready*

- Engineered a hospitality data generation and analytics framework producing **~47,500 booking transactions** across 25–30 hotels in 6 Indian cities over **274 days**
- Modelled **₹67.2M gross revenue** with a platform commission of **₹11.8M** and partner payouts of **₹55.4M**
- Simulated operational KPIs including **52% average occupancy**, **₹738 RevPAR**, **₹1,415 average ADR**, and **1.35-night average stay**
- Built composite Poisson demand models with calibrated weekend, seasonal, monsoon, and property-type multipliers
- Produced normalised star-schema CSV tables with DAX-ready KPI definitions for direct Power BI import
- **Tech Stack:** `Python` `NumPy` `pandas` `Power BI` `DAX` `Matplotlib` `Seaborn` `Poisson Distribution`

---

### [Retail Demand Forecasting](https://github.com/MercuryConnor/Retail-Demand-Forecasting) &nbsp; ![Research](https://img.shields.io/badge/Research-8B5CF6?style=flat-square)

*Scalable big-data ML forecasting pipeline on Walmart multi-store sales — PySpark + XGBoost + Prophet*

- Architected a scalable forecasting pipeline using **PySpark 4.0.0** to process Walmart multi-store, multi-department weekly sales data
- Integrated **12 external feature dimensions** including temperature, fuel price, promotions, CPI, unemployment, holidays, store type, and store size
- Engineered lag variables, rolling averages, holiday flags, and distributed joins across multiple heterogeneous datasets
- Benchmarked **XGBoost 3.0.2** against **Prophet 1.1.7** using RMSE and MAE
- **Tech Stack:** `Python` `PySpark 4.0.0` `pandas` `XGBoost` `Prophet` `scikit-learn` `Jupyter`

---

### [Climate AI: Forest Monitoring](https://github.com/MercuryConnor/climate-ai-forest-monitoring) &nbsp; ![Research](https://img.shields.io/badge/Research-8B5CF6?style=flat-square)

*Satellite imagery + computer vision pipeline for deforestation detection and climate-driven canopy loss modelling*

- Developed a **computer vision pipeline for satellite-based forest cover change detection**, processing multi-temporal remote sensing imagery
- Applied image segmentation and temporal differencing to identify canopy loss events and estimate land-cover changes
- Trained a CNN-based land-cover classifier to distinguish forested, degraded, and non-forested regions
- Built a geospatial preprocessing workflow integrating satellite imagery with deep learning inference
- **Tech Stack:** `Python` `TensorFlow` `Keras` `OpenCV` `NumPy` `pandas` `Matplotlib` `Jupyter` `scikit-learn`

---

### [DMARS — Domain Marketplace Backend](https://github.com/MercuryConnor/dmars-domain-marketplace-backend) &nbsp; ![In Dev](https://img.shields.io/badge/In_Dev-F59E0B?style=flat-square)

*Production-grade RESTful marketplace backend with explainable ML-style ranking engine — 12 endpoints, 5 phases*

- Architected a **production-grade RESTful API** across 12 documented endpoints covering domain CRUD, marketplace analytics, and recommendations
- Built a deterministic ranking engine scoring unsold domains 0–100 using keyword relevance, engagement CTR, price competitiveness, and conversion signals
- Implemented on-demand marketplace analytics using SQL aggregation with no stored derived metrics
- Designed across clean architectural layers: ORM models → Pydantic schemas → CRUD → analytics → recommendation API
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
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)

### Data · Analytics · Visualisation

![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3776AB?style=flat&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

### Backend · APIs · Infrastructure

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-PostgreSQL-336791?style=flat)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

### Frontend · Dashboards

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)

### Deployment

![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat&logo=render&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)

---

# 📊 GitHub Stats

![](https://github-readme-stats.shion.dev/api?username=MercuryConnor&theme=shadow_green&hide_border=false&include_all_commits=true&count_private=true)<br/>
![](https://streak-stats.demolab.com/?user=MercuryConnor&theme=shadow_green&hide_border=false)<br/>
![](https://github-readme-stats.shion.dev/api/top-langs/?username=MercuryConnor&theme=shadow_green&hide_border=false&include_all_commits=true&count_private=true&layout=compact)

---

<div align="center">

<i>Always open to conversations about ML research, AI engineering, analytics challenges, or interesting data problems.</i>

<br><br>

<a href="https://www.linkedin.com/in/mrityunjay-chauhan-5b1813265/">
  <img src="https://img.shields.io/badge/Let's_connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

</div>
