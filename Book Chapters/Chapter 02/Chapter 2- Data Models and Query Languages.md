## Overview

- Focuses on how data is represented (data models) and accessed (query languages) in data-intensive applications.
- Explores trade-offs between relational, document, and graph models, and their implications for application design.
---
## Key Concepts

### Data Models

- **Relational Model**
    - Data organized into tables (relations) with rows and columns.
    - Strengths: Structured, supports joins, good for many-to-one/many-to-many relationships.
    - Weaknesses: Impedance mismatch with object-oriented programming; less flexible for hierarchical data.
- **Document Model**
    - Data stored as nested, self-contained documents (e.g., JSON, XML).
    - Strengths: Flexible for hierarchical data, locality (data fetched together stays together).
    - Weaknesses: Poor support for joins; schema-on-read can complicate queries.
- **Graph Model**
    - Data represented as nodes (entities) and edges (relationships).
    - Strengths: Ideal for complex relationships (e.g., social networks, recommendation systems).
    - Variants: Property graphs (nodes/edges with properties) and triple-stores (RDF/SPARQL).

### Query Languages

- **Declarative (e.g., SQL)**
    - Specify _what_ you want, not _how_ to get it; database optimizes execution.
    - Benefits: Easier to write, adaptable to changing storage structures.
- **Imperative (e.g., MapReduce)**
    - Define _how_ to process data step-by-step.
    - Benefits: Fine-grained control; suited for distributed systems.
- **Graph Queries**
    - Cypher (for property graphs) and SPARQL (for RDF) enable traversal of relationships.
    - Powerful for interconnected data but less general-purpose.

### Trade-Offs

- **Scalability**: NoSQL (document/graph) arose for better scalability than relational databases.
- **Flexibility**: Document/graph models handle evolving schemas better; relational models enforce structure.
- **Query Complexity**: Relational excels at joins; document/graph better for localized or relational queries.

## Notable Insights

- **Object-Relational Mismatch**: Disconnect between application code (objects) and relational tables requires translation (e.g., ORMs like Hibernate).
- **NoSQL Origins**: Driven by need for scale, flexibility, and handling unstructured data.
- **Datalog**: A foundational query language blending declarative and relational concepts, influencing modern systems.

## Practical Takeaways

- Choose a data model based on:
    - Data structure (hierarchical vs. tabular vs. relational).
    - Query patterns (joins vs. locality vs. traversals).
    - Scalability needs (volume, throughput).
- Query language choice impacts developer productivity and system performance.