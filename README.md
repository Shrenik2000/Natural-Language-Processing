# CS5803: Natural Language Processing
A brief description of the assignments and project done as part of this course

## Assignments

#### Assignment 1: BLEU Score [Papineni et al., 2002]
- Q1: Implement BLEU Score metric. Pre-process the text by lower-casing the text and removing punctuation.
- Q2: Use this implementation to find BLEU Score when x = ”The boys were playing happily on the ground.” and y = ”The boys were playing football on the field.”.
- Q3: Can you explain why we are taking minimum in the numerator in the equation of BLEU Score.
- Q4: Use your implementation to find BLEU Score between any 5 sentence pairs and explain what are potential disadvantages of using the BLEU Score.

#### Assignment 2: Language Modelling
In this question, we’ll use n-gram probabilities for Language modelling. Download the pre-processed dataset from https://www.kaggle.com/datasets/moxxis/harry-potter-lstm. You can use the first 10,000 words for this question.
- Q1: Preprocess and tokenize the dataset using NLTK.
- Q2: Refer NLTK documentation and fit two bigram language models on the text: MLE and Kneser-Ney discounting.
- Q3: Use the beginning words 1. ”Harry Potter” and 2. ”Dumbledore” to generate text using both the language models. Keep the maximum text length as 20.

The above language modelling approaches are greedy approaches (the predicted next word is the word with highest conditional probability). But it is possible that this greedy decoding may be sub- optimal. Hence better decoding strategies have been proposed in literature. One popular decoding strategy is beam search. Beam search is a tree-based search strategy similar to BFS. In BFS, we expand every child node, however in Beam search, we expand only top k most probable children. The generated text is the text with the highest probability.

- Q4: To Implement Beam Search, you would have to find the top k most probable words given some context. Implement a function for this. Hint: You may use the lm.vocab variable to your advantage.
- Q5: Implement Beam search. Use the MLE Language model trained previously.
- Q6: Repeat part 3 using Beam Search with k=2 and depth=10. Find the 5 generated texts with highest probability for each of the 2 beginning phrases.

Note that you can calculate probability of generated text while doing beam search itself.


## Course Project

#### Title: Simplification of Legal Documents
#### Abstract: 
Comprehending legal documents is often made difficult by the complexity of language used. Therefore, we propose a
new model called SUSI (Summarization, Simplification) to make
it easier for people to understand such materials. In contrast with
other methods, SUSI combines the power of summarization with
simplification strategies that can effectively distil complex legal
jargon. Readability and comprehension are optimized through
the use of a pre-trained Legal Pegasus model for summarization
and BART model for simplification by SUSI. We assess its
performance on MILDSum dataset using evaluation metrics like
GFI index, ROUGE-1, ROUGE-2, ROUGE-L and BertScore.
The outcome shows that our BART-based SUSI model performs
better than other models thereby signifying great strides towards
simplifying legal documents.
