# Graph-Generator
Graph Generation Using LangChain and Neo4j

First, the document is split into chunks. In the paper they maintained paragraph structure while chunking. However, that is hard to do in a generic way. Therefore, we will use naive chunking here.

Next, each chunk is processed by the LLM to identify atomic facts, which are the smallest, indivisible units of information that capture core details. For instance, from the sentence “The CEO of Neo4j, which is in Sweden, is Emil Eifrem” an atomic fact could be broken down into something like “The CEO of Neo4j is Emil Eifrem.” and “Neo4j is in Sweden.” Each atomic fact is focused on one clear, standalone piece of information.

From these atomic facts, key elements are identified. For the first fact, “The CEO of Neo4j is Emil Eifrem,” the key elements would be “CEO,” “Neo4j,” and “Emil Eifrem.” For the second fact, “Neo4j is in Sweden,” the key elements would be “Neo4j” and “Sweden.” These key elements are the essential nouns and proper names that capture the core meaning of each atomic fact.
