# Knowledge Graph

GraphRAG uses indexing prompts to create an knowledge graph.

https://www.microsoft.com/en-us/research/blog/graphrag-auto-tuning-provides-rapid-adaptation-to-new-domains/

> The knowledge graph creation process is called indexing. An LLM, guided by a set of domain-specific prompts, reads all the source content and extracts the relevant information, including entities and relationships, which are then used to construct the graph.

## What is a knowledge graph (entities and relationships)?

A knowledge graph is a knowledge network that systematically connects various knowledge (= knowledge) and represents it in a graph structure. Prior research has been conducted since the 1960s, and in recent years it has been used in various fields as a practical foundational technology for AI.

GraphRAG uses LLMs to build comprehensive knowledge graphs detailing entities and their relationships from any collection of text documents.

By creating a knowledge graph that pre-analyzes the "entities" (people, places, etc.) that appear in a text and their "relationships," questions about them can be answered more accurately.

This graph allows the system to generate responses to complex queries that require a broad understanding of the entire text.

## Indexing prompts

https://www.microsoft.com/en-us/research/blog/graphrag-auto-tuning-provides-rapid-adaptation-to-new-domains/

GraphRAG uses "indexing prompts" to build an index (knowledge graph).

During the indexing process, GraphRAG uses a series of "indexing prompts" to direct the LLM to read the source content, extract and organize relevant information, and build a knowledge graph. There are three main indexing prompts in GraphRAG:

- Entity and relationship extraction: Identify all entities present and establish relationships between them.
- Entity and relationship summarization: Consolidate entity instances and their relationships into one concise description.
- Community report generation: Generate a summary report for each community in the built knowledge graph.

