# Information-Retrieval
Information Retrieval Projects
# Project Subject & Objectives 

**Subject**

> Implementation of the BSB Indexer for an IR system

**Objective**:

> The objective of this homework is to implement an indexer for an information retrieval system in Python. You will be required to implement four classes, including `Index`, `Documents`, `Lexicon`, and `CollectionStatistics`. The implementation of `Index` class will use the **Block Sort-Based Indexing** algorithm to create an inverted index for a given collection with collection path. The resulting index will then be stored in an index file path given as input. The implementation will also include methods for loading and storing all of the classes, `Documents`, `Lexicon`, and `CollectionStatistics`.

> I used **Dataset** for this project is **Milliyet100K** in Turkish language and the neccessary code cells that load the dataset is given below under the topic "DATASET".

DATASET
MilliyetCollection100K.zip

This is the collection we used for the test of your implementation.

It contains 100K documents, and apprx. it has apprx. 25 million tokens, i.e. 95.5/4.

Load Milliyet collection 100K & extract
File ID for gdown
1-X0kWT2NCc4VOI0v1ErkWWbFq9oIJtgs

Code:

!pip install gdown
import gdown
import zipfile

url = 'https://drive.google.com/uc?id=1-X0kWT2NCc4VOI0v1ErkWWbFq9oIJtgs'
output = 'Milliyet100K.zip'
gdown.download(url, output, quiet=False)

with zipfile.ZipFile(output, 'r') as zip_ref:
    zip_ref.extractall('Milliyet100K')
    
!gdown 1-X0kWT2NCc4VOI0v1ErkWWbFq9oIJtgs
!unzip /content/MilliyetCollection100k.zip -d /content

## To Install Zstandard library
The files in the collection directory is compressed using the **Zstandard** compression algorithm.

!pip install zstandard



