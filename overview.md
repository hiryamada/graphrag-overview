# GraphRAG Overview

Official site
https://microsoft.github.io/graphrag/

GitHub repository (GraphRAG core library)
https://github.com/microsoft/graphrag

FAQ (GraphRAG: Responsible AI FAQ)
https://github.com/microsoft/graphrag/blob/main/RAI_TRANSPARENCY.md

Microsoft's Project GraphRAG page
https://aka.ms/graphrag

arXiv preprint (pre-peer reviewed paper): From Local to Global: A Graph RAG Approach to Query-Focused Summarization
https://arxiv.org/html/2404.16130v1

## (Before explaining GraphRAG) What is RAG?

Retrieval-Augmented Generation.

Combining external data with a large-scale language model to generate answers that are in line with the external data.

Azure makes it relatively easy to achieve RAG by using "Azure OpenAI on your data".

https://learn.microsoft.com/ja-jp/azure/ai-services/openai/concepts/use-your-data?tabs=ai-search%2Ccopilot

## What is GraphRAG?

https://github.com/microsoft/graphrag/blob/main/RAI_TRANSPARENCY.md#what-is-graphrag

GraphRAG is an AI-based content interpretation and search capability. Using LLMs, it parses data to create a knowledge graph and answer user questions about a user-provided private dataset.

GraphRAG uses LLMs to create a comprehensive knowledge graph detailing entities and their relationships from any collection of text documents.

It creates a "knowledge graph" that pre-analyzes "entities" such as people and places that appear in a text and their "relationships".

This graph allows it to generate responses to complex queries that require a broad understanding of the entire text.

It has been shown to produce more useful results than traditional RAG architectures when applied to a variety of scenarios, including social media, news articles, workplace productivity, and chemistry.

In contrast to GraphRAG, traditional RAGs are called "naive RAG" or "baseline RAG".

*In the IT world, "naive" means simple implementation.

## Does the emergence of GraphRAG make naive RAG unnecessary? Should we always use GraphRAG?

No. According to the GraphRAG paper, traditional RAG is superior to traditional search engines and vector search in answering direct questions (e.g., "Tell me about XX") using keyword search and semantic search, which are areas where RAG excels.

https://arxiv.org/html/2404.16130v1#:~:text=na%C3%AFve%20RAG%20produces%20the%20most%20direct%20responses%20across%20all%20comparisons

GraphRAG can generate more accurate responses to complex queries that require a broad understanding of the entire text.

## Are the answers GraphRAG outputs accurate?

It can answer questions with higher accuracy than traditional RAGs, but it does not necessarily output the "correct answer".

https://github.com/microsoft/graphrag/blob/main/RAI_TRANSPARENCY.md#what-are-graphrags-intended-uses

> GraphRAG is capable of providing high degrees of insight on complex information topics, however human analysis by a domain expert of the answers is needed in order to verify and augment GraphRAG’s generated responses.

## Who (where) is developing GraphRAG?

https://www.microsoft.com/en-us/research/blog/graphrag-unlocking-llm-discovery-on-narrative-private-data/

GraphRAG was developed by researchers at [Microsoft Research](https://www.microsoft.com/en-us/research/). It is now open source, and developers from all over the world are participating in its development.

## Is GraphRAG a Microsoft product?

No. GraphRAG itself is being researched by Microsoft Research, but the implementation (https://github.com/microsoft/graphrag) is open source software under the MIT License.

It has not yet been commercialized, particularly as an Azure service.

## What technology is GraphRAG developed with?

Python. A Jupyter Notebook interface is also available for operation.

The code is available from the following GitHub repository:

https://github.com/microsoft/graphrag

## How much does GraphRAG cost?

GraphRAG itself is open source and can be used for free. There is no need to purchase a license from Microsoft.

However, to actually run GraphRAG, resources such as large-scale language models and servers are required, and there is a fee for these resources.

In particular, a large cost is incurred at the time of index (knowledge graph) creation.

reference: https://techcommunity.microsoft.com/t5/ai-azure-ai-services-blog/graphrag-costs-explained-what-you-need-to-know/ba-p/4207978

## How do I use GraphRAG?

GraphRAG is actually a Python library and can be installed with the following command.

```
pip install graphrag
```

After installation, initialize (create) a workspace (working directory), set the LLM type, endpoint address, API key, model name, etc. in the configuration file, and create a knowledge base.

Once the knowledge base is created, send a question to GraphRAG, which will search the knowledge base internally and use the extracted information to generate an answer using the LLM.

You can use a Python notebook for this series of operations.

## Do I need Azure or OpenAI to use GraphRAG?

You can use Azure or OpenAI to use GraphRAG, but it can also be implemented on AWS, Google Cloud, on-premise servers, etc. 
