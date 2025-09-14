### LLMs
- LLMs works through classification
- Using a word bank (typically 40k ~ 60k words), predicts the next word
- Models have billions of 'parameters' (more on that later)

### Text Normalization and Tokenization
- Stems and affixes (e.g., 'cats' where 'cat' is the stem and 's' is the affix)
- We need to correct misspellings
- **Problematic Words Examples**
  - **Possession**: Finland's capital = Finland + 's + capital = 3 tokens
  - **Contraction**: (it's = it + is) **OR** (it's = it + has)
  - **Hyphenated terms**: Hewlett-Packard, state-of-the-art
  - **Words with variants**: lowercase, lower case, lower-case
- Tokenizing words in languages that do not use whitespace (e.g., Chinese, Japanese) 
need to use more complex processes to tokenize (max matching algorithm)
- **Lemmatization** is the process of reducing inflections or variant forms to the base form.
  - am, are, is = be
  - bike, bikes, bike's, bikes' = bike
- **Morphology** is the idea that words are build from smaller units (i.e., stems and affixes)
  - Inflectional Affix Examples
    - cat to cats
    - climb to climbed
  - Derivational Affix Examples
    - act to react
    - act to actor
- **Stemming** a faster and dumber solution (compared to lemmatization) where
we just reduce words to their stems
  - Defined as crude affix removal (e.g., strip suffix get base form)
- **Case Folding** is normalizing case (uppercase and lowercase) so that 'The' counts
the same as 'the'

### Semantics
- This is the part of linguistics that deals with meanings, which are called 'senses' in NLP.
- Synonyms map to the same 'sense' such as filbert and hazelnut.
- **More Examples**
  - Water vs H20
  - Couch vs Sofa
  - Hi vs Hello
- The **Linguistic Principle of Contrast** is the idea that even if they are synonyms 
the difference in form means a difference in meaning.