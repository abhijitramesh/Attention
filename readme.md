# Attention

This is one of the most celebrated applications in the field of deep learning. Basically what attention does is to mimic what our brain does. 
Human Brain does not process a whole visual snapshot of what it sees instead it looks at a particular portion of something and the process it sequentially over time. Applying the same principal to computer vision we can get really good results such as if we use an eye tracking with another camera to see what the eye sees we can represent to the machine how our brain is learning.

# Sequence to Sequence

## Application

As I have mentioned that sequence to sequence is one of the most celebrated applications of deep learning to get a better understanding of what we can do with sequence to sequence lets say we train it with english phrases and its translation to french then we have an english to french translator. Let us say we have train it on text conversation then we have a chat bot or if we train it on images and captions then we have and image captioning model and so on.

## Encoders and Decoders

![download](https://user-images.githubusercontent.com/43090559/84361500-5fba5c80-abe9-11ea-832d-d451e03cab04.png)

In a very basic level Sequence to Sequence model consist of an encoder and a decoder.
The encoder can be a Cnn or an Rnn. It takes in an input and processes the information and passes this tensor of what it understood called the state to the decoder which in-turn would give the output.


![1_1JcHGUU7rFgtXC_mydUA_Q](https://user-images.githubusercontent.com/43090559/84361788-cb9cc500-abe9-11ea-9a81-2a9a80ff2935.jpeg)

If we consider the Encoder and Decoder as both RNN's then we can unfold them to see what is happening in each time-step and naturally they have loops and RNNs feed the output of one node to other till the last state where it gives the output as a tensor to the decoder which again is an RNN with its own network.

### Limitation of Sequence to Sequence model

As we can see above the Encoder Rnn would have a specific length of hidden state in each step but at the end it only sends a single vector to the Decoder. This means that the model is not able to summarize a long sequence with a context vector which has small dimensions. This is what Attention solves.
