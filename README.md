# Merlin AI Bot

Merlin is a standalone, offline AI chatbot built for a research organization. It is designed to understand, summarize, and retrieve content from complex technical manuals, including text, schematics, and part diagrams. Powered by an on-disk LLaMA model, Merlin supports zero-internet environments and campus-network-only deployments.

## Key Capabilities
- ✅ Summarizes lengthy technical documentation using prompt-based interactions
- 🎯 Retrieves part-specific illustrations and schematics upon user query
- 🧠 Learns document metadata during ingestion and offloads it to a graph database to minimize GPU usage
- 🛠️ Fully offline and disk-based, suitable for air-gapped or campus environments

## Value Proposition
- 📚 Reduces the time engineers and researchers spend navigating dense manuals
- 🚀 Boosts efficiency by offering proactive, context-aware document assistance
- 🔒 Supports privacy-focused environments (no cloud dependency)
- ⚡ Reduces inference cost post-training via graph-based recall
