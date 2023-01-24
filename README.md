#### information-retrieval

# **Search Engine Design and Implementation**

## **About the Project**

As part of our practical coursework of our module Information Retrieval, teams of 3s were asked to build a search engine. The design stage of the proposed 
search engine is contained in 'Group62_PresentationSlides_assignment3.pdf', which includes:
* a general architecture of the search engine, showing its components/modules, and how they relate to each others
* which retrieval model(s) we will be using
* the tool(s) we will be using to build the search engine
* who in our group will be responsible for what
* the time plan for the building of the search engine
* any scenario that we willbe investigating (a particular type of retrieval, using a particular type of documents, etc.)

## **Overview of Experiment**
The experimental search engine uses BM25F model to improve retrieval results of regulatory text.

**Why BM25F?**
BM25, considered one of the most effective retrieval models, considers texts as unstructured, undifferentiated in any way. As an extension of this model, 
BM25F considers documents to be composed of several fields (title, abstract, body, etc.) with possibly different degrees of importance, term relevance 
saturation and length normalisation. 

**Why regulatory texts?**
Regulatory texts tend to have consistent structure and unique approach to topic inclusion - highly relevant concepts are mentioned in opening sections, 
often without repetition in the body. Therefore, some fields may be more predictive of relevance than others. 

**Goal**
By computing and assigning relative weights to pre-specified fields of the documents, the goal is to improve upon the retrieval results of the benchmark
model BM25. 

**Evaluation**
Performance is measured using mean average precision and recall. 

**Overview of Architecture**

<img width="1237" alt="Screenshot 2023-01-24 at 19 24 51" src="https://user-images.githubusercontent.com/118363955/214388940-2c9b2c04-b5a3-42d8-9bd0-ba972496877b.png">

**Tools Used:**

Python was used to implement the search engine components. The libraries that were utilised to scape and prepare the data, implement the search engine and 
run experiments with results are listed below:
* **Beautiful Soup**: used to scrape HTML from the web containing the relevant documents
* **Requests**: used to apply HTTP request and get URLs desired for the dataset
* **Pickle**: used to move data
* **Pandas**: used to read csv file and transform it to a data frame
* **PyTerrier**: used to **index data, apply the retrieval models, tune the parameters (field weights) for the BM25F model and run experiments**.
