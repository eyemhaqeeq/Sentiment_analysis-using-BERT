
BERT Sentiment Analysis on Amazon Reviews

This project demonstrates fine-tuning of the BERT (bert-base-uncased) model for binary sentiment classification using the Amazon Fine Food Reviews dataset. The implementation leverages the Hugging Face Transformers library with PyTorch and is optimized to run efficiently on Google Colab GPU.

Model Summary

Model: BERT (bert-base-uncased)
Task: Binary Sentiment Classification (Positive vs Negative)
Dataset: Amazon Fine Food Reviews (Kaggle)
Sample Size Used: 5000 reviews
Max Sequence Length: 128 tokens
Training Epochs: 2
Batch Size: 16 (train), 64 (eval)
Tokenizer: BertTokenizer from Hugging Face

Libraries Used

transformers
scikit-learn
pandas
torch
Google Colab (with GPU)

Evaluation Results

Accuracy: 0.9375
Precision: 0.9507
Recall: 0.9740
F1 Score: 0.9622
Training Time: 144.22 seconds
Testing Time: 5.10 seconds

Workflow

1. Load the Amazon Fine Food Reviews dataset.
2. Remove neutral reviews (Score == 3).
3. Map scores to binary labels: 0 for negative, 1 for positive.
4. Tokenize using BERT tokenizer with max_length = 128.
5. Create a PyTorch Dataset compatible with Hugging Face Trainer.
6. Fine-tune BertForSequenceClassification.
7. Evaluate using scikit-learn metrics.

File Structure

- BERT_Sentiment_Analysis.ipynb: Jupyter notebook with training and evaluation steps.
- Reviews.csv: Dataset file.
- README.md: Project documentation and summary.

Future Work

- Compare BERT with RoBERTa and DistilBERT.
- Add explainability using SHAP or LIME.
- Explore robustness to noisy text input and zero-shot classification.

License

This project is licensed under the MIT License.

MIT License

Copyright (c) 2025 Haqeeq Ahmed

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
