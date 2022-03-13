# NLP

Natural Language processing, a sub-field of machine learning has gained immense popularity in the last 5 years in both research and industrial applications due to the advancement in the field of deep learning and improvement in the computational power of hardware systems. It is a technique for computers to understand how human languages work involving the usage of computational linguistics and the computer science domain. In recent years, NLP has found its usage in several applications related to understanding and interpreting text, audio, and video files.

##  Sentiment Analysis

![image](https://user-images.githubusercontent.com/88995459/158042565-ed6282a9-4763-4ab3-bf91-a69e5c9f1f64.png)

One of the key areas where NLP has been predominantly used is Sentiment analysis. The understanding of customer behavior and needs on a company’s products and services is vital for organizations. Generally, the feedback provided by a customer on a product can be categorized into Positive, Negative, and Neutral. Interpreting customer feedback through product reviews helps companies evaluate how satisfied the customers are with their products/services.


### Data Pre-processing

pre-processing  the data before converting it into vectors and passing it to the machine learning model.

1. First, we will iterate through each record, and using a regular expression, we will get rid of any characters apart from alphabets.

2. Then, we will convert the string to lowercase as, the word “Good” is different from the word “good”.
Because, without converting to lowercase, it will cause an issue when we will create vectors of these words, as two different vectors will be created for the same word which we don’t want to.

3. Then we will tokenize the text in to sent tokenizer or word tokenizer as required

4. Then we will check for stopwords in the data and get rid of them. Stopwords are commonly used words in a sentence such as “the”, “an”, “to” etc. which do not add much value.

5. Then, we will perform lemmatization on each word,i.e. change the different forms of a word into a single item called a lemma.
A lemma is a base form of a word. For example, “run”, “running” and “runs” are all forms of the same lexeme, where the “run” is the lemma. Hence, we are converting all occurrences of the same lexeme to their respective lemma.

6. And, then return a corpus of processed data.



## How are words/sentences represented by NLP?

The genius behind NLP is a concept called word embedding. Word embeddings are representations of words as vectors, learned by exploiting vast amounts of text. Each word is mapped to one vector and the vector values are learned in a way that resembles an artificial neural network.
Each word is represented by a real-valued vector with often tens or hundreds of dimensions. Here a word vector is a row of real valued numbers where each number is a dimension of the word’s meaning and where semantically similar words have similar vectors. i.e. Queen and Princess would be closer vectors.
If we label 4 words (King, Queen, Woman, Princess) with some made up dimensions in a hypothetical word vector, it might look a bit like below:

![image](https://user-images.githubusercontent.com/88995459/158042855-54e38ffe-04d0-451b-b2ce-c45b03aa2b70.png)

The numbers in the word vector represent the word’s distributed weight across dimensions. The semantics of the word are embedded across these dimensions of the vector. Another simplified example across 4 dimensions is as below:

![image](https://user-images.githubusercontent.com/88995459/158042871-faf2e25a-fccc-4abc-b349-1b4bd28ee4dc.png)

We can visualize the learned vectors by projecting them down to simplified 2 dimensions as below and it becomes apparent that the vectors capture useful semantic information about words and their relationships to one another.

![image](https://user-images.githubusercontent.com/88995459/158042883-52c4b22f-71f4-491f-ab81-76701a5c5f1c.png)

These are distributional vectors based on the assumption that words appearing within similar context possess similar meaning. For example, in the figure below, all the big cats(i.e. cheetah, jaguar, panther, tiger and leopard) are really close in the vector space.

![image](https://user-images.githubusercontent.com/88995459/158042909-459b091b-3dfa-4462-af65-c22b7275d242.png)

The word embedding algorithm takes as its input from a large corpus of text and produces these vector spaces, typically of several hundred dimensions. A neural language model is trained on a large corpus (body of text) and the output of the network is used to each unique word to be assigned to a corresponding vector. The most popular word embedding algorithms are Google ‘s Word2Vec, Stanford ‘s GloVe or Facebook ‘s FastText.


### Data modelling

1. Creating the Bag of Word Model or Embeddings

2. Splitting into train and test

3. Model building

4. Testing the model
