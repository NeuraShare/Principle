# `Refers To` relation

---

/!\ The Data Singleton format isn't defined yet and can change at any time. 

---

## How it works

Those relations are generated between Data Singletons and from their own definitions.

When adding a Data Singleton to a chunk via the appropriate pragma, your singleton is added to the chunk too.
Then, when uploading your Data Singleton to the server, it will process your definitions and check if any of the words refers to an other data singleton in the same
chunk. If it does, one _Refers To_ relation is created.

## Example


Thermodynamics Data Singleton:
```
#include chunk Science

# Thermodynamics

Some description about thermodynamics laws.
```

Law Data Singleton:
```
#include chunk Science

# Law

What is a science law?
```

Here, a reference to `Science::Law` will be infered from the Thermodynamics Singleton so that a _Refers to_ relation will be created between them.

## See Also

- [Knowledge Graph]()
- [Data Singleton]()
- [Chunk]()