# AI Record Manager & Vector Database Sync Workflow

This workflow is designed to synchronize external content with a vector database (Pinecone) while maintaining a record manager in MySQL. It fetches data from APIs, processes each item, and generates a unique hash to detect whether a record is new, updated, or unchanged. Based on this, it decides whether to create, update, or skip records—ensuring efficient data handling without duplication.

It also handles deletion logic, comparing API data with stored database records to identify removed items. If a record no longer exists in the source, it deletes both the database entry and its corresponding vector from Pinecone. This keeps the system clean and fully in sync with the source of truth.

Additionally, the workflow prepares content for AI use cases by splitting text into chunks, generating embeddings, and storing them in Pinecone for retrieval (RAG systems). It also supports file uploads (like PDFs) for embedding, making it a complete pipeline for managing, updating, and querying AI-ready data.
