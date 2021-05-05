1. Creating embedding vectors from BERT using transfer learning and feeding that embedding vectors to a Neural Network for classification.
2. like how we used glove w2v in the same way we are getting embedding from bert from Tensorflow HUB.
3. BERT(Bidirectional Encoder Representation from Transformers) trie to understand the underlining of any language
4. One trickier part was data preprocessing followed by Tokenization before getting embedding from BERT, like this model of bert was needed 3 inputs i) Sequence of words represented as integers ii)mask vector if we are padding anything iii)segment vectors. If we are giving only one sentence for the classification, total seg vector is 0
