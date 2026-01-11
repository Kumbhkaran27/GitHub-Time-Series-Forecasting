📊 GitHub Time-Series Forecasting

A full-stack project that retrieves GitHub repository activity metrics and forecasts trends using time-series models.
It combines data retrieval, forecasting, and interactive visualization into a Docker-ready, microservices-based architecture.

🚀 Project Summary

This application:

✅ Fetches GitHub repo metrics (stars, forks, issues, contributors) via the GitHub API
✅ Stores and indexes data using Elasticsearch
✅ Provides time-series forecasting using:

TensorFlow/Keras (LSTM/Neural models)

Prophet

StatsModels
✅ Features interactive visualizations and semantic search
✅ Deploys as Dockerized microservices on Google Cloud
👉 Live demo (may require valid tokens): https://react2-409252817409.us-central1.run.app/

🧠 Key Features
📌 Data Ingestion

Pulls GitHub activity using authenticated API requests

Supports multiple repos

Stores data in Elasticsearch for indexing and fast search

📈 Time-Series Forecasting

Predicts future activity using multiple forecasting methods:

Neural networks (TensorFlow)

Prophet (seasonal + trend decomposition)

StatsModels (traditional statistical models)

📊 Visualization & UI

Interactive charts and tables

Semantic search to query similar issues across repos

Frontend dashboard built with React

🐳 Deployment

Docker Compose setup for backend, frontend, and services

Suitable for cloud deployment (e.g., Google Cloud Run)

🛠 Tech Stack
Layer	Technology
Frontend	React, JavaScript
Backend	Flask (Python)
Forecasting	TensorFlow/Keras, Prophet, StatsModels
Data Store & Search	Elasticsearch
Deployment	Docker, Google Cloud
API	GitHub REST API
📁 Repository Structure


🧪 Installation & Setup
🔹 Clone the Repo
git clone https://github.com/Kumbhkaran27/GitHub-Time-Series-Forecasting.git
cd GitHub-Time-Series-Forecasting

🔹 Prerequisites

Install:

✔ Docker & Docker Compose
✔ Python 3.8+
✔ Node.js & npm/yarn

🔹 Environment Variables

Create a .env file:

GITHUB_TOKEN=<your_github_token>
ELASTIC_HOST=<elasticsearch_host>
ELASTIC_PORT=<elasticsearch_port>
FLASK_ENV=development


GitHub tokens are required because unauthenticated requests are rate-limited.

🐳 Run via Docker Compose
docker compose up --build


This brings up:

📌 Frontend (React)
📌 Backend (Flask)
📌 Elasticsearch
📌 Forecast workers

Navigate browser to:

http://localhost:3000

🚀 How to Use
🔹 Step 1 — Fetch Repo Data

Use the UI or API endpoint to fetch metrics for one or more GitHub repos.

Example endpoint:

POST /api/repos
{
  "full_name": "owner/repo"
}

🔹 Step 2 — Forecast Metrics

Choose forecasting method:

Prophet

StatsModels

LSTM

Select a metric (e.g., stars or issues) and run predictions.

🔹 Step 3 — View Interactive Charts

Dashboards will show:

📈 historical data
🔮 future forecasts
🔍 semantic search results

⚙️ Forecast Models Included
Model	Type	Strength
Prophet	Additive/Multiplicative	Handles seasonality
StatsModels	ARIMA/SARIMA	Statistical forecasting
TensorFlow	LSTM/Deep model	Captures nonlinear trends
🧠 Design Decisions

🎯 Why Elasticsearch?
For efficient search + near-real-time indexing of GitHub content.

🎯 Why multiple forecasting models?
Allows comparison of traditional vs. ML-based predictions.

🎯 Why microservices?
Scalability & easier deployment to cloud platforms.

🛣 Future Enhancements

✨ Add authentication + user dashboard
✨ Historical data caching
✨ Alerting (e.g., repository anomaly alerts)
✨ Export forecasts as CSV/Excel
