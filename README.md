# OCRDocumentClassifier
This dataset represents the output of the OCR stage of the data pipeline. The word order for the dataset comes directly from the OCR layer. Trained a document classification model using Random forest, Linear SVC and Sequential NN using TF-IDF Features

The given CSV file contains raw OCR data read from PDF soft copies. The document consists of a document type in the first column and followed by hashed OCR delimited by space. Each hashed word is assigned to a unique word and it is assumed that they are all ordered. A sample line looks like below:

CANCELLATION NOTICE,641356219cbc f95d0bea231b ... [lots more words] ... 52102c70348d b32153b8b30c


1.Trained a document classification model.
2. Deployed my model to a public cloud platform (AWS) as a webservice.

Accuracies of the experimented algorithms:

1. Linear SVC: 0.816023166023166
2. Logistic Regression: 0.7010939510939511
3. Seq Neural Network : 0.8566

Chose the best performing to model to create a RESTful API using Flask and also created a UI template for real time document analysis.

Webservice spec:

-RESTful API
-Respect content-type header (application/json and text/html minimum other bonus)
-Discoverable from root path
-URL encoded GET parameter "words" returns predicted document type (confidence is a bonus) in field "prediction" and "confidence"
-HTML pages should be readable by a human and allow for action, aka input field and submit buttons etc.



