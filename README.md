# 🚀 AI Enterprise Model Router

<div align="center">

![GitHub stars](https://img.shields.io/github/stars/vishakha2121/ai-model-router-enterprise?style=social)
![GitHub forks](https://img.shields.io/github/forks/vishakha2121/ai-model-router-enterprise?style=social)
![GitHub issues](https://img.shields.io/github/issues/vishakha2121/ai-model-router-enterprise)
![GitHub license](https://img.shields.io/github/license/vishakha2121/ai-model-router-enterprise)
![Python Version](https://img.shields.io/badge/python-3.10+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.104.1-green.svg)
![React](https://img.shields.io/badge/React-18.2.0-blue.svg)

**An intelligent middleware system that automatically selects the most appropriate Large Language Model (LLM) for each user query based on multiple dynamic factors.**

[View Demo](https://github.com/vishakha2121/ai-model-router-enterprise) • [Report Bug](https://github.com/vishakha2121/ai-model-router-enterprise/issues) • [Request Feature](https://github.com/vishakha2121/ai-model-router-enterprise/issues)

</div>

---

## 📋 Table of Contents

- [📖 About The Project](#-about-the-project)
- [✨ Features](#-features)
- [🏗️ Architecture](#️-architecture)
- [🚀 Getting Started](#-getting-started)
- [📁 Project Structure](#-project-structure)
- [🔧 Tech Stack](#-tech-stack)
- [📊 Routing Algorithm](#-routing-algorithm)
- [📈 Performance Metrics](#-performance-metrics)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [👨‍💻 Contact](#-contact)

---

## 📖 About The Project

The **AI Enterprise Model Router** is an intelligent middleware system designed to optimize the use of multiple Large Language Models (LLMs) in enterprise environments. Instead of relying on a single model, this system intelligently routes each user query to the most suitable model based on:

- **Task Complexity** - Simple queries go to faster models, complex ones to advanced models
- **Latency Requirements** - Time-sensitive queries are routed to faster models
- **Cost Optimization** - Budget considerations influence model selection
- **Privacy Sensitivity** - Sensitive data is routed to privacy-focused models
- **Model Reliability** - Historical performance metrics guide decisions

### 🎯 Why This Project?

In today's AI landscape, organizations face a critical challenge: **which LLM to use for which task?**

| Model | Strengths | Weaknesses | Best For |
|-------|-----------|------------|----------|
| **GPT-4** | High quality, complex reasoning | Expensive, slower | Complex tasks, coding, analysis |
| **Claude** | Ethical reasoning, long context | Moderate speed | Document analysis, ethical queries |
| **Gemini** | Fast, multilingual | Moderate quality | Quick responses, multilingual |
| **Llama 2** | Free, private, open-source | Lower accuracy | Sensitive data, cost-sensitive |
| **Mistral** | Efficient, good performance | Limited features | General tasks, cost-effective |
| **Qwen** | Asian language support | Region-specific | Asian language tasks |

**The Solution:** Let the system automatically decide which model to use for each query!

---

## ✨ Features

### 🎯 **Smart Routing Engine**
- Real-time query analysis and model selection
- Weighted scoring algorithm based on multiple factors
- Automatic fallback and error handling

### 📊 **Real-time Dashboard**
- Live model performance monitoring
- Cost tracking and optimization insights
- Visual analytics and charts

### 💬 **Intelligent Chat Interface**
- Context-aware conversations
- Model badges on responses
- Response metrics display

### 🔍 **Performance Analytics**
- Model comparison charts
- Cost analysis reports
- Latency tracking
- Usage patterns

### 🗄️ **Caching System**
- Query-response caching
- Configurable expiration
- Performance optimization

### 🔒 **Privacy & Security**
- Privacy-preserving routing
- Sensitive data detection
- Secure API key management

---

## 🏗️ Architecture

---

## 🚀 Getting Started

### 📋 Prerequisites

- **Python 3.10+**
- **Node.js 16+**
- **npm or yarn**
- **Git**
- **Google Gemini API Key** (free tier available)

### 🔧 Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/vishakha2121/ai-model-router-enterprise.git
cd ai-model-router-enterprise

cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
cp .env.example .env

# Add your Gemini API key to .env
# GEMINI_API_KEY=your-api-key-here

# Initialize database
python -c "from app.database import init_db; init_db()"

# Run backend server
uvicorn app.main:app --reload --port 8000

cd ../frontend

# Install dependencies
npm install

# Create .env file
cp .env.example .env

# Run frontend server
npm start