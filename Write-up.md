# OrientDB

## Homepage
http://orientdb.org/

## Github Repo
https://github.com/orientechnologies/orientdb

## Introduce
OrientDB is the first Open Source Multi-Model NoSQL DBMS with the support of Native Graphs, Documents, Full-Text search, Reactivity, Geo-Spatial and Object Oriented concepts. It's written in Java and it's amazingly fast. No expensive run-time JOINs, connections are managed as persistent pointers between records. You can traverse thousands of records in no time. Supports schema-less, schema-full and schema-mixed modes. Has a strong security profiling system based on user, roles and predicate security and supports SQL amongst the query languages.

OrientDB uses several indexing mechanisms based on B-tree and Extendible hashing, the last one is known as "hash index", there are plans to implement LSM-tree and Fractal tree index based indexes.

## Architecture

OrientDB can be distributed across different servers and used in different ways to achieve the maximum of performance, scalability and robustness.

OrientDB uses the Hazelcast Open Source project for auto-discovering of nodes, storing the runtime cluster configuration and synchronize certain operations between nodes. Some of the references in this page are linked to the Hazelcast official documentation to get more information about such topic.


## Data Model
The OrientDB engine supports Graph, Document, Key/Value, and Object models, so you can use OrientDB as a replacement for a product in any of these categories.

However, the main reason why users choose OrientDB is because of its true Multi-Model DBMS abilities, which combine all the features of the four models into the core. These abilities are not just interfaces to the database engine, but rather the engine itself was built to support all four models. This is also the main difference to other multi-model DBMSs, as they implement an additional layer with an API, which mimics additional models. However, under the hood, they're truly only one model, therefore they are limited in speed and scalability.

### The Document Model

The data in this model is stored inside documents. A document is a set of key/value pairs (also referred to as fields or properties), where the key allows access to its value. Values can hold primitive data types, embedded documents, or arrays of other values. Documents are not typically forced to have a schema, which can be advantageous, because they remain flexible and easy to modify. Documents are stored in collections, enabling developers to group data as they decide. OrientDB uses the concepts of "classes" and "clusters" as its form of "collections" for grouping documents.



| Relational Model | Document Model | OrientDB Document Model |
|:----------------:|:--------------:|:-----------------------:|
| Table            | Collection     | Class or Cluster        |
| Row              | Document       | Document                |
| Column           | Key/value pair | Document field          |
| Relationship     | not available  | Link                    |


### The Graph Model

A graph represents a network-like structure consisting of Vertices (also known as Nodes) interconnected by Edges (also known as Arcs). OrientDB's graph model is represented by the concept of a property graph, which defines the following:

- **Vertex** - an entity that can be linked with other Vertices and has the following mandatory properties:
  - unique identifier
  - set of incoming Edges
  - set of outgoing Edges

- **Edge** - an entity that links two Vertices and has the following mandatory properties:
  - unique identifier
  - link to an incoming Vertex (also known as head)
  - link to an outgoing Vertex (also known as tail)
  - label that defines the type of connection/relationship between head and tail vertex

In addition to mandatory properties, each vertex or edge can also hold a set of custom properties. These properties can be defined by users, which can make vertices and edges appear similar to documents. In the table below, you can find a comparison between the graph model, the relational data model, and the OrientDB graph model:

| Relational Model | Graph Model              | OrientDB Graph Model                                    |
|:----------------:|:------------------------:|:-------------------------------------------------------:|
| Table            | Vertex and Edge Class    | Class that extends "V" (for Vertex) and "E" (for Edges) |
| Row              | Vertex                   | Vertex                                                  |
| Column           | Vertex and Edge property | Vertex and Edge property                                |
| Relationship     | Edge                     | Edge                                                    |


### The Key/Value Model
This is the simplest model of the three. Everything in the database can be reached by a key, where the values can be simple and complex types.
OrientDB supports Documents and Graph Elements as values allowing for a richer model, than what you would normally find in the classic Key/Value model.

### The Object Model

This model has been inherited by Object Oriented programming and supports Inheritance between types (sub-types extends the super-types), Polymorphism when you refer to a base class and Direct binding from/to Objects used in programming languages.

The table below illustrates the comparison between the relational model, the Object model, and the OrientDB Object model:



| Relational Model | Object Model    | OrientDB Object Model                  |
|:----------------:|:---------------:|:--------------------------------------:|
| Table            | Class           | Class or Cluster                       |
| Row              | Object          | Document or Vertex                     |
| Column           | Object property | Document field or Vertex/Edge property |
| Relationship     | Pointer         | Link                                   |

## Applications

- Banking
- Big Data
- Fraud prevention
- Loan management software
- Recommendation engines
- Social networking
- Traffic management systems
