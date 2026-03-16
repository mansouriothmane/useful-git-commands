# 🧭 Guide for Attending a Presentation on MCP & Agentic AI  
*A beginner‑friendly introduction to help you follow technical discussions*

---

## 📌 1. Purpose of This Guide
This document prepares you to attend a presentation about:
- **MCP (Model Context Protocol)**
- **Agentic AI systems**
- **Technical choices in implementing AI agents**
- **Performance, correctness, latency, and token efficiency**

It gives you the essential vocabulary, concepts, diagrams (described in text), and hidden assumptions that experts often skip.

---

# 🧩 2. Core Concepts You Should Know

## 🤖 Large Language Models (LLMs)
Key terms you will hear:
- **Inference** — the model generating an output.
- **Context window** — how much text the model can process at once.
- **Tokens** — the units of text the model reads/writes.
- **Prompt** — the input you give the model.

### Why tokens matter
- More tokens → higher cost  
- More tokens → slower responses  
- Too many tokens → model loses focus  

---

## 🧠 Agentic AI (AI Agents)
An *agent* is an LLM that can:
- understand a goal  
- plan steps  
- call tools or APIs  
- observe results  
- iterate until the task is done  

### Typical Agent Lifecycle (you may see this diagram)

```memaid
Goal → Planning → Tool Call → Observation → Reflection → Next Action → Final Answer
```

Common frameworks or patterns:
- **ReAct** (Reason + Act)
- **Plan-and-Execute**
- **Chain-of-Thought**
- **Self-Reflection / Self-Correction**

---

## 🔌 MCP (Model Context Protocol)
MCP is a protocol that allows LLMs to interact with external tools in a structured way.

You will likely hear about:
- **Tool schemas** (JSON definitions of tool inputs/outputs)
- **Capabilities** (what tools the agent can use)
- **Context management**
- **Tool discovery**
- **Security boundaries**

Think of MCP as the “API layer” that lets an AI agent safely use external systems.

---

# 📐 3. Technical Terms You Will Likely Hear

## ⚙️ Performance Metrics
These often come with formulas.

### **Accuracy / Correctness**
How often the model gives the right answer.

### **Latency**
Time between request and response.  
Often broken down into:
- Model inference latency  
- Tool call latency  
- Network latency  

### **Throughput**
How many requests per second the system can handle.

### **Token Efficiency**
How many tokens are used to complete a task.  
Lower = cheaper, faster, often more reliable.

### **Hallucination Rate**
How often the model produces incorrect or invented information.

---

## 📊 LLM Evaluation Concepts
Expect mentions of:
- **Benchmarks** (MMLU, GSM8K, HumanEval)
- **Prompt engineering**
- **RAG (Retrieval-Augmented Generation)**
- **Guardrails**
- **Safety filters**

---

# 🧱 4. Architecture Topics That Often Come Up

Even if not in the draft, these topics frequently appear in MCP/agent discussions.

## 🏗️ System Architecture
Typical components:
- LLM  
- MCP server  
- Tools (APIs, databases, internal services)  
- Vector store (for RAG)  
- Orchestration layer (agent framework)  

## 🔐 Security & Permissions
Expect discussion about:
- sandboxing tools  
- limiting agent capabilities  
- authentication for tool calls  
- preventing harmful actions  

## 🧩 Tooling Ecosystem
Names you may hear:
- LangChain  
- LlamaIndex  
- OpenAI MCP  
- Vercel MCP  
- AutoGen  
- CrewAI  
- Semantic Kernel  

These are frameworks for building agentic systems.

---

# 🧠 5. Mathematical Concepts You Might See (Simplified)

You don’t need to compute anything — just understand the meaning.

### **Inference Complexity**
Often expressed like:

```
O(n · d)
```

Meaning: more tokens → more compute → more latency.

### **Accuracy**

```
Accuracy = correct outputs / total outputs
```

### **Latency Breakdown**

```
Total Latency = Model Latency + Tool Latency + Network Latency
```

### **Cost Estimation**

```
Cost = tokens used × price per token
```


---

# 🧠 6. Hidden Prerequisites Experts Assume You Know

## 🧩 JSON & Schemas
MCP tools are described using JSON schemas.  
They define:
- required inputs  
- output structure  
- types  

## 🧠 Embeddings
Vector representations of text used for:
- search  
- retrieval  
- similarity  

## 📚 RAG Pipelines
Retrieval-Augmented Generation:
1. Retrieve relevant documents  
2. Feed them to the LLM  
3. Improve accuracy  

## 🔄 Streaming
LLMs often stream tokens instead of sending the full answer at once.

---

# 🧭 7. Smart Questions You Can Ask
These make you sound engaged without needing deep expertise.

- “How does the MCP handle tool discovery and capability negotiation?”
- “What strategies are used to reduce token usage?”
- “How do you evaluate the agent’s reasoning quality?”
- “What guardrails prevent unsafe tool calls?”
- “How do you measure the impact of tool latency on overall performance?”

---

# 🌱 8. A Simple Mental Model
Think of the system as:

- **Brain** → the LLM  
- **Hands** → tools  
- **Nerves** → MCP  
- **Plans** → agentic reasoning  
- **Metrics** → accuracy, latency, cost  

If you keep this metaphor in mind, the entire presentation becomes easier to follow.
