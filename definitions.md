# NeuraShare - Definitions

Here are all the concepts emerging from the NeuraShare project:
- Data singleton
- Data chunk
- `Refers to` relation
- `Is part of` relation

## Data Singleton

A _Data Singleton_ is a piece of knowledge, describing a concept. It is composed of:
- a name
- a short description
- a long description

From them are generated `Refers to` relations, pointing at other data singletons emerging from the **long description**.
For each `Refers to` relation, the frontend client ( [NeuraShare Workstation](https://github.com/NeuraShare/workstation) )
generates a link to those referenced singletions.

Data Singletons are kind of "contained" in `Data Chunk`s, with a `Is part of` relation. 

## Data Chunk

## `Refers to` relation

## `Is part of` relation