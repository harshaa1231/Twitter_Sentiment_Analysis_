# Project Overview
This project focuses on enhancing the trustworthiness of AI model outputs in real-world applications. Using a Twitter sentiment analysis model ([cardiffnlp/twitter-roberta-base-sentiment](https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment)), the project explores how lightweight modifications — specifically, applying a confidence threshold — can significantly improve the reliability of AI systems without retraining or fine-tuning.

Rather than forcing the model to predict every input, the system selectively abstains from making predictions when confidence is low, thereby improving user trust in the outputs.

# Key Goals
Analyze trust issues in AI predictions, particularly low-confidence outputs.
Define measurable trust metrics: Accuracy and Coverage.
Implement a simple but effective trust-enhancing strategy: Confidence Thresholding (set at 70%).
Evaluate system behavior before and after applying the trust improvement.
Simulate real-world interaction through manual and random tweet testing.

# Problem Addressed
Low-confidence AI predictions can mislead users, damage trust, and create poor user experiences. In fraud detection and user-facing product environments, trustworthy outputs are critical — it is better to refrain from predicting than to provide misleading or incorrect information. This project demonstrates how applying a confidence-based filtering mechanism can strengthen the system’s trustworthiness in practice.

# Technical Approach
Dataset: [TweetEval Sentiment Analysis subset (Hugging Face Datasets)](https://huggingface.co/datasets/cardiffnlp/tweet_eval)
Model: cardiffnlp/twitter-roberta-base-sentiment
Metrics:
Accuracy: Correct predictions after applying threshold
Coverage: Percentage of inputs the system confidently acts upon
Enhancement Strategy: Confidence Threshold at 70%

# Evaluation:
Distribution of confidence scores
Accuracy before and after thresholding
Coverage before and after thresholding
Random input testing and manual interaction

# Key Insights
Many predictions initially had confidence between 50–75%.
Applying a confidence threshold improved prediction trustworthiness significantly.
Trust improvement comes at the cost of some coverage — a classic precision-recall tradeoff.
Lightweight interventions like thresholding offer a practical, explainable path to more reliable AI systems.

# Applications
This approach and methodology are directly applicable to:
Product Data Science: Improving user-facing AI system reliability and transparency.
Fraud/Abuse Detection: Filtering uncertain outputs to avoid false positives and improve risk-based decisions.
Responsible AI Practices: Building systems that act transparently, fairly, and reliably in uncertain conditions.

