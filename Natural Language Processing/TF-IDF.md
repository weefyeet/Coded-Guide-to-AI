**Brief Linguistic Context** <br>
In human language, words in a sentence can be classified into parts of speech that define the syntactic function of words, similar to how keywords in programming languages have pre-defined purposes that contribute to syntax rules (hence the term programming *languages*). These parts of speech are used in conjunction with each other, filling specific roles in a sentence such as subject, object, and verb. While parts of speech like nouns, verbs, and adjectives are typically most important in filling these core syntactic roles, other common words are used to add specific contenxt or nuance to the simple trio of subject, object, and verb. 

Let's take the *Harry Potter* series as an example. Of the top ten most common words by frequency, the only nouns, verbs, and adjectives present are "Harry" and "said." The rest are "the", "and", "to", "of", "a", "he", "was", and "his". Most of these words are not contextually essential but will top word frequency lists. Using non-contextual frequency tokenization methods like bag-of-words will not yield meaningful information. 

**TD-IDF** <br>
The Harry Potter series consists of seven books. Let's say that we wanted to determine which characters are principly significant to specific books; that is, the characters that are more restricted to certain books rather than the whole series like protagonist Harry Potter for instance. In that case, the TF-IDF (term frequency - inverse document frequency) can be employed. 

Term frequency simply measures the frequency of a word in a document; it is calculated by: 
- the ratio of the number of occurrences of a word in a document : the total words in the document

Inverse document frequency measures the 
