# 🧠 NLP-Based Agentic AI System

An intelligent NLP-powered Agentic AI system capable of autonomously analyzing text, selecting appropriate actions, and generating meaningful outputs through sentiment analysis and text summarization.

---

## 📖 Overview

This project explores the concept of Agentic Artificial Intelligence by combining Natural Language Processing (NLP) techniques with autonomous decision-making capabilities.

Unlike traditional NLP pipelines that follow predefined workflows, this system evaluates incoming text, determines which actions are required, and executes those actions automatically.

The agent is capable of:

- Understanding user input
- Analyzing sentiment
- Summarizing lengthy reviews
- Making decisions about which NLP tools to use
- Storing results in memory

The project uses Amazon customer reviews as a dataset and leverages pre-trained Transformer models from Hugging Face.

---

## 🎯 Objectives

The main objectives of this project are:

- Demonstrate Agentic AI principles.
- Implement autonomous decision-making.
- Perform sentiment analysis using Transformer models.
- Generate concise summaries of lengthy reviews.
- Build an architecture consisting of Perception, Planning, Memory, and Action components.

---

## 🤖 What is Agentic AI?

Agentic AI refers to systems that can independently decide how to solve a problem rather than following a fixed sequence of instructions.

An Agentic AI system typically consists of:

### 👀 Perception

Receives and interprets information from the environment.

### 🧠 Planning

Determines what actions need to be performed.

### 💾 Memory

Stores previous results and information.

### ⚡ Action

Executes tasks using available tools.

---

## 🏗️ System Architecture

```text
                 User Input
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
  Sentiment Analysis      Text Summarization
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

### Step 1: Data Loading

The system loads Amazon customer reviews from a CSV dataset.

The dataset contains:

- Review Text
- Product Ratings

---

### Step 2: Review Processing

Customer reviews are extracted and prepared for NLP analysis.

Ratings are converted into sentiment labels:

```text
4-5 Stars → Positive

3 Stars → Neutral

1-2 Stars → Negative
```

---

### Step 3: Agent Perception

The agent receives a review and analyzes its content.

Example:

```text
This product is amazing. The battery life is excellent and performance is outstanding.
```

---

### Step 4: Agent Planning

The Planning Module determines which actions should be performed.

Rules used:

- Long reviews → Summarization
- Opinion-based reviews → Sentiment Analysis
- Complex reviews → Both tasks

The agent decides this automatically.

---

### Step 5: Sentiment Analysis

The sentiment analysis model identifies the emotional tone of the review.

Possible outputs:

```text
POSITIVE

NEGATIVE
```

Example:

```text
Review:
The product exceeded my expectations.

Output:
POSITIVE
```

---

### Step 6: Text Summarization

Long reviews are compressed into concise summaries.

Example:

```text
Original Review:
The product arrived quickly...
[Long Review]

Summary:
Fast delivery and excellent product quality.
```

---

### Step 7: Memory Storage

The generated outputs are stored in memory.

Stored information includes:

- Sentiment Result
- Generated Summary

This allows the system to maintain awareness of previous actions.

---

### Step 8: Final Response

The results are returned to the user.

Example:

```text
Sentiment: Positive

Summary:
Excellent product quality with strong performance and battery life.
```

---

## ✨ Features

- Agentic AI Architecture
- Autonomous Decision Making
- Sentiment Analysis
- Text Summarization
- Memory Component
- Dynamic Task Selection
- Transformer-Based NLP
- Customer Review Analysis

---

## 🛠️ Technologies Used

### Programming Language

- Python

### Libraries & Frameworks

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

This project uses an Amazon Reviews dataset containing:

```text
reviewText
overall
```

The dataset is used for:

- Sentiment Classification
- Text Summarization
- Agent Evaluation

---

## 📊 Evaluation

The sentiment analysis component is evaluated using:

### Accuracy

Measures overall prediction correctness.

### F1 Score

Measures balance between precision and recall.

These metrics provide insight into the model's performance on customer reviews.

---

## 💬 Example Output

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
[Long Customer Review]

Summary:
Excellent product with reliable performance.
```

### Combined Agent Output

```text
Sentiment:
POSITIVE

Summary:
Excellent quality product with strong performance.
```

---

## 🌍 Real-World Applications

This system can be used for:

- Customer Feedback Analysis
- Review Mining
- Market Research
- E-Commerce Platforms
- Customer Support Systems
- Intelligent Virtual Assistants

---

## 📈 Future Improvements

Potential enhancements include:

- Multi-Agent Systems
- Retrieval-Augmented Generation (RAG)
- Long-Term Memory
- Tool-Augmented Agents
- Real-Time User Interaction
- Web-Based Interface
- Multi-Modal Inputs

---

## 📸 Demonstration

Add screenshots showing:

### Review Analysis

![Review Analysis](screenshots/review-analysis.png)

### Sentiment Detection

![Sentiment Analysis](screenshots/sentiment-analysis.png)

### Generated Summary

![Summary](screenshots/summary.png)

---

## 👨‍💻 Author

**Ali Raza**

AI & Machine Learning Enthusiast

Interested in Agentic AI, NLP, Machine Learning, Deep Learning, and Intelligent Systems.
