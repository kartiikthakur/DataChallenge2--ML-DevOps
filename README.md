# OCRDocumentClassifier
This dataset represents the output of the OCR stage of the data pipeline. The word order for the dataset comes directly from the OCR layer. Trained a document classification model using Random forest, Linear SVC and Sequential NN using TF-IDF Features

The given CSV file contains raw OCR data read from PDF soft copies. The document consists of a document type in the first column and followed by hashed OCR delimited by space. Each hashed word is assigned to a unique word and it is assumed that they are all ordered. A sample line looks like below:

CANCELLATION NOTICE,641356219cbc f95d0bea231b ... [lots more words] ... 52102c70348d b32153b8b30c



