# Model-Choose GraphRAG API

A powerful API service that combines RAG (Retrieval-Augmented Generation), Knowledge Graph, and Model Selection capabilities.

## Features

- **📚 Multi-Document Support**: Process various document formats including PDF, DOCX, TXT, CSV, and more
- **🔍 Advanced OCR**: Extract text from scanned documents and images
- **🌐 Knowledge Graph**: Build and utilize knowledge graphs from documents
- **🤖 Model Selection**: Choose from different LLM and embedding models
- **🏢 Multi-Company Support**: Manage multiple separate knowledge bases
- **🔄 Hybrid Retrieval**: Combine vector search and knowledge graph for better results
- **📊 Visualizations**: Generate visual representations of knowledge graphs
- **🔄 Background Processing**: Asynchronous document ingestion and graph building

## API Endpoints

### Root
- `GET /`: Welcome message

### Company Management
- `GET /companies`: List all companies
- `GET /companies/active`: Get the active company
- `POST /companies`: Create a new company
- `PUT /companies/{company_id}/active`: Set a company as active
- `PUT /companies/{company_id}/models`: Update company models
- `DELETE /companies/{company_id}`: Delete a company

### Model Management
- `GET /models/llm`: List available LLM models
- `GET /models/embeddings`: List available embedding models
- `GET /settings`: Get system settings
- `PUT /settings`: Update system settings

### Document Ingestion
- `POST /ingest/upload`: Upload files for ingestion
- `POST /ingest/process`: Process uploaded files (background task)
- `GET /ingest/status/{task_id}`: Check ingestion task status

### Knowledge Graph
- `POST /graph/build`: Build knowledge graph from vector store
- `GET /graph/visualize`: Visualize knowledge graph

### Query Endpoints
- `POST /query`: Query the RAG system with various options

### Utility Endpoints
- `GET /uploads/{filename}`: Retrieve an uploaded file
- `GET /visualizations/{filename}`: Retrieve a visualization file