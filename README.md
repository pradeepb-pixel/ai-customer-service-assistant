<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a192f,50:112240,100:2D7EFF&height=180&section=header&text=AI%20Customer%20Service%20Assistant&fontSize=30&fontColor=64ffda&fontAlignY=45&desc=AWS%20Lex%20%7C%20LLM%20%7C%20NLP%20%7C%20Python&descSize=15&descAlignY=68&descColor=8892b0&animation=fadeIn" width="100%"/>

</div>

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-64ffda?style=flat-square&logo=python&logoColor=0a192f)
![AWS Lex](https://img.shields.io/badge/AWS-Lex-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![LLM](https://img.shields.io/badge/LLM-Powered-64ffda?style=flat-square&logo=openai&logoColor=0a192f)
![NLP](https://img.shields.io/badge/NLP-Enabled-64ffda?style=flat-square&logo=spacy&logoColor=0a192f)
![Lambda](https://img.shields.io/badge/AWS-Lambda-FF9900?style=flat-square&logo=aws-lambda&logoColor=white)
![Status](https://img.shields.io/badge/Status-Production-success?style=flat-square)

</div>

---

## 🧠 Overview

An **AI-powered banking customer service chatbot** built using **AWS Lex** and **Large Language Models (LLM)** — designed to handle high-volume customer queries intelligently, reduce support workload, and deliver faster, more accurate responses than traditional rule-based systems.

Deployed in a production banking environment at **Citi Bank** to handle real customer interactions at scale.

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                        CUSTOMER INTERFACE                           │
│              (Web  ·  Mobile App  ·  Chat Widget)                   │
└──────────────────────────┬──────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────────┐
│                        AWS LEX BOT                                  │
│         Intent Recognition  ·  Slot Filling  ·  NLU Engine         │
└──────────┬────────────────────────────────────┬─────────────────────┘
           │                                    │
           ▼                                    ▼
┌─────────────────────┐              ┌──────────────────────┐
│   AWS LAMBDA        │              │    LLM REASONING     │
│  Fulfillment Layer  │              │  (Complex Queries)   │
│  Business Logic     │              │  Context Handling    │
└──────────┬──────────┘              └──────────┬───────────┘
           │                                    │
           └────────────────┬───────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────────────┐
│                     BANKING DATA LAYER                              │
│           DynamoDB  ·  S3  ·  Core Banking APIs                    │
└─────────────────────────────────────────────────────────────────────┘
```

---

## ⚡ Key Features

| Feature | Description |
|---|---|
| 🗣️ **Natural Language Understanding** | AWS Lex NLU handles varied customer phrasing |
| 🧠 **LLM-Powered Responses** | Complex queries handled by LLM for human-like answers |
| 🔄 **Multi-turn Conversations** | Maintains context across a full conversation session |
| 🏦 **Banking Intent Coverage** | Account queries, transactions, disputes, card services |
| ⚡ **Real-time Response** | Sub-second query resolution for common intents |
| 🔒 **Secure by Design** | No PII stored in conversation logs |
| 📊 **Analytics & Monitoring** | Query tracking, fallback rates, satisfaction signals |
| 🔁 **Human Handoff** | Seamless escalation to live agent when needed |

---

## 🛠️ Tech Stack

```python
tech_stack = {
    "conversational_ai" : ["AWS Lex v2", "NLU", "Intent Classification"],
    "llm_layer"         : ["LLM Integration", "Prompt Engineering"],
    "backend"           : ["AWS Lambda", "Python 3.10+"],
    "storage"           : ["DynamoDB", "S3"],
    "nlp"               : ["NLP Pipeline", "Entity Extraction", "Slot Filling"],
    "monitoring"        : ["AWS CloudWatch", "CloudTrail"],
}
```

---

## 🚀 Getting Started

### Prerequisites

```bash
Python 3.10+
AWS Account with Lex + Lambda access
AWS CLI configured
```

### Installation

```bash
# Clone the repo
git clone https://github.com/pradeepb-pixel/ai-customer-service-assistant.git
cd ai-customer-service-assistant

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Configuration

```bash
# Set your AWS credentials
export AWS_ACCESS_KEY_ID=your_key
export AWS_SECRET_ACCESS_KEY=your_secret
export AWS_DEFAULT_REGION=us-east-1

# Set Lex Bot details
export LEX_BOT_ID=your_bot_id
export LEX_BOT_ALIAS_ID=your_alias_id
```

### Run

```bash
python main.py
```

---

## 📁 Project Structure

```
ai-customer-service-assistant/
│
├── lex_bot/
│   ├── intents/               # Intent definitions (JSON)
│   ├── slots/                 # Slot type configurations
│   └── bot_config.json        # Lex bot configuration
│
├── lambda/
│   ├── fulfillment.py         # Lambda fulfillment handler
│   ├── llm_handler.py         # LLM integration for complex queries
│   └── banking_api.py         # Core banking API connector
│
├── nlp/
│   ├── intent_classifier.py   # Custom NLP classification
│   └── entity_extractor.py    # Entity recognition pipeline
│
├── config/
│   └── settings.py            # Configuration & environment vars
│
├── main.py                    # Entry point
├── requirements.txt
└── README.md
```

---

## 🔄 How It Works

**1. Customer Sends Message** — Via web, mobile, or chat widget

**2. AWS Lex Processes** — Identifies intent and extracts key entities (slots)

**3. Simple Query** → Lambda fulfillment handles it instantly with banking data

**4. Complex Query** → Routed to LLM layer for context-aware, human-like response

**5. Response Delivered** — Back to customer in real time

**6. No Resolution** → Seamless handoff to a live human agent

---

## 📊 Results

| Metric | Outcome |
|---|---|
| ⚡ Response Time | Real-time query resolution |
| 📉 Support Workload | Significant reduction in manual support tickets |
| 🎯 Intent Accuracy | High NLU accuracy across banking query types |
| 😊 Customer Experience | Improved resolution quality and response consistency |
| 🔁 Escalation Rate | Reduced human escalations for common queries |

---

## 🏢 Built At

Designed and deployed as part of AI Engineering work at **Citi Bank** — serving real banking customers with production-grade reliability, security, and compliance standards.

---

## 👤 Author

**Pradeep B** — AI Engineer | Data Scientist

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a192f?style=flat-square&logo=linkedin&logoColor=64ffda)](https://linkedin.com/in/1199pb123)
[![Email](https://img.shields.io/badge/Email-0a192f?style=flat-square&logo=gmail&logoColor=64ffda)](mailto:pradeepb4646@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-0a192f?style=flat-square&logo=vercel&logoColor=64ffda)](https://pradeepb.dev)

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2D7EFF,50:112240,100:0a192f&height=100&section=footer" width="100%"/>

</div>

