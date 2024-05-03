---

# RAG (Retrieval-Augmented Generation)

RAG is a Python package designed to facilitate information retrieval and generation tasks, particularly in natural language processing applications. With RAG, users can input a PDF file along with a Hugging Face model, enabling the extraction of relevant data from the PDF and responding to user queries based on the extracted information.

## Features

- **PDF Parsing**: RAG can parse PDF files to extract textual information.
- **Information Retrieval**: Using Hugging Face models, RAG retrieves relevant data from the parsed PDF.
- **Query Response**: Users can ask questions or input queries, and RAG will provide responses based on the extracted information.

## Installation

To install RAG, clone the repository and install the required dependencies:

```bash
pip install git+https://github.com/SayedShaun/pyrag.git
```

## Usage

Using RAG is straightforward. Here's a basic example of how to use it:

```python
from rag import RAG

# Initialize and Provide a PDF file and Hugging Face model
rag = RAG(
    model_id="meta-llama/Meta-Llama-3-8B-Instruct",
    embedding_model="sentence-transformers/all-mpnet-base-v2",
    hf_token="your huggingface token",
    pdf_path="/kaggle/input/sample-resume/donna robbins.pdf"
)

# Retrieve data from the PDF
rag.retrieve_answer("what skills she has?")

# Response
"""
Donna Robbins has skills in Microsoft NAV Dynamics,
Cashflow planning & management, State & federal tax codes,
Bookkeeping, Exceptional communication, and Fluent in German.
"""
```

## Contributing

We welcome contributions from the community to enhance RAG's functionality, improve its performance, or fix any issues. To contribute, please follow these steps:

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---