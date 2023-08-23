# DistilBert Text Classification  
### Steps
1- Use GPU on google colab or Cloud to imporve your computation power<br/>
2- install trnasformers<br/>
3-import dependencies<br/>
4-define path and import the csv file<br/>
5-Create some EDA  (Category value counts, word count frequency)<br/>
6-Encode Categories for training<br/>
7- create dictionary of encoded cat as key and categories as value to use to decode the encoded categories<br/>
8-Split data to training and testing ,split the training to training and validation <br/>
9-Use the distilbert tokenizer to encode the training and testing datasets<br/>
10-convert training and testing data to tf.data.dataset to be easily used in distilbert model<br/>
11-Use the distilbert model and set the num_labels to 5 as we have 5 classes<br/>
12-Set loss function to sparsecategoricalcrossentropy as we have our labels as integer not hotencoded<br/>
13-Set the optimizer to Adam and set the learning rate to 5e-5<br/>
14-compile the model using our loss function,optimizer and set the metrics to accuracy<br/>
15-fit the model on training dataset which has shuffle buffer =100 and divided into 16 batch for two epochs<br/>
16-evaluate the model using the test set with the same format of the traning set as tf.data.dataset<br/>
17-save the model on your directory and the tokenizer to be resued later <br/>
18- load the model and tokenizer from the saved directory<br/>
19-Enter your text which you want to predict on , encode it using our loaded tokenizer and apply padding and truncation and return tensors as tf tensors<br/>
20-The output will be the logits prob of each class then use the argmax function to return the index that got the highest value ,finally decode the encoded_class and return the class<br/>
21-use classify function to predict on a text from the val set or any news and our model will assign it to the most fitted class<br/>


