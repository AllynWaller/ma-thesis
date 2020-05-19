# ma-thesis
A collection of code and data from my Master's Thesis at Tufts University in the Digital Tools for Premodern Studies program

The code is in several Jupyter Python notebooks.

generate_citation_list takes a folder of documents in XML format, strips everything but the text and the labels, and produces a .tsv file with the passage identifier and the text. 

citations_to_labels takes that .tsv and assigns labels based on author and work. (Currently set up to distinguish historiography from anything else.) It produces a .txt file (another tsv file, but saved as .txt because it's easier to open in a variety of editors). This contains the same identifiers and text, but with a binary label added in a third column. 

random_labels takes the same list of citations as citations_to_labels, but assigns random labels to each section of text. This is used for comparison to the correctly labeled data. 

cross_validation_predictions uses that labelled data and trains a logistic regression model on it in a few different ways. It uses SciKit-Learn's implementation of logistic regression for most of the heavy lifting. Importantly, this notebook produces a list of passages whose algorithmic classification does not align with the classification of the whole book. 

length_counter produces a variety of statistics on the results of cross_validation_predictions, primarily different measures of accuracy. It enables comparison between works of different sizes by giving absolute and relative error rates. 
