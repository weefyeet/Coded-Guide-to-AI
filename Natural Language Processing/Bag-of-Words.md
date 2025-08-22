In a colletive body of word sequences (known as a corpus) with n unique words, each unique word in the corpus can be represented as a vector dimension aggregating to an n-unique dimension vector space. Each sequence can then be represented in terms of these word dimensions, with value indicating word frequency across the corpus, with no other information retained. For instance, examine the following sequences:

Group A
- "these are cats"
- "these are dogs"
- "cats are not dogs"

Each sentence can first be broken down into smaller units known as "tokens." Each tokenization can also be represented as vector spaces. 

- "these are cats" --> ["these", "are", "cats"] --> [1, 1, 1]
- "these are dogs" --> ["these", "are", "dogs"] --> [1, 1, 1]
- "cats are not dogs" --> ["cats", "are", "not", "dogs"] --> [1, 1, 1, 1]


The unique terms of the three sentence corpus are thus the five dimensional vector space represented by ["these", "are", "cats", "dogs", "not"]. With two occurrences of tokens "these," "cats," "are," "dogs," and one occurrence of token "are," the values for the vector space of Group A can be represented accordingly as [2, 2, 2, 2, 1]. 

The loss of context and order in the vector space lends its nature to the name "bag-of-words" model, where ordered sentences wtih context are jumbled into the unordered space. 

