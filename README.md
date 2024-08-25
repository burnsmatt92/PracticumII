## Handwritten History: Automated Digitization and Transcription of Historical Documents
### MSDS696 – Data Science Practicum II
The goal for this project was to see if I could build an effective optical character recognition model to offer the Windsor Art & Heritage Center of Colorado for their large collection of historical city documents. I went with Tensorflow and Keras as they were ranked highest for free models that excel at handwriting OCR. 
With a parternship with The Windsor Art & Heritage Center, I was given hundreds of thousands of pages with no transcription. These books are over a hundred years old and are starting to really show their age and succumb to the elements so the clock is ticking. I wanted to see how well we can leverage deep learning to ensure history is not lost. While I didn't quite get there over the course of the course, I'm continuing my work on it in hopes of delivering a standalone model that be given to museums for transcription.

### Dataset Example
![Example of the images given by Windsor Museum](/images/010.jpg)

### Training
I attempted three different levels of training the model based on epochs.
#### 60 Epochs
60 epochs seems to work decently well, but still missed the mark on several of the testing validation words.

![Graph showing performance of model after 60 epochs](/images/60_Epochs.png)

Below you can see how it handled predicting the words from the training dataset.
![Testing validation words](/images/60_Epochs_Training.png)

And here is how it handled the words from my own dataset.
![Windsor Museum Dataset Performance on 60 epochs](/images/60_Epochs_Results.png)
#### 100 Epochs
100 epochs seemed to perform better, but we are starting to drift in the direction of overfitting.

![Graph showing performance of model after 100 epochs](/images/100_Epochs.png)

Here is how it handled my dataset.
![Windsor Museum Dataset Performance on 100 epochs](/images/100_Epochs_Results.png)

Some better and some worse.
#### 200 Epochs
Finally I decided to try 200 epochs, and while it is demonstrating some overfitting, especially in the performance graph, I do find the result overall were better.

![Graph showing performance of model after 200 epochs](/images/200_Epochs.png)

But you can see the results, despite overfitting, below.
![Windsor Museum Dataset Performance on 200 epochs](/images/200_Epoch_Results.png)

## Conclusion
My model wasn’t the most accurate. However a lot of it is readable. I was suprised it worked as well as it did given the legibilty and photo difficulties that arise.

The model was designed for words not sentences or pages. More work needs to be done to scale up to handle the thousands of pages the museum has.

I Didn’t accomplish my goal of transcribing all of Windsor’s documents. However, I did get an excellent experience in deep learning that I will continue to lean on.

I’m not finished with this project. I’m going to continue working on this so that I can help Windsor preserve their history with the digitization of their documents.
