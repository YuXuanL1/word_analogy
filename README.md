# word_analogy
Anthology helps to assess how well the word embedding model captures semantic
and syntactic relationships between words
## dataset
[Google Word Analogy](https://arxiv.org/pdf/1301.3781)
- 19,544 entries
  - 5 sub-categories for semantic relationships
  - 9 sub-categories for syntactic relationships
- Each entry: four words, separated by a space. (e.g. A B C D)
- Task: A is to B in the same sense that C is to ?
  - The forth word (D) in each entry is the answer.

![螢幕擷取畫面 2025-03-26 231132](https://github.com/user-attachments/assets/d46aa90f-e2d3-4246-90dc-0b99ffa3808d)

## model
- pretrained model (gensim "glove-wiki-gigaword-100")
- model_1：Word2Vec (with preprocessing) (20% training data)
- model_2：Word2Vec (without preprocessing) (20% training data)
- model_3：Word2Vec (without preprocessing) (30% training data)

## pre-processing steps
- 分詞：使用NLTK套件的word_tokenize 
- 移除stop words：使用NLTK套件的english stopwords
- Lemmatization (詞形還原)：使用NLTK套件的WordNetLemmatizer

## performaces
![螢幕擷取畫面 2025-03-26 231511](https://github.com/user-attachments/assets/c5bd64f3-0e07-4620-ac96-1561d459144d)

![螢幕擷取畫面 2025-03-26 231704](https://github.com/user-attachments/assets/5871001e-0c8e-4962-9ea8-f6efe2ad694f)

## for more complete analysis
[report](https://github.com/user-attachments/files/19469857/NLP_HW1_NCCU_110306085.docx)
