# Google Agent Development Kit (ADK) Overview

The **Agent Development Kit (ADK)** is Google's open-source framework designed to build, test, evaluate, and deploy production-ready AI agents and multi-agent systems at scale. Unlike simple prompt-engineering wrappers, ADK brings traditional software engineering principles—such as modularity, unit testing, telemetry, and structured orchestration—to agentic AI development.

---

## Key Overview & Features

| Attribute | Details |
| :--- | :--- |
| **Framework Name** | Google Agent Development Kit (ADK) |
| **Primary Goal** | Streamline full-stack development of single and multi-agent AI systems from prototype to enterprise deployment. |
| **Multi-Language Support** | Available in **Python**, **TypeScript**, **Go**, **Java**, and **Kotlin**. |
| **Model Ecosystem** | Deeply integrated with **Google Gemini** and **Vertex AI**, while supporting third-party models via **LiteLLM**. |
| **Multi-Agent Orchestration** | Native support for sequential, parallel, loop workflows, as well as dynamic LLM-driven agent routing and delegation. |
| **Multimodal Capabilities** | Features built-in bidirectional audio and video streaming for natural real-time human-agent interactions. |
| **Tool-as-Agent Abstraction** | Enables developers to encapsulate APIs, external tools, or other agents as callable tools, promoting modular reuse. |
| **Evaluation & Testing** | Includes a built-in evaluation harness (`AgentEvaluator`) for scenario-driven testing, tracking execution trajectories, and benchmarking performance. |
| **Deployment Options** | Flexible deployment: local developer CLI/UI, Docker containers, Cloud Run, GKE, or fully managed enterprise runtime on Vertex AI. |

---

## Key Feature Breakdown vs. Usability / Use Cases

| Core Component / Feature | Capabilities | Typical Usability & Use Cases |
| :--- | :--- | :--- |
| **Single-Purpose Agents** | Lightweight, focused agents designed for execution of dedicated task primitives. | Calendar fetching, currency conversion, document summarization, or single API interactions. |
| **Hierarchical Multi-Agent Systems** | Orchestration patterns where a parent/router agent delegates tasks to specialized sub-agents. | Complex customer support automation, enterprise knowledge synthesis, and multi-step research. |
| **Flexible Orchestrators** | Deterministic pipeline controls (`Sequential`, `Parallel`, `Loop`) mixed with dynamic LLM routing. | Order processing pipelines, data transformation workflows, and automated triage systems. |
| **Tooling & Connectivity Ecosystem** | Pre-built and custom adapters connecting agents to databases, web search, enterprise tools, and APIs. | Connecting AI agents directly to CRM databases, enterprise file stores, and cloud infrastructure. |
| **Local Dev & Debugger UI** | Interactive local developer CLI and web workbench for rapid scaffolding, state inspection, and step-by-step debugging. | Fast prototyping, inspecting intermediate agent reasoning steps, and local session testing. |
| **Built-in Telemetry & Evaluation** | Native logging, tracing, metrics tracking, and automated evaluation against benchmark test datasets. | Regression testing before release, monitoring token usage, and evaluating agent trajectory correctness. |

---

## Quick Example (Python)

```python
from google.adk import Agent
from google.adk.tools import google_search

# Define a single-purpose research agent
researcher = Agent(
    name="researcher_agent",
    model="gemini-2.5-flash",
    instructions="You are a helpful research assistant. Use Google Search to verify facts.",
    tools=[google_search]
)

# Execute query
response = researcher.run("Summarize the latest developments in AI agent frameworks.")
print(response.text)



Gemini is AI and can make mistakes.

# Google Agent Development Kit (ADK) Overview

The **Agent Development Kit (ADK)** is Google's open-source framework designed to build, test, evaluate, and deploy production-ready AI agents and multi-agent systems at scale. Unlike simple prompt-engineering wrappers, ADK brings traditional software engineering principles—such as modularity, unit testing, telemetry, and structured orchestration—to agentic AI development.

---

## Key Overview & Features

| Attribute | Details |
| :--- | :--- |
| **Framework Name** | Google Agent Development Kit (ADK) |
| **Primary Goal** | Streamline full-stack development of single and multi-agent AI systems from prototype to enterprise deployment. |
| **Multi-Language Support** | Available in **Python**, **TypeScript**, **Go**, **Java**, and **Kotlin**. |
| **Model Ecosystem** | Deeply integrated with **Google Gemini** and **Vertex AI**, while supporting third-party models via **LiteLLM**. |
| **Multi-Agent Orchestration** | Native support for sequential, parallel, loop workflows, as well as dynamic LLM-driven agent routing and delegation. |
| **Multimodal Capabilities** | Features built-in bidirectional audio and video streaming for natural real-time human-agent interactions. |
| **Tool-as-Agent Abstraction** | Enables developers to encapsulate APIs, external tools, or other agents as callable tools, promoting modular reuse. |
| **Evaluation & Testing** | Includes a built-in evaluation harness (`AgentEvaluator`) for scenario-driven testing, tracking execution trajectories, and benchmarking performance. |
| **Deployment Options** | Flexible deployment: local developer CLI/UI, Docker containers, Cloud Run, GKE, or fully managed enterprise runtime on Vertex AI. |

---

## Key Feature Breakdown vs. Usability / Use Cases

| Core Component / Feature | Capabilities | Typical Usability & Use Cases |
| :--- | :--- | :--- |
| **Single-Purpose Agents** | Lightweight, focused agents designed for execution of dedicated task primitives. | Calendar fetching, currency conversion, document summarization, or single API interactions. |
| **Hierarchical Multi-Agent Systems** | Orchestration patterns where a parent/router agent delegates tasks to specialized sub-agents. | Complex customer support automation, enterprise knowledge synthesis, and multi-step research. |
| **Flexible Orchestrators** | Deterministic pipeline controls (`Sequential`, `Parallel`, `Loop`) mixed with dynamic LLM routing. | Order processing pipelines, data transformation workflows, and automated triage systems. |
| **Tooling & Connectivity Ecosystem** | Pre-built and custom adapters connecting agents to databases, web search, enterprise tools, and APIs. | Connecting AI agents directly to CRM databases, enterprise file stores, and cloud infrastructure. |
| **Local Dev & Debugger UI** | Interactive local developer CLI and web workbench for rapid scaffolding, state inspection, and step-by-step debugging. | Fast prototyping, inspecting intermediate agent reasoning steps, and local session testing. |
| **Built-in Telemetry & Evaluation** | Native logging, tracing, metrics tracking, and automated evaluation against benchmark test datasets. | Regression testing before release, monitoring token usage, and evaluating agent trajectory correctness. |

---

## Quick Example (Python)

```python
from google.adk import Agent
from google.adk.tools import google_search

# Define a single-purpose research agent
researcher = Agent(
    name="researcher_agent",
    model="gemini-2.5-flash",
    instructions="You are a helpful research assistant. Use Google Search to verify facts.",
    tools=[google_search]
)

# Execute query
response = researcher.run("Summarize the latest developments in AI agent frameworks.")
print(response.text)
