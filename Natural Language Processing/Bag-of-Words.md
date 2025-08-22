**BAG OF WORDS** <br>
In a collective body of word sequences (known as a corpus) with n unique words, each unique word in the corpus can be represented as a vector dimension aggregating to an n-unique dimension vector space. Each sequence can then be represented in terms of these word dimensions, with value indicating word frequency across the corpus, with no other information retained. For instance, examine the following sequences:

Group A
- "these are cats"
- "these are dogs"
- "cats are not dogs"

Each sentence can first be broken down into smaller units known as "tokens." Each tokenization can also be represented as vector spaces. 

- "these are cats" --> ["these", "are", "cats"] --> [1, 1, 1]
- "these are dogs" --> ["these", "are", "dogs"] --> [1, 1, 1]
- "cats are not dogs" --> ["cats", "are", "not", "dogs"] --> [1, 1, 1, 1]


The unique terms of the three sentence corpus are thus the five-dimensional vector space represented by ["these", "are", "cats", "dogs", "not"]. With two occurrences of tokens "these", "cats", "are", "dogs", and one occurrence of token "not", the values for the vector space of Group A can be represented accordingly as [2, 2, 2, 2, 1]. Each individual sentence in terms of the corpus vector space will have the following numerical vectors:

- "these are cats" --> [1, 1, 1, 0, 0]
- "these are dogs" --> [1, 1, 0, 1, 0]
- "cats are not dogs" --> [0, 1, 1, 1, 1]

The loss of context and order in the vector space lends its nature to the name "bag-of-words" model, where ordered sentences with context are jumbled into the unordered space. 

**BAG OF N GRAMS** <br>
When the occurrence of particular strings of tokens is important, complete tokenization into the standard bag-of-words model cannot capture the frequency due to loss of order, and thus any context associated with repeated phrases is also lost. However, modifications of the bag-of-words model can address these issues by considering entire phrases as tokens. These extensions can be classified by phrase size as a "bag of n-grams" model, where n denotes the token length of phrases. Note that phrases are defined as consecutive, ordered sequences of tokens, which means context is preserved within the n-grams. Let's use Group A as an example once more:

- Unigram: n = 1 (phrase of token length n = 1)
- Bigram: n = 2 
- Trigram: n = 3 and so on

Starting with phrases of size n = 2, each sentence in Group A can be broken down into bigrams:
- "these are cats" --> ["these are", "are cats"] --> [1, 1]
- "these are dogs" --> ["these are", "are dogs"] --> [1, 1]
- "cats are not dogs" --> ["cats are", "are not", "not dogs"] --> [1, 1, 1]

The corpus vector space of bigrams is represented by the six-dimensional vector space ["these are", "are cats", "are dogs", "cats are", "are not", "not dogs"]. Note that token order in each bigram is preserved, resulting in bigrams like "cats are" and "are cats" being considered unique despite having equivalent vectors in the bag-of-words model. Consider each sentence in Group A in terms of the corpus bigram vector space:

- "these are cats" --> [1, 1, 0, 0, 0 , 0]
- "these are dogs" --> [1, 0, 1, 0, 0, 0]
- "cats are not dogs" --> [0, 0, 0, 1, 1, 1]

The sum of the vectors is [2, 1, 1, 1, 1, 1]. Compared to the unigram vector [2, 2, 2, 2, 1], the bigram vector provides additional information about the specific repeated phrase "these are" that cannot otherwise be ascertained from the unigram vector. At unigram level context and order are lost, and at higher n, analysis can become quite expensive computationally, but n-grams of reasonably small n are highly useful in efficiently analyzing context through the frequency of ordered phrases. 



