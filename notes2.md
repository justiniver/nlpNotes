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

