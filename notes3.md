### More n-gram Stuff
- For unigram
    - P(A, B, C) = P(A) * P(B) * P(C)
    - Ignore 'start-of-sequence' token so that P(s, A, B) = P(A, B)
- To create a good **n-gram language model**, we need to:
  - **train**
    - learn the things to predict next token
  - **score**
    - create an evaluation system
  - **generate**
    - sample or decode tokens based on learned probabilities
- **Evaluation**
    - **Intrinsic**: Measures model performance on its core task directly (e.g., perplexity for language models)
    - **Extrinsic**: Measures model performance as part of a real-world application (e.g., impact on machine translation)
- **Perplexity** is used as a measure of "surprise"
  - If perplexity of a language model is higher it means less likely to have generated the sequence (and vice versa)
- PP(W) = (# of char appearance/# of tokens)*(-1/N)

### Precision and Recall
- Precision = tp / (tp + fp)
- Recall = tp / (tp + fn)
