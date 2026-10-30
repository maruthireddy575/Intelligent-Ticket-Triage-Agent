# 🎫 Intelligent Ticket Triage Agent

An AI-powered support ticket classification and prioritization system built with Python, Streamlit, and scikit-learn.

---

## 🌟 Features

- **🤖 ML-Powered Classification**: TF-IDF + Logistic Regression for 5 categories
- **📊 Risk-Based Prioritization**: Multi-factor risk scoring (category, urgency, sentiment, uncertainty)
- **🔄 State Machine**: Explicit state transitions with full logging
- **🚨 Smart Escalation**: Auto-escalates low-confidence tickets
- **📈 Full Observability**: Complete audit trail with Run IDs
- **🎯 Reproducibility**: Fixed seed ensures consistent results
- **💡 AI Insights**: Pattern detection and recommendations
- **⏳ Timeline View**: Grouped transition history by ticket

---

## 📋 Categories

| Category | Description | Base Risk |
|----------|-------------|-----------|
| 💰 Billing | Payment, invoice, refund issues | 0.6 |
| 🔧 Technical | Bugs, errors, performance | 0.5 |
| 📦 Delivery | Shipping, orders, tracking | 0.5 |
| 🔐 Account | Login, password, access | 0.4 |
| ❓ General | Questions, suggestions | 0.2 |

---

## ⚡ Priority Levels

- **🔴 High**: Risk score > 0.7
- **🟡 Medium**: Risk score 0.4 – 0.7
- **🟢 Low**: Risk score < 0.4

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| Frontend | Streamlit |
| ML Framework | scikit-learn |
| Data Processing | pandas, numpy |
| Visualization | Plotly |
| Database | SQLite |
| Sentiment Analysis | TextBlob |
| Navigation | streamlit-option-menu |

---

## 🚀 Quick Start

### Prerequisites
- Python 3.10 or higher
- pip package manager

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/intelligent-ticket-triage-agent.git
cd intelligent-ticket-triage-agent

# 2. Create virtual environment (recommended)
python -m venv venv

# Activate on Windows:
venv\Scripts\activate

# Activate on Mac/Linux:
source venv/bin/activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Train the ML model (first time only)
python train_model.py

# 5. Run the application
streamlit run app.py
