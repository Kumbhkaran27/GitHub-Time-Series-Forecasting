# GitHub Time-Series Forecasting

A full-stack application that collects GitHub repository activity metrics and generates time-series forecasts to predict future trends. The project combines data ingestion, indexing, forecasting, and interactive visualization in a Docker-ready microservices architecture.

---

## What this project does

This application:

- Fetches GitHub repository activity metrics (stars, forks, issues, contributors) using the GitHub REST API
- Stores and indexes the data in Elasticsearch for fast retrieval and search
- Forecasts future repository trends using multiple time-series approaches:
  - Prophet
  - StatsModels (ARIMA/SARIMA-style statistical forecasting)
  - TensorFlow / Keras (LSTM-based forecasting)
- Visualizes historical trends and predictions through an interactive React dashboard
- Supports semantic-style search on indexed repository content
- Runs locally using Docker Compose and can be deployed to cloud platforms (Google Cloud)

Live demo (may require valid GitHub tokens):
https://react2-409252817409.us-central1.run.app/

---

## Architecture overview

The system is organized into independent services:

- Frontend: React dashboard for metrics, charts, and results
- Backend API: Flask service for ingestion, retrieval, and forecasting triggers
- Search / Storage: Elasticsearch for indexing and queries
- Forecasting modules: multiple model implementations for comparisons and experimentation

This design keeps each component isolated and makes it easier to test, scale, and deploy.

---

## Key features

### Data ingestion
- Pulls GitHub activity using authenticated API requests
- Supports multiple repositories
- Indexes data for fast access and future analysis

### Forecasting
- Generates future trends using multiple models
- Allows comparing traditional time-series methods with deep learning
- Supports forecasting by metric (stars, issues, etc.)

### Visualization
- Interactive charts and tables for historical + predicted values
- Simple dashboard experience for exploring repository trends

### Deployment
- Docker Compose setup for local development
- Cloud-ready design (Google Cloud Run compatible)

---

## Tech stack

Frontend:
- React
- JavaScript

Backend:
- Python
- Flask

Forecasting:
- Prophet
- StatsModels
- TensorFlow / Keras

Search and storage:
- Elasticsearch

Deployment:
- Docker
- Google Cloud

---

## Repository setup

### Prerequisites
Make sure you have:

- Docker and Docker Compose
- Python 3.8+
- Node.js + npm (or yarn)

### Clone the repository
```bash
git clone https://github.com/Kumbhkaran27/GitHub-Time-Series-Forecasting.git
cd GitHub-Time-Series-Forecasting
