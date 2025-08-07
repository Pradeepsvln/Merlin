# Metadata Integration to Graph DB (Neo4j or Local Graph Store)

After parsing and summarizing manuals, Merlin extracts structured metadata such as:
- Part numbers and descriptions
- Cross-references between parts and illustrations
- Page and section location metadata
- Relationships among components (e.g., part-of, depends-on)

These entities and their relations are transformed into graph structures and pushed to a local graph database (e.g., Neo4j).

This metadata store is queried during chatbot operation to:
- Avoid rerunning full LLM inference
- Enable schema-aware answers for engineering lookups
- Display part hierarchy, dependencies, and illustrations without GPU usage

## Technologies
- `py2neo` or `neo4j-driver` for Python
- Can use embedded graph engines (e.g., SQLite with GraphView)
- Exports in Cypher or GraphML for portability

## Example Cypher Entity:
```cypher
CREATE (p:Part {id: "P-1004", name: "Pressure Regulator", location: "Manual B, Pg 47"})
CREATE (i:Image {url: "./img/regulator.png"})
CREATE (p)-[:ILLUSTRATED_BY]->(i)
```
