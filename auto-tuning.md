# GraphRAG "Auto-tuning"

https://www.microsoft.com/en-us/research/blog/graphrag-auto-tuning-provides-rapid-adaptation-to-new-domains/

An automated tool that generates domain-specific prompts, resulting in higher quality knowledge graphs.

It is already included in the [GraphRAG core library repository](https://github.com/microsoft/graphrag).

Takes source content and automatically generates a set of domain-specific indexing prompts.

## Description

https://www.microsoft.com/en-us/research/blog/graphrag-auto-tuning-provides-rapid-adaptation-to-new-domains/

> The knowledge graph creation process is called indexing. An LLM, guided by a set of domain-specific prompts, reads all the source content and extracts the relevant information, including entities and relationships, which are then used to construct the graph.

> However, each domain has a different set of entity and relationship types. In the field of chemistry, for instance, entity types include molecules, enzymes, and reactions, while relationship types include “catalyzes” and “reduces.” Although our default news domain prompts in GraphRAG can produce a graph when applied to chemistry, they don’t capture the specific content a chemist would expect. 

> we developed an automated tool that generates domain-specific prompts, which are tuned and ready to use. 

## How to use

See the documentation below

https://github.com/microsoft/graphrag/blob/main/docsite/posts/prompt_tuning/auto_prompt_tuning.md