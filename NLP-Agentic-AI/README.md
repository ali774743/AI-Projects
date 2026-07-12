# 🧠 NLP-Based Agentic AI System

An Agentic AI system that analyzes Amazon customer reviews using Natural Language Processing (NLP). The agent autonomously decides which actions to perform, including sentiment analysis and text summarization, based on the content of the review.

---

## 📖 Overview

This project implements an NLP-based Agentic AI architecture using Amazon customer reviews as input data.

The system combines pre-trained Transformer models from Hugging Face with an agent framework consisting of four key components:

- Perception
- Planning
- Action
- Memory

Instead of following a fixed workflow, the agent examines the input review and determines which NLP tools should be executed. Depending on the review content, the agent may perform sentiment analysis, text summarization, or both.

The project demonstrates how autonomous decision-making can be integrated with NLP pipelines to create intelligent systems capable of selecting their own actions.

---

## 🎯 Objectives

The goals of this project are:

- Implement an Agentic AI architecture.
- Perform sentiment analysis using Transformer models.
- Generate summaries for lengthy reviews.
- Demonstrate autonomous task selection.
- Evaluate NLP model performance using standard metrics.

---

## 🤖 What is Agentic AI?

Agentic AI refers to systems capable of making decisions about how to solve a problem instead of following a rigid sequence of instructions.

The agent implemented in this project consists of four components:

### 👀 Perception

Receives and processes incoming information.

### 🧠 Planning

Determines which NLP actions are required.

### ⚡ Action

Executes the selected NLP tools.

### 💾 Memory

Stores generated outputs for future reference.

---

## 🏗️ System Architecture

```text
                 Amazon Review
                       │
                       ▼
                  Perception
                       │
                       ▼
                    Planning
                       │
           ┌───────────┴───────────┐
           │                       │
           ▼                       ▼
    Sentiment Analysis     Text Summarization
           │                       │
           └───────────┬───────────┘
                       ▼
                     Memory
                       │
                       ▼
                  Final Output
```

---

## ⚙️ How It Works

### Step 1: Load Dataset

The system loads Amazon customer reviews from a CSV dataset.

The dataset contains:

- Review Text
- Product Ratings

Ratings are converted into sentiment labels:

```text
4–5 Stars → Positive
3 Stars   → Neutral
1–2 Stars → Negative
```

---

### Step 2: Load NLP Models

The project uses two Hugging Face Transformer pipelines:

#### Sentiment Analysis Model

Used to identify whether a review expresses positive or negative sentiment.

#### Summarization Model

Used to generate concise summaries of lengthy customer reviews.

---

### Step 3: Agent Perception

The Perception module receives a review and prepares it for analysis.

Example:

```text
This product is amazing. The battery life is excellent and performance is outstanding.
```

---

### Step 4: Agent Planning

The Planning module decides which actions should be executed.

Rules used by the agent:

- Reviews longer than 15 words → Summarization
- Reviews containing opinion-based terms such as good, bad, great, or poor → Sentiment Analysis
- Reviews meeting both conditions → Both tasks

---

### Step 5: Agent Action

The selected NLP tools are executed.

#### Sentiment Analysis

Example:

```text
Review:
This product exceeded my expectations.

Output:
POSITIVE
```

#### Text Summarization

Example:

```text
Review:
The product arrived quickly and worked perfectly. The battery lasted all day and the overall build quality was excellent.

Summary:
Excellent product with strong battery life and build quality.
```

---

### Step 6: Memory Storage

The generated results are stored inside the agent's memory component.

Stored outputs may include:

- Sentiment Results
- Generated Summaries

This allows the agent to retain information about previous actions.

---

### Step 7: Final Output

The agent returns the generated results.

Example:

```text
{
  'sentiment': 'POSITIVE',
  'summary': 'Excellent product with strong battery life and build quality.'
}
```

---

## ✨ Features

- Agentic AI Architecture
- Autonomous Task Selection
- Sentiment Analysis
- Text Summarization
- Transformer-Based NLP
- Memory Component
- Amazon Review Analysis
- Dynamic Decision Making

---

## 🛠️ Technologies Used

### Programming Language

- Python

### Libraries

- Transformers
- PyTorch
- Pandas
- Scikit-Learn
- SentencePiece

### Models

- Hugging Face Sentiment Analysis Pipeline
- Hugging Face Summarization Pipeline

---

## 📂 Dataset

The project uses:

```text
amazon_reviews.csv
```

Important columns:

```text
reviewText
overall
```

The dataset is used for:

- Sentiment Classification
- Review Summarization
- Agent Evaluation

---

## 📊 Model Evaluation

The sentiment analysis model is evaluated using:

### Accuracy

Measures overall prediction correctness.

### F1 Score

Measures the balance between precision and recall.

Evaluation is performed on a subset of Amazon reviews to assess model performance.

---

## 💬 Sample Output

### Sentiment Analysis

```text
Review:
This product works perfectly and exceeded expectations.

Output:
POSITIVE
```

### Summarization

```text
Review:
The product arrived quickly and worked flawlessly. Battery life exceeded expectations and overall quality was excellent.

Summary:
Excellent product with reliable performance and battery life.
```

### Agent Output

```text
{
  'sentiment': 'POSITIVE',
  'summary': 'Excellent product with reliable performance and battery life.'
}
```

---

## 🌍 Applications

This project can be applied to:

- Customer Feedback Analysis
- Review Mining
- Market Research
- E-Commerce Platforms
- Opinion Analysis
- Intelligent Review Systems

---

## 🚀 Future Improvements

Potential future enhancements include:

- Multi-Agent Architectures
- Retrieval-Augmented Generation (RAG)
- Long-Term Memory Systems
- Real-Time User Interaction
- Web-Based Interface
- Tool-Augmented Agents

---

## 📸 Demonstration

Add screenshots showing:

### Dataset Loading

### Agent Output

### Sentiment Analysis Results

### Text Summarization Results

### Evaluation Metrics

---

## 👨‍💻 Author

**Ali Raza**

AI & Machine Learning Enthusiast

Interested in Agentic AI, NLP, Deep Learning, Generative AI, and Intelligent Systems.
