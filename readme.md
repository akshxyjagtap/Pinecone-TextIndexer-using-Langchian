# Data Embedding and Pinecone Indexing

**Ingestion.py** is a Python script designed to create embeddings of data and facilitate the indexing of these embeddings in [Pinecone](https://www.pinecone.io/). Before using the script, you need to set specific environment variables for the OpenAI API key, Pinecone API key, and Pinecone environment region. This README provides an overview of the script and instructions on how to set these environment variables.

## Table of Contents

- [Introduction](#introduction)
- [Setting Environment Variables](#setting-environment-variables)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Ingestion.py simplifies the process of generating embeddings from data and indexing them in Pinecone, a powerful vector database for efficient similarity search. Whether you're building a recommendation system, content retrieval, or any application requiring similarity-based querying, this script can streamline the process.

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
## Features
- Data Embeddings: Ingestion.py can create embeddings from various data sources, including text, images, and more.
- Pinecone Integration: Seamlessly connect to Pinecone to create and manage embeddings in a scalable, high-performance vector database.
- Embedding Customization: Customize embedding generation for your specific use case.
- Scalability: Handle large-scale data and future growth with ease.
- Logging and Monitoring: Monitor the status and performance of embedding generation and indexing.
Efficient Search: Leverage Pinecone's capabilities for fast and accurate similarity search.