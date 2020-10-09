# Neurashare - Definitions

Here are all the concepts emerging from the Neurashare project:
- Data singleton
- Data chunk
- Knowledge Graph
- `Refers to` relation
- `Is part of` relation

## Data Singleton

A _Data Singleton_ is a piece of knowledge, describing a concept. It is composed of:
- a name
- a short description
- a long description

From them are generated `Refers to` relations, pointing at other data singletons emerging from the **long description**.
For each `Refers to` relation, the frontend client ( [Neurashare Workstation](https://github.com/Neurashare/workstation) )
generates a link to those referenced singletions.

Data Singletons are kind of "contained" in `Data Chunk`s, with a `Is part of` relation. It can be included in more than one
Chunk.

A Data Singleton is represented by one node in the knowledge graph.

## Data Chunk

A _Data Chunk_ is a group of Data Singletons that have the `Is part of` relation with the Data Chunk node.

A Data Chunk is kind of a tag added to Data Singletons.

When writing a new Data Singleton, the user need to define of which Data Chunk the Singleton is related to even if it is `none`.
When including its own Data Singleton to a Data Chunk, the server will know with which other Data Singletons the new one should be linked to. In that case, multiple meaning Singletons can't exist, Chunk act like contextual uses of the Data Singletons.

## `Refers to` relation

## `Is part of` relation

## Knowledge Graph
