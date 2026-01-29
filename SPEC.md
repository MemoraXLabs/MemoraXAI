# MemoraX Memory Layer — SPEC v0.2
### The memory layer for long-horizon intelligence

**Version:** 0.2  
**Date:** 29 January 2026  
**Status:** Conceptual specification (non-implementation)  
**License:** MIT  

**This specification extends SPEC v0.1**  
Original v0.1: SPEC-v0.1.md  

Core primitives and philosophy remain unchanged.  
SPEC v0.2 adds scope clarification, lifecycle semantics, governance boundaries, and reference use cases.

---

## 1. Purpose

MemoraX defines the memory layer required for long-horizon intelligence.

Modern AI systems are episodic.  
They act, respond, and reset.

Even with large context windows, retrieval systems, and agent frameworks, most systems fail to remain the same system over time.

Long-horizon intelligence requires something different:
- persistent identity
- continuity across executions
- compounding understanding

Storage remembers data.  
MemoraX remembers the system.

---

## 2. Position in the AI Stack

MemoraX occupies a distinct position in the AI stack.

- Models → reason  
- Tools → act  
- Storage → store data  
- **MemoraX → preserve identity across time**

Without this layer, intelligence fragments into isolated episodes.

---

## 3. Core Principle

**If the system restarts, is it still the same system?**

If the answer is “no”, the system lacks long-horizon memory.

MemoraX exists to make the answer “yes”.

---

## 4. Scope and Non-Goals

### 4.1 What MemoraX Is

MemoraX is:
- an architectural memory layer
- identity-preserving
- continuity-first
- model-agnostic
- compatible with agents, robotics, physical AI, and long-running systems

MemoraX governs what persists and how identity evolves over time.

### 4.2 What MemoraX Is Not

MemoraX is not:
- a language model
- an agent framework
- a vector database
- a retrieval pipeline
- a chat history store
- a personalization feature

MemoraX does not replace reasoning, retrieval, or storage.  
It defines the continuity layer between them.

---

## 5. Canonical Primitives

MemoraX defines three canonical primitives.

### 5.1 Identity

An **Identity** represents a single continuous intelligent system.

An identity:
- persists across executions and deployments
- anchors all memory operations
- remains stable as the system evolves

Identity is not a user.  
It is not an account.  
It is the continuous self of an AI system.

### 5.2 Memory Objects

All memory in MemoraX is represented as **Memory Objects**.

A memory object contains:
- `memory_id`
- `identity_id`
- `content`
- `provenance`
- `confidence` (0.0–1.0)
- `created_at`
- `updated_at`

Memory objects are not immutable logs.  
They are mutable components of an evolving system.

### 5.3 Continuity Graph

MemoraX organizes memory as a **continuity graph**.

The graph represents:
- what the system knows
- how that knowledge was learned
- how understanding changes over time
- how conflicts are resolved into coherent state

Memory is not only retrieved.  
It shapes future behavior.

---

## 6. Memory Lifecycle Semantics

Memory persistence follows explicit lifecycle stages.

1. Context — transient input  
2. Candidate Memory — eligible for persistence  
3. Committed Memory — promoted to long-horizon state  
4. Updated Memory — modified through experience  
5. Merged Memory — conflict-resolved coherent state  
6. Deprecated Memory — retained but down-weighted  
7. Archived Memory — no longer behavior-shaping

Context → Candidate → [Governance checks (confidence, drift, policy)] → Committed → Updated or Merged → Deprecated → Archived

This prevents uncontrolled accumulation, drift, and silent identity corruption.

---

## 7. Core Operations

All operations occur within identity context.

- **WRITE** — propose new memory  
- **UPDATE** — modify existing memory  
- **MERGE** — resolve conflicts  
- **READ** — retrieve relative to full history  
- **DEPRECATE** — reduce influence without deletion  
- **AUDIT** — trace provenance and evolution  

Deletion is a governance event, not a default behavior.

---

## 8. Memory Governance

Governance is a first-class concern.

Long-horizon systems must define:
- what is allowed to persist
- how memory evolves
- how drift is detected
- how accountability is enforced

Without governance, persistent memory leads to drift, bias accumulation, and identity degradation.

---

## 9. Relationship to Retrieval and Storage

Retrieval systems operate episodically.  
MemoraX operates continuously.

Retrieval answers questions.  
MemoraX shapes behavior.

MemoraX complements storage and retrieval by governing what survives beyond them.

---

## 10. Reference Use Cases

- **Long-running AI agents** that retain preferences and improve workflows across months without resetting identity  
- **Customer support systems** that maintain consistent policy interpretation and customer history across interactions  
- **Physical AI and robotics** that preserve operational identity across deployments and environments  
- **Human–AI collaboration** that co-evolves shared understanding over long periods without repeated re-initialization

---

## 11. Relationship to Implementations

Existing systems implement memory mechanisms.

MemoraX defines the architectural abstraction that makes memory a first-class layer for long-horizon intelligence.

---

## 12. Status

This specification is:
- conceptual
- vendor-neutral
- implementation-agnostic

It defines the memory layer required for identity-preserving, long-horizon intelligent systems.

---

## Closing Statement

The future remembers.  
Intelligence compounds.  
It starts with MemoraX.
