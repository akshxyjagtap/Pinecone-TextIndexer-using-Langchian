# Data Embedding and Pinecone Indexing


Ingestion.py is a Python program that facilitates the ingestion of text data, generates embeddings using OpenAI, and indexes these embeddings in Pinecone for fast and efficient retrieval. This README provides an overview of the program, installation instructions, usage guidelines, and configuration options.

## Overview

Ingestion.py automates the process of transforming text data into semantic embeddings and indexing them in Pinecone, a high-performance vector database. This enables seamless and efficient semantic search over your text data, making it ideal for applications like recommendation systems, content retrieval, and more.

## Usage

### Install Dependencies

Before using Ingestion.py, make sure you have the necessary dependencies installed. You can install them using pip:

```shell
pip install langchain pinecone python-dotenv
````


## Setting Environment Variables

Before you can use Ingestion.py, you need to set the following environment variables:

- **OPENAI_API_KEY**: Your OpenAI API key, which is required for certain functionality in the script. You can obtain this key by signing up for an OpenAI account.

- **PINECONE_API_KEY**: Your Pinecone API key, used to authenticate with Pinecone's services. You can obtain this key by creating a Pinecone account.

- **PINECONE_ENVIRONMENT_REGION**: The region where your Pinecone environment is hosted (e.g., "us-west1" or "eu-west-1"). Make sure it matches the region of your Pinecone environment.

To set these environment variables, you can add them to your system's environment variables or include them in a `.env` file in the project directory. Here's an example of a `.env` file:

```plaintext
OPENAI_API_KEY=your-openai-api-key
PINECONE_API_KEY=your-pinecone-api-key
PINECONE_ENVIRONMENT_REGION=your-pinecone-environment-region
```



Run Ingestion.py
To start the ingestion process, simply run the Ingestion.py script:

```shell
python ingestion.py
```
## The program will perform the following steps:

- **Load text data using the ReadTheDocsLoader:**
Split the text into chunks using the RecursiveCharacterTextSplitter.
Generate OpenAI embeddings for each chunk.
Index the embeddings in Pinecone for fast retrieval.
## Configuration
You can configure various aspects of the ingestion process by modifying the provided configuration options in the config.yml file. The following parameters are available for customization:

- TEXT_DATA_URL: URL of the text data source to ingest.
- EMBEDDING_MODEL: The OpenAI embedding model to use.
- CHUNK_SIZE: The size of text chunks to generate embeddings from.
- CHUNK_OVERLAP: The overlap between consecutive text chunks.
- PINECONE_INDEX_NAME: The name of the Pinecone index to create for storage.
By adjusting these parameters, you can fine-tune the ingestion process to suit your specific use case.

## How it Works
Ingestion.py operates as follows:

- ReadTheDocsLoader: Loads text data from the specified URL.
- RecursiveCharacterTextSplitter: Splits the text into overlapping chunks for embedding generation.
- OpenAIEmbeddings: Generates a vector embedding for each text chunk using the chosen OpenAI model.
- A Pinecone index is created with the specified name.

The embeddings and associated metadata are inserted into the Pinecone index.
This workflow enables fast and efficient semantic search over the ingested text data using Pinecone's vector similarity search capabilities.









































