### LLMs (part 2)
- Uses a lot of parameters (e.g., semantics, syntax)


### Counting words
- **type**: an entry in a vocabulary (or lexicon)
  - words, punctuation, disfluencies (filler words), fragments, etc...
- **vocabulary**: the set of types that we'll be working with for the given application
  - {I, like, run, to, car, ...}
- **token**: an instance of some type in some text
- For example:
  - "The cat chased the dog over the fence." 
    - 9 tokens and 7 types {the, cat, chased, dog, over, fence, .}
- **Corpus**: collection of real world text or speech data
- Types can be denoted as **|V|** (i.e., the size of vocabulary == number of types).
- Heap's Law states that **|V|** = kN^(beta) where k ~ 0.7
  - So, the vocab size for a given text goes up significantly faster than sqrt(N)

### Probability
- **n-gram**: means sequence of length n
- P(hard | the homework was) = count('the homework was hard') / count('the homework was')
- **|V|**: represents the size of the vocabulary
- **Laplace Smoothing**: Add one to numerator and add |V| to denominator
- **prefix**: all previous words in the sequence
- We can model word prediction as assessing conditional 
probability of a word given the prefix 
- We can calculate these types of probabilities from counts in a large corpus
- A bigram language model just means n = 2
- The chain rule for probabilities looks like 
P(A, B, C, D) = P(A) * P(B | A) * P(C | A, B) * P(D | A, B, C)
- Example of bigram probabilities. This is our training data with 14 tokens and 10 vocabulary size:
  - I am Sam
  - Sam I am
  - I do not like green eggs and ham
    - P('I', 'am', 'Sam') = P('I') * P('am' | 'I') * P('Sam' | 'am')
