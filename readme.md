# Assignment - Do you Agree?

## Task 1: Model Training

In Task 1, we utilized the BookCorpus dataset and trained our model on 100,000 samples. The training focused on building a model for Natural Language Inference (NLI) using the Sentence-BERT architecture. We processed the text data, performed tokenization, and trained the model to classify sentence pairs into three categories: entailment, neutral, and contradiction.

## Task 2: Fine-Tuning Sentence-BERT

For Task 2, we took the model trained in Task 1 and fine-tuned it specifically for the NLI task using Sentence-BERT. The pre-trained model was further optimized and adapted to better handle sentence embeddings and improve performance for the given NLI classification task.

## Task 3: Evaluation and Results

In Task 3, we evaluated the model using a classification report on the test data. The following table summarizes the performance of the model:

### Classification Report

| Class         | Precision | Recall | F1-Score | Support |
|---------------|-----------|--------|----------|---------|
| Entailment    | 0.00      | 0.00   | 0.00     | 3368    |
| Neutral       | 0.00      | 0.00   | 0.00     | 3219    |
| Contradiction | 0.33      | 1.00   | 0.50     | 3237    |
| **Accuracy**  |           |        | **0.33** | 9824    |
| Macro avg     | 0.11      | 0.33   | 0.17     | 9824    |
| Weighted avg  | 0.11      | 0.33   | 0.16     | 9824    |

**Accuracy**: 0.3295  
**Precision**: 0.1086  
**Recall**: 0.3295  
**F1-Score**: 0.1633

### Analysis

The classification report shows that the model struggles with classifying the "entailment" and "neutral" labels, as both have zero precision, recall, and F1 scores, indicating poor performance on these classes. It performs well on "contradiction" with a perfect recall (1.00) but low precision (0.33), resulting in a low F1 score of 0.50. Overall, the model's accuracy is 32.95%, with poor performance on the minority classes, as seen in the macro and weighted averages. This suggests the need for improvements, such as addressing class imbalance and optimizing the model further.

## Limitations and Challenges

The Sentence-BERT model for NLI tasks faces challenges such as class imbalance, limited dataset size, and high computational costs. Performance can also be sensitive to hyperparameters, and overfitting is a risk with small datasets. To improve, techniques like class balancing, using larger datasets, leveraging pre-trained models, and hyperparameter tuning can enhance results. Regularization methods, advanced architectures like RoBERTa, and data augmentation can help with generalization, while using additional metrics like MCC can better assess performance. Utilizing cloud-based GPUs and conducting error analysis will optimize training and refine the model.

