


# Llama-Mistral-PDF-QA

Llama-Mistral-PDF-QA is a project designed to create a robust Question & Answer assistant that processes and analyzes PDF files. The system uses state-of-the-art technologies, including:

- **LlamaIndex**: For efficient indexing and retrieval.
- **Hugging Face Models**: To power natural language understanding and generation.
- **Sentence Transformers**: For high-quality embeddings and semantic search.

## Features
- Load and parse PDF documents into a queryable format.
- Provide precise answers to user questions based on PDF content.
- Supports advanced LLMs like Mistral-7B for customizable responses.

## Setup Instructions

### Prerequisites
Ensure you have the following installed:
- Python 3.8 or higher
- CUDA-compatible GPU (optional, for faster processing)

### Installation
1. Clone the repository:
   ```bash
   git clone 
   cd 
   ```
2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

### Hugging Face Authentication
Log in to Hugging Face to access the required models:
```bash
huggingface-cli login
```

### Directory Setup
Create a folder named `Data` and place your PDF files inside:
```bash
mkdir Data
```

### Running the Project
1. Load the PDF documents:
   ```python
   from llama_index import SimpleDirectoryReader
   documents = SimpleDirectoryReader("./Data/").load_data()
   ```
2. Build the index and query engine:
   ```python
   index = VectorStoreIndex.from_documents(documents, service_context=service_context)
   query_engine = index.as_query_engine()
   ```
3. Query your documents:
   ```python
   response = query_engine.query("What is the PDF about?")
   print(response)
   ```

## Contributing
Feel free to submit issues and pull requests to enhance the functionality.

## License
This project is licensed under the MIT License.
```


