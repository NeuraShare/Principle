# Neurashare - Definitions

Here are all the concepts emerging from the Neurashare project:
- Data singleton
- Data chunk
- Knowledge Graph
- `Refers to` relation
- `Is part of` relation

## Data Singleton

A _Data Singleton_ is a piece of knowledge, describing a concept. It is composed of:
- some pragmas
- a name
- a short description
- a long description

From them are generated `Refers to` relations, pointing at other data singletons emerging from the **long description**.
For each `Refers to` relation, the frontend client ( [Neurashare Workstation](https://github.com/Neurashare/workstation) )
generates a link to those referenced singletions.

Data Singletons are kind of "contained" in `Data Chunk`s, with a `Is part of` relation. It can be included in more than one
Chunk.

A Data Singleton is represented by one node in the knowledge graph.

### Pragmas

Pragmas are builtin informations about the Data Singleton. They define for example the imported chunks.

## Data Chunk

A _Data Chunk_ is a group of Data Singletons that have the `Is part of` relation with the Data Chunk node.

A Data Chunk is kind of a tag added to Data Singletons.

When writing a new Data Singleton, the user need to define of which Data Chunk the Singleton is related to even if it is `none`.
When including its own Data Singleton to a Data Chunk, the server will know with which other Data Singletons the new one should be linked to. In that case, multiple meaning Singletons can't exist, Chunk act like contextual uses of the Data Singletons.

All concepts defined by data singletons that are neighbors of a Chunk are considered in the chunk's context.

## `Refers to` relation

A _Refers to_ relation is a relation between two Data Singletons. They are automatically generated from the description of a Data Singleton.

[**How it works**](refers_to.md)

## `Is part of` relation

A _Is part of_ relation is a relation between a Data Singleton and a Chunk node in the Knowledge Graph. It is defined by one pragma at the beginning of the Data Singleton description:

(This format isn't definitive)
```
#import chunk Physics

...
```

This creates a relation of kind _Is part of_ between the Data Singleton (the description) and the Physics chunk.

## Knowledge Graph

The _Knowledge Graph_ is the whole graph containing all the Data Singletons, Chunks, relations, ...

When working with Neurashare, the user is working with this graph. For example, all the `Refers to` relations are defined from this graph by browsing it.