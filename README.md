# T0xN: Cognitive Data Architecture

![Status](https://img.shields.io/badge/Status-Research%20%26%20Prototyping-blueviolet)
![License](https://img.shields.io/badge/License-MIT-green)
![Philosophy](https://img.shields.io/badge/Philosophy-10th%20Man%20Rule-orange)

> **⚠️ PROJECT NATURE DISCLAIMER**
> This is not the work of a Senior Software Architect, but a **Human-AI collaboration experiment**.
> The human author provided the core intuition and some dusty academic memories, but lacks deep practical experience in modern software design.
> Everything that follows was structured, expanded, and formalized through interaction with **Gemini 3 Pro** (November 2025).
> Please treat this document not just as a technical proposal, but as a **benchmark of the architectural reasoning capabilities** of current Generative AI.

> **Pronunciation:** `/ˈtɒksɪn/` (Toxin)

## 1. TL;DR
**JSON is the bottleneck of the AI age.**
We are feeding supercomputers with text formats designed for simple websites twenty years ago. **Project T0xN** is a multi-modal data architecture designed to replace JSON in high-performance Data Science and Generative AI pipelines. It separates **Schema** from **Payload**, treats data as **Typed Tensors**, and introduces a **"Dreaming" cycle** to optimize storage autonomously.

---

## 2. The Vision: The Cognitive Mesh

We envision a future where data is not a static artifact stored on a disk, but a fluid, semantic entity that flows between Edge devices, Vector Databases, and Large Language Models with zero friction.

T0xN is not just a serialization format; it is a proposal for a **Distributed Cognitive Mesh**. A system where a sensor, a database, and an AI agent share the same "native language"—compact, typed, and binary-efficient—eliminating the massive computational waste of serialization and tokenization.

### What does T0xN mean?
The acronym is polymorphic, reflecting the observer's perspective:
1.  **T**oken **O**ptimized e**X**change **N**otation *(The Economic View)*
2.  **T**ensor **0**-latency e**X**ecution **N**ode *(The Performance View)*
3.  **T**ype **0x** **N**ative *(The Systems View)*

---

## 3. The Technical Lab: Why Redis?
T0xN is an agnostic research project, but it requires a concrete "test bench."
We chose the **Redis ecosystem** (Core, Streams, Modules) as our experimental laboratory not out of preference, but necessity:
1.  **Schema Fluidity:** To implement "Dreaming" (T0xN-D), the database must mutate data structures over time without SQL rigidity.
2.  **Direct Memory Access:** The Modules API allows C/Rust access to raw RAM, essential for testing **T0xN-B** (SIMD operations on contiguous bytes).
3.  **Streams:** Native support for Event Sourcing (T0xN-E).

---

## 4. The 5 Pillars of T0xN

### 🅰️ T0xN-A: The Alphabet
**Status:** 🟡 Draft Spec Ready
A human-readable, token-efficient text format acting as the interface layer. It hybridizes the visual density of **TOON** with the rigid schema definition of **TONL** and the semantic richness of **NTV**.
*   **Goal:** Reduce token consumption by ~60% compared to JSON.
*   **Feature:** Tabular Arrays with inline typing (`users[3]{id:u8, name:str}`).

### 🅱️ T0xN-B: The Binary Core
**Status:** 🔴 Conceptual / To Be Developed
The storage engine designed for in-memory implementation. Unlike BSON or MsgPack, it strictly separates the Schema (stored once) from the Payload (stored as contiguous C-structs).
*   **Goal:** Enable O(1) access to fields and SIMD vector operations directly on compressed memory.

### 🅲 T0xN-C: The Context Protocol
**Status:** 🔴 Conceptual / Future Research
A protocol for "Semantic Zipping". Using local Small Language Models (SLMs) to compress natural language user requests into dense logic formulas before they hit the network.

### 🅳 T0xN-D: The Dream (The 10th Man Rule)
**Status:** 🟣 Theoretical / Deep Research
A biological metaphor applied to database architecture. During low-load cycles ("sleep"), the database analyzes short-term memory (T0xN-B).
*   **The Consensus:** It compresses recurring patterns into "Archetypes".
*   **The Dissent:** Data that fits *no* archetype is treated as "Divergent Thought". Following the **10th Man Doctrine**, this data is protected, kept raw, and flagged as critical to prevent cognitive blindness to anomalies.

### 🅴 T0xN-E: The Event
**Status:** 🔴 Conceptual
The evolution of Data Streams for IoT. A mechanism to filter binary streams "on the fly" based on byte positioning, without full deserialization.

---

## 5. Standing on the Shoulders of Giants
This research builds upon:
*   **[TOON](https://github.com/toon-format/toon)** & **[TONL](https://github.com/tonl-dev/tonl)** (Inspiration for T0xN-A)
*   **[JSON-NTV](https://github.com/loco-philippe/NTV)** (Semantic Fidelity)
*   **[Redis](https://redis.io)** (The in-memory laboratory)

## 6. Contributing
This is an experimental project. We are looking for:
*   **Rust Developers** for the Redis Module.
*   **Data Scientists** for the Dreaming algorithms.

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.
