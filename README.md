# GitHub MCP Agent

This repository currently contains a Python retrieval demo for finding relevant passages in sample company policies.

## What the code does

`Complete_RAG_Pipeline.py`, titled **TechCorp PolicyCopilot** in its source, demonstrates:

1. Splitting five embedded policy documents into overlapping chunks.
2. Adding the chunks and metadata to an in-memory Chroma collection.
3. Embedding a question with Sentence Transformers and retrieving three matching chunks.
4. Building a prompt from the retrieved context.
5. Returning a fixed, simulated answer.

The answer-generation function does not call a language-model service.

## Getting started

Requires Python 3 and compatible installations of ChromaDB, Sentence Transformers, LangChain, and NumPy. The repository has no dependency manifest or pinned versions; its `langchain.text_splitter` import needs a compatible LangChain release. Model downloads may require network access on first use.

Once the dependencies are available, run:

```bash
python3 Complete_RAG_Pipeline.py
```

The script runs five built-in policy questions and pauses for Enter between demonstrations. Edit `test_queries` to try another question, or `policy_documents` to change the sample material. There is no external policy dataset or API key configuration.

## Status and limits

This is a standalone learning demo. GitHub access, Model Context Protocol integration, and a web interface are not implemented. Retrieval is real code; final answer generation is simulated and does not use the prompt contents. The default Chroma client does not configure persistent storage.

No tests are included.

## License

No license file is included.
