# GraphRAG Demo

This repository was initially created as a companion to a Microsoft Tech Community blog article: [Your First GraphRAG Demo - A Video Walkthrough](https://techcommunity.microsoft.com/blog/aiplatformblog/your-first-graphrag-demo---a-video-walkthrough/4410246).

See the below links for more information about GraphRAG:

|   |   |
|---|---|
| Code | 👉 [GraphRAG GitHub Repository](https://github.com/microsoft/graphrag/blob/main/README.md) |
| | 👉 [Read the docs](https://microsoft.github.io/graphrag) |
| Research | 👉 [Microsoft Research Blog Post](https://www.microsoft.com/en-us/research/blog/graphrag-unlocking-llm-discovery-on-narrative-private-data/) |
| Industrialization | 👉 [GraphRAG Accelerator solution](https://github.com/Azure-Samples/graphrag-accelerator) |
|   |   |

## Why GraphRAG
While traditional RAG (the top "N" search pattern) allows for easy access to information, GraphRAG may offer additional capability with dealing challenging topics or complex information spaces.

The table below provides a quick comparison for reference. The key takeaway is that many Generative AI topics involve a tradeoff between cost and speed versus scale and depth of reasoning.

With the GraphRAG design, a lot of reasoning is done upfront to generate a corpus with much greater depth later on. This approach is more expensive initially and has longer query times, but it allows for a depth of analysis that other techniques can't achieve. It's definitely a case of choosing the right tool for the right job.

<div align="center">

![RAG v GraphRAG Comparison](/assets/approach_comparision_tbl.png "RAG v GraphRAG Comparison")
**Table: RAG v GraphRAG Comparison**

</div>

## Local Environment Setup
For guidance on how to set up your local environment, follow the steps in [Local Environment Setup](./local-environment-setup.md).

## Run GraphRAG Use Case Notebooks

- [Use Case A Research Assistant](./Use%20Case%20A%20Research%20Assistant.ipynb)

More to come!

## Visualize the Graph

Follow the steps in [GraphRAG Visualization Guide](https://microsoft.github.io/graphrag/visualization_guide/).



