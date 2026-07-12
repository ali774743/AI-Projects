# Hybrid AI Chatbot with Product Recommendation System

An intelligent hybrid chatbot that combines Microsoft's **Phi-2 Large Language Model** with a custom **Product Recommendation Engine**. The system can engage in natural conversations, answer general questions, and provide data-driven product recommendations by automatically identifying the user's intent.

---

## Overview

Traditional chatbots are designed to generate conversational responses, while recommendation systems focus on ranking and suggesting products. This project combines both approaches into a single intelligent application.

The chatbot first determines whether the user's query is conversational or product-related. General questions are handled by the Phi-2 language model, while recommendation requests are processed by a custom recommendation engine that analyzes product data and returns the most relevant suggestions.

The system also maintains conversation history, allowing users to ask follow-up questions and receive context-aware responses.

---

## 🎯 Objectives

The primary objectives of this project are:

- Build a conversational AI assistant using a Large Language Model.
- Develop a product recommendation system capable of ranking products intelligently.
- Implement intent detection to automatically route queries.
- Maintain conversational context for follow-up interactions.
- Demonstrate the integration of NLP and recommendation systems within a single application.

---

## 🏗️ System Architecture

```text
                    User Query
                         │
                         ▼
                 Intent Detection
                         │
            ┌────────────┴────────────┐
            │                         │
            ▼                         ▼
     Phi-2 Language Model     Recommendation Engine
            │                         │
            └────────────┬────────────┘
                         ▼
                  Final Response
```

---

## ⚙️ How It Works

### Step 1: User Input

The user enters a query.

Examples:

```text
What is Artificial Intelligence?
```

```text
Recommend a router around $200
```

---

### Step 2: Intent Detection

The system analyzes the query to determine whether it is:

- A conversational request
- A product recommendation request

The detection process looks for:

- Product categories
- Recommendation keywords
- Budget information
- Product-related terms

---

### Step 3A: Conversational AI Processing

If the query is conversational:

1. The user's message is sent to Microsoft's Phi-2 model.
2. Previous conversation history is attached.
3. Phi-2 generates a contextual response.
4. The response is returned to the user.

Example:

```text
User: What is Machine Learning?

Bot: Machine Learning is a branch of Artificial Intelligence that enables computers to learn patterns from data and improve performance without explicit programming.
```

---

### Step 3B: Product Recommendation Processing

If the query is product-related:

1. Budget information is extracted.
2. Product category is identified.
3. Desired features are detected.
4. Products are evaluated and scored.
5. The highest-ranking products are returned.

Example:

```text
User: Recommend a security camera under $150
```

---

### Step 4: Product Scoring

Each product receives a score based on multiple factors.

#### Price Matching

Products closer to the user's budget receive higher scores.

#### Feature Matching

Products containing requested features receive additional points.

#### Product Ratings

Higher-rated products are ranked higher.

#### Review Count

Products with more customer reviews gain higher confidence scores.

#### Competition Level

Lower competition products receive better scores.

#### Profit Margin

Products with stronger profit margins receive additional ranking benefits.

---

### Step 5: Recommendation Generation

The recommendation engine returns the top-ranked products along with:

- Product Name
- Category
- Price
- Rating
- Features
- Estimated Profit Margin

---

### Step 6: Context Memory

The chatbot stores previous interactions to support follow-up questions.

Example:

```text
User: Recommend a router around $200

Bot: [Recommendations]

User: What about Ubiquiti?

Bot: [Provides information about the previously recommended Ubiquiti product]
```

This allows the chatbot to maintain conversational continuity.

---

## ✨ Features

- Hybrid AI Architecture
- Conversational AI using Phi-2
- Product Recommendation Engine
- Intent Detection
- Context-Aware Memory
- Follow-Up Question Support
- Product Ranking System
- Feature-Based Product Search
- Budget-Based Recommendations

---

## 📂 Dataset Requirement

This project requires a product dataset named:

```text
products.csv
```

The recommendation engine uses this dataset to analyze and rank products.

### Expected Dataset Columns

```text
product_name
category
price
rating
review_count
features
bsr
competition
cost_price
shipping_cost
referral_fee_rate
```

Without the dataset, the recommendation system cannot function correctly.

---

## 🛠️ Technologies Used

### Programming Language

- Python

### Libraries & Frameworks

- PyTorch
- Hugging Face Transformers
- Pandas
- SentencePiece
- Accelerate

### AI Components

- Microsoft Phi-2
- Natural Language Processing (NLP)
- Intent Detection
- Recommendation Systems

---

## ▶️ Installation

### Clone Repository

```bash
git clone https://github.com/your-username/AI-Projects.git
```

### Install Dependencies

```bash
pip install transformers accelerate sentencepiece torch pandas
```

---

## ▶️ Running the Project

### Step 1

Place the dataset file inside the project directory:

```text
products.csv
```

### Step 2

Run the chatbot:

```bash
python chatbot.py
```

---

## 💬 Example Queries

### General Conversation

```text
What is Artificial Intelligence?

Explain Neural Networks.

How does Deep Learning work?
```

### Product Recommendations

```text
Recommend a router around $200

Recommend a security camera under $150

Suggest a product with high ratings and low competition
```

### Follow-Up Questions

```text
What about Reolink?

Tell me more about Ubiquiti.
```

---

## 📊 Applications

This project can be adapted for:

- E-Commerce Platforms
- Online Shopping Assistants
- Customer Support Systems
- Product Discovery Applications
- Conversational Recommendation Systems
- Intelligent Virtual Assistants

---

## 📈 Future Improvements

Potential future enhancements include:

- Web-Based Interface
- Voice Assistant Integration
- Database Connectivity
- Personalized Recommendations
- User Authentication
- Multi-User Support
- Retrieval-Augmented Generation (RAG)
- Real-Time Product Databases

---

## 👨‍💻 Author

**Ali Raza**

AI & Machine Learning Enthusiast

Building intelligent systems using NLP, Machine Learning, Deep Learning, Generative AI, and Agentic AI.
