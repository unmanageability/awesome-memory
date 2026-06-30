# awesome-memory

> A curated list of **memory layers for LLMs and AI agents** — the libraries, frameworks, and
> services that give agents persistent, long-term memory across sessions.

If you're choosing a memory layer, start here. Projects are grouped by category and ranked by
GitHub stars. Each entry notes what it does, its **memory model** (vector / graph / hybrid /
tiered / profile), whether it's **open source or commercial**, and how it's hosted.

**GitHub star counts are a snapshot taken 2026-06-30 via the GitHub API and move fast.** "Memory
model" labels are simplified — read the docs before committing. Pricing is vendor-stated and
changes often.

---

## Contents

- [At a glance — ranked by stars](#at-a-glance--ranked-by-stars)
- [Dedicated agent-memory layers](#dedicated-agent-memory-layers)
- [Knowledge-graph & temporal-memory engines](#knowledge-graph--temporal-memory-engines)
- [RAG / retrieval engines (memory-adjacent)](#rag--retrieval-engines-memory-adjacent)
- [Personal-AI / "second brain"](#personal-ai--second-brain)
- [Commercial & managed platforms](#commercial--managed-platforms)
- [Curated lists & research collections](#curated-lists--research-collections)
- [Architecture cheat-sheet](#architecture-cheat-sheet)
- [How to choose](#how-to-choose)

---

## At a glance — ranked by stars

| ★ Stars | Project | Type | Memory model | License | Hosting |
|--------:|---------|------|--------------|---------|---------|
| 59,756 | [Mem0](https://github.com/mem0ai/mem0) | Memory layer | Hybrid (vector + graph + KV) | Apache-2.0 | OSS + SaaS |
| 37,180 | [LightRAG](https://github.com/HKUDS/LightRAG) | RAG engine | Graph + vector | MIT | OSS |
| 34,096 | [GraphRAG](https://github.com/microsoft/graphrag) (Microsoft) | RAG engine | Knowledge graph | MIT | OSS |
| 28,169 | [Graphiti](https://github.com/getzep/graphiti) (powers Zep) | Memory engine | Temporal knowledge graph | Apache-2.0 | OSS + SaaS (Zep) |
| 27,953 | [Supermemory](https://github.com/supermemoryai/supermemory) | Memory layer | Vector / context engine | MIT | OSS + SaaS |
| 25,880 | [Cognee](https://github.com/topoteretes/cognee) | Memory layer | Hybrid (vector + graph) | Apache-2.0 | OSS + SaaS |
| 23,589 | [Letta](https://github.com/letta-ai/letta) (ex-MemGPT) | Memory layer | OS-tiered (core/recall/archival) | Apache-2.0 | OSS + SaaS |
| 15,605 | [Second-Me](https://github.com/mindverse/Second-Me) | Personal AI | Personal memory/identity | Apache-2.0 | OSS |
| 15,503 | [Memori](https://github.com/GibsonAI/memori) (GibsonAI) | Memory layer | Relational / SQL-native | OSS¹ | OSS + SaaS |
| 13,948 | [memU](https://github.com/NevaMind-AI/memU) | Memory layer | Vector / profile | Source-available¹ | OSS + SaaS |
| 12,689 | [txtai](https://github.com/neuml/txtai) | Embeddings DB | Vector | Apache-2.0 | OSS |
| 10,037 | [MemOS](https://github.com/MemTensor/MemOS) | Memory OS | Hybrid (MemCube) | Apache-2.0 | OSS |
| 7,909 | [R2R](https://github.com/SciPhi-AI/R2R) | RAG engine | Hybrid (vector + graph) | MIT | OSS + SaaS |
| 5,658 | [Honcho](https://github.com/plastic-labs/honcho) | Memory layer | User-profile / personalization | AGPL-3.0 | OSS + SaaS |
| 4,714 | [Zep](https://github.com/getzep/zep) | Memory platform | Temporal KG (Graphiti) | Apache-2.0 | OSS + SaaS |
| 3,816 | [fast-graphrag](https://github.com/circlemind-ai/fast-graphrag) | RAG engine | Graph (adaptive) | MIT | OSS |
| 3,551 | [MIRIX](https://github.com/mirix-ai/MIRIX) | Memory layer | Multimodal / screen-activity | Apache-2.0 | OSS |
| 3,137 | [MemMachine](https://github.com/MemMachine/MemMachine) | Memory layer | Pluggable storage/retrieval | Apache-2.0 | OSS |
| 3,131 | [ReMe / MemoryScope](https://github.com/modelscope/memoryscope) (Alibaba) | Memory layer | Vector + management kit | Apache-2.0 | OSS |
| 2,772 | [Memobase](https://github.com/memodb-io/memobase) | Memory layer | User-profile / time-aware | Apache-2.0 | OSS + SaaS |
| 2,625 | [Memary](https://github.com/kingjulio8238/Memary) | Memory layer | Knowledge graph (Neo4j) | MIT | OSS (less active) |
| 2,165 | [MemSearch](https://github.com/zilliztech/memsearch) (Zilliz) | Memory layer | Vector (Markdown + Milvus) | MIT | OSS |
| 1,590 | [Pixeltable](https://github.com/pixeltable/pixeltable) | Data backend | Multimodal store/index | Apache-2.0 | OSS |
| 1,531 | [LangMem](https://github.com/langchain-ai/langmem) (LangChain) | Memory SDK | Vector + extraction | MIT | OSS |
| 1,488 | [MemoryOS](https://github.com/BAI-LAB/MemoryOS) | Memory OS | Hierarchical (short/mid/long) | Apache-2.0 | OSS |
| 1,071 | [A-MEM](https://github.com/agiresearch/A-mem) | Research | Agentic / Zettelkasten | MIT | OSS |
| 928 | [WhyHow KG Studio](https://github.com/WhyHow-AI/knowledge-graph-studio) | KG builder | Knowledge graph | MIT | OSS (less active) |
| 692 | [Memoripy](https://github.com/caspianmoon/memoripy) | Memory layer | Vector + decay/clustering | Apache-2.0 | OSS |
| 204 | [Nemori](https://github.com/nemori-ai/nemori) | Memory layer | Episodic | MIT | OSS |
| 68 | [MFS](https://github.com/zilliztech/mfs) (Zilliz) | Context harness | Vector (local, file-like) | Apache-2.0 | OSS |
| 11 | [membase](https://github.com/unibaseio/membase) (Unibase) | Memory SDK | Decentralized | OSS¹ | OSS (early) |

¹ GitHub did not return a standard SPDX license id — verify the license in the repo before use.

> **Curated lists** (not in the table): [IAAR-Shanghai/Awesome-AI-Memory](https://github.com/IAAR-Shanghai/Awesome-AI-Memory)
> (1,032★) and [topoteretes/awesome-ai-memory](https://github.com/topoteretes/awesome-ai-memory) (803★).

---

## Dedicated agent-memory layers

Purpose-built "memory layers" that sit between your app and the LLM — capturing, storing, and
recalling per-user / per-agent memories.

### [Mem0](https://github.com/mem0ai/mem0) · 59,756★ · Apache-2.0 · Python/TS
The de-facto default and most-starred project in the space. A model-agnostic memory layer that
auto-extracts facts from conversations and retrieves them with **multi-signal recall: semantic
vector similarity + BM25 keyword + graph entity-linking**. ~21 framework integrations (LangChain,
LlamaIndex, CrewAI, AutoGen…) and ~20 vector-store backends. Ships an `OpenMemory` MCP server for
local-first use. Open-source self-host **plus** the managed **Mem0 Platform** (Free / Starter $19 /
Growth $79 / Pro $249 / Enterprise). YC-backed.

### [Supermemory](https://github.com/supermemoryai/supermemory) · 27,953★ · MIT · TypeScript
"The Memory API for the AI era." A fast, scalable memory **and context engine** that can run fully
locally; ingests docs, chats, and web content and exposes a retrieval API plus connectors. OSS core
+ hosted SaaS at supermemory.ai.

### [Letta](https://github.com/letta-ai/letta) (formerly MemGPT) · 23,589★ · Apache-2.0 · Python
The MemGPT thesis productized. Implements **OS-inspired tiered memory** — *core* (in-context),
*recall* (conversation history), and *archival* (long-term vector store) — where the **agent edits
its own memory** through tool calls (`core_memory_append`, `archival_memory_insert/search`). Comes
with the Agent Development Environment (ADE). OSS server + **Letta Cloud** (Free / Pro $20 / API
usage / Enterprise). `cpacker/MemGPT` redirects here.

### [Memori](https://github.com/GibsonAI/memori) · 15,503★ · OSS · Python
Agent-native memory infrastructure that's notably **SQL-native** — it turns agent execution and
conversation into structured, queryable, persistent state in a standard relational database.
LLM-agnostic. OSS + GibsonAI managed cloud. Good fit if you want memory you can query with plain SQL.

### [memU](https://github.com/NevaMind-AI/memU) · 13,948★ · source-available · Python
Personal memory for agents focused on **fast retrieval, self-evolving skills, and lower cost** —
aimed at companions and personal assistants. OSS + cloud.

### [MemOS](https://github.com/MemTensor/MemOS) · 10,037★ · Apache-2.0 · Python/TS
A self-evolving "**memory operating system**" for LLMs/agents. Introduces a `MemCube` abstraction,
hybrid retrieval, and cross-task skill reuse; claims ~35% token savings via ultra-persistent memory.

### [Honcho](https://github.com/plastic-labs/honcho) · 5,658★ · AGPL-3.0 · Python
Memory library for stateful agents from Plastic Labs, specialized in **user modeling /
personalization** ("theory of mind") — builds rich, evolving representations of each user rather than
generic fact storage. OSS + hosted.

### [MIRIX](https://github.com/mirix-ai/MIRIX) · 3,551★ · Apache-2.0 · Python
A multi-agent personal assistant that captures **on-screen activity** and consolidates real-time
**multimodal** inputs into structured memories — a knowledge base that adapts to your digital life.

### [MemMachine](https://github.com/MemMachine/MemMachine) · 3,137★ · Apache-2.0 · Python
A "universal memory layer for AI agents" emphasizing **scalable, extensible, interoperable** storage
and retrieval to streamline agent state management. Newer entrant.

### [ReMe / MemoryScope](https://github.com/modelscope/memoryscope) · 3,131★ · Apache-2.0 · Python
Alibaba/ModelScope's "Memory Management Kit for Agents" (*Remember Me, Refine Me*). Provides
long-term memory with consolidation/refinement utilities and a service interface.

### [Memobase](https://github.com/memodb-io/memobase) · 2,772★ · Apache-2.0 · Python
**User-profile-based**, time-aware long-term memory built for AI chatbot / companion applications —
maintains evolving structured user profiles. OSS + Memobase cloud.

### [Memary](https://github.com/kingjulio8238/Memary) · 2,625★ · MIT · Python
"The open-source memory layer for autonomous agents." **Knowledge-graph memory** on Neo4j with entity
knowledge and reasoning. Note: last meaningful push in 2024 — historically influential but **less
actively maintained**.

### [MemSearch](https://github.com/zilliztech/memsearch) · 2,165★ · MIT · Python
Zilliz's persistent, unified memory layer for **coding agents** (Claude Code, Codex). **Markdown
files are the source of truth; Milvus is a rebuildable shadow index.** Hybrid dense + BM25 sparse +
reciprocal-rank-fusion recall over three layers; a stop-hook auto-captures transcripts and summarizes
them. Backends: Milvus Lite (default) / Zilliz Cloud / self-hosted Docker. Vector, not graph.

### [LangMem](https://github.com/langchain-ai/langmem) · 1,531★ · MIT · Python
LangChain's memory SDK for LangGraph/LangChain agents — extract, store, and retrieve long-term
memories, with background ("hot path" vs. async) memory formation.

### [MemoryOS](https://github.com/BAI-LAB/MemoryOS) · 1,488★ · Apache-2.0 · Python
A "memory operating system" for personalized agents with a **hierarchical short/mid/long-term**
store. EMNLP 2025 (Oral).

### [A-MEM](https://github.com/agiresearch/A-mem) · 1,071★ · MIT · Python
"Agentic Memory for LLM Agents" — a research implementation using **Zettelkasten-style** dynamic
note-linking so memories interconnect and evolve. Good reference architecture.

### [Memoripy](https://github.com/caspianmoon/memoripy) · 692★ · Apache-2.0 · Python
Lightweight memory layer with short- and long-term storage, **semantic clustering**, and optional
**memory decay** for context-aware apps.

### [Nemori](https://github.com/nemori-ai/nemori) · 204★ · MIT · Python
A minimalist MVP demonstrating that aligning AI memory to **human episodic-memory granularity** lets
simple methods rival complex frameworks on conversational tasks.

### [MFS](https://github.com/zilliztech/mfs) · 68★ · Apache-2.0 · Python
Zilliz's "Multi-source File-like Search" — a **context harness** that unifies code, session memory,
skills, docs, messages, and external sources into one searchable, browsable, **file-like** workspace
(`ls`/`cat`/`tree`/`head`/`tail`). Runs **fully local by default** (BGE-M3 int8 embeddings, no API
key, no GPU); optional Milvus/Zilliz Cloud + Postgres backends. New and fast-moving.

### [membase](https://github.com/unibaseio/membase) · 11★ · Python
Early SDK for **decentralized** agent memory on the Unibase data-availability layer. Very early-stage.

---

## Knowledge-graph & temporal-memory engines

Memory built on graphs — entities, relationships, and (for Graphiti) time. These are squarely
"agent memory" but differ from vector-first layers by modeling structure.

### [Graphiti](https://github.com/getzep/graphiti) · 28,169★ · Apache-2.0 · Python
The open-source **temporal knowledge-graph** engine that powers **Zep**. Bi-temporal: tracks both
when an event occurred and when it was ingested, with explicit **edge validity intervals**, and
updates incrementally in real time. Self-host on Neo4j, FalkorDB, Kuzu (deprecated but supported),
or Amazon Neptune. Backed by the arXiv paper *"Zep: A Temporal Knowledge Graph Architecture for
Agent Memory."* Best when relationships and "what was true when" matter.

### [Cognee](https://github.com/topoteretes/cognee) · 25,880★ · Apache-2.0 · Python
Open-source AI memory platform that ingests data in any format and builds a self-hosted **knowledge
graph + vector embeddings (hybrid)**. Its `cognify` / ECL (Extract–Cognify–Load) pipeline uses an
LLM to extract entities and relationships, embeds them (pgvector/LanceDB/Qdrant) and commits edges to
a graph (Neo4j/Kuzu/Postgres-native). ~14 retrieval modes, cognitive-science-grounded ontology
generation. OSS + Cognee Cloud. Maintained by topoteretes (who also publish `awesome-ai-memory`).

---

## RAG / retrieval engines (memory-adjacent)

Not per-user agent memory, but frequently used *as* memory over a document corpus. Reach for these
when the "memory" is a knowledge base rather than evolving user/agent state.

- **[LightRAG](https://github.com/HKUDS/LightRAG)** · 37,180★ · MIT — Simple, fast **graph-based RAG** (EMNLP 2025); dual-level retrieval over an extracted KG.
- **[GraphRAG](https://github.com/microsoft/graphrag)** · 34,096★ · MIT — Microsoft's modular **graph-based RAG**: entity/community extraction + hierarchical summarization for global questions.
- **[txtai](https://github.com/neuml/txtai)** · 12,689★ · Apache-2.0 — All-in-one **embeddings database** for semantic search and LLM workflows; a common DIY memory substrate.
- **[R2R](https://github.com/SciPhi-AI/R2R)** · 7,909★ · MIT — Production **agentic RAG** with hybrid vector + KG, collections, and a RESTful API.
- **[fast-graphrag](https://github.com/circlemind-ai/fast-graphrag)** · 3,816★ · MIT — GraphRAG that **adapts** to your data and queries; cheaper/faster than full GraphRAG.
- **[WhyHow KG Studio](https://github.com/WhyHow-AI/knowledge-graph-studio)** · 928★ · MIT — Knowledge-graph building/management platform (less active).

---

## Personal-AI / "second brain"

### [Second-Me](https://github.com/mindverse/Second-Me) · 15,605★ · Apache-2.0 · Python
Train a personal AI "self" that learns your identity and context locally — personal memory framed as
a digital extension of you, rather than infrastructure for third-party agents.

---

## Commercial & managed platforms

Most leaders are **open-core**: self-host the OSS, or pay for a managed tier with persistence, scaling,
auth, and compliance.

| Platform | Backed by OSS | Notes |
|----------|---------------|-------|
| **Mem0 Platform** | [mem0](https://github.com/mem0ai/mem0) | Free / $19 / $79 / $249 / Enterprise; SOC 2, HIPAA |
| **Zep Cloud** | [Graphiti](https://github.com/getzep/graphiti) | Managed temporal-KG memory; LangChain/LlamaIndex integrations |
| **Letta Cloud** | [letta](https://github.com/letta-ai/letta) | Free / Pro $20 / usage-based API / Enterprise |
| **Supermemory** | [supermemory](https://github.com/supermemoryai/supermemory) | Hosted memory API + app |
| **Cognee Cloud** | [cognee](https://github.com/topoteretes/cognee) | Managed knowledge-graph memory |
| **GibsonAI** | [Memori](https://github.com/GibsonAI/memori) | Managed SQL-native agent memory |
| **Honcho (Plastic Labs)** | [honcho](https://github.com/plastic-labs/honcho) | Hosted user-modeling memory |
| **Memobase** | [memobase](https://github.com/memodb-io/memobase) | Hosted user-profile memory |

**Closed-source / product-embedded memory** (no self-host): OpenAI ChatGPT Memory, Anthropic's Claude
memory tool / context management, Pinecone (vector DB + Assistant), and Zilliz Cloud (managed Milvus,
the substrate under MemSearch/MFS).

---

## Curated lists & research collections

- **[IAAR-Shanghai/Awesome-AI-Memory](https://github.com/IAAR-Shanghai/Awesome-AI-Memory)** · 1,032★
  — Continuously updated knowledge base: **507 papers + 107 OSS projects** across long-term memory,
  reasoning, retrieval, and memory-native system design. A "Systems and Open Sources" section lists
  usable tools, not just papers.
- **[topoteretes/awesome-ai-memory](https://github.com/topoteretes/awesome-ai-memory)** · 803★ — Tools,
  frameworks, optimizers, and storage layers, tagged on three axes: **open / managed / closed** ×
  **tool / framework / optimizer / storage** × **graph / vector**. Maintained by the Cognee team.

---

## Architecture cheat-sheet

| Approach | What it's good at | Projects |
|----------|-------------------|----------|
| **Vector / embedding recall** | Fast semantic recall of past facts & messages | Mem0 (core), MemSearch, MFS, txtai, Memoripy, memU, LangMem |
| **Knowledge graph / temporal KG** | Relationships, entities, "what was true when" | Graphiti/Zep, Memary, GraphRAG, LightRAG |
| **Hybrid (vector + graph)** | Semantic recall *plus* structured reasoning | Cognee, Mem0, R2R, MemOS |
| **OS-style tiered (agent self-manages)** | Long-running agents that edit their own memory | Letta/MemGPT, MemOS, MemoryOS |
| **User-profile / personalization** | Companions, assistants, per-user modeling | Honcho, Memobase, memU, Second-Me, MIRIX |
| **Relational / SQL-native** | Queryable, auditable structured memory | Memori |
| **Episodic** | Human-like event-grained recall | Nemori, A-MEM |

---

## How to choose

- **Want the safe default with the biggest ecosystem and a managed option** → **Mem0**.
- **Need relationship-aware, time-aware facts (temporal knowledge graph)** → **Zep / Graphiti** or **Cognee**.
- **Want agents that manage their own memory (OS metaphor)** → **Letta**.
- **Need fully local / no API keys / self-hosted** → **MFS**, **MemSearch**, **Memoripy**.
- **Building companions or per-user personalization** → **Honcho**, **Memobase**, **memU**.
- **Want SQL-queryable, auditable structured memory** → **Memori**.
- **Memory is really a doc corpus, not evolving user state** → **GraphRAG**, **LightRAG**, **R2R**, **txtai**.

---

<sub>Compiled 2026-06-30 via a multi-source deep-research pass with adversarial fact-checking, plus
live GitHub API metadata. Star counts, pricing, and licenses are point-in-time — verify before
relying on them. PRs welcome.</sub>
