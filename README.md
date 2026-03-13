# Reflection Agent using LangGraph

## Overview

This project implements a **Reflection Agent architecture** using **LangGraph and LangChain**.
The agent generates a response, critiques it, and iteratively improves the output through a reflection loop.

The workflow simulates how humans refine their work through **self-evaluation and revision**, enabling better responses from large language models.

---

## Architecture

The system follows a simple **Generate → Reflect → Improve** loop:

1. **Generate Node**

   * Produces the initial response from the user prompt.

2. **Reflect Node**

   * Critiques the generated response and suggests improvements.

3. **Iteration Loop**

   * The improved feedback is sent back to the generation step.

This continues until the stopping condition is reached.

```
User Input
    ↓
Generate Response
    ↓
Reflect / Critique
    ↓
Improve Response
    ↓
Repeat until limit
```

---

## Tech Stack

* Python
* LangChain
* LangGraph
* Anthropic Claude API
* LangSmith (for tracing and debugging)

---

## Project Structure

```
reflection-agent
│
├── main.py            # LangGraph workflow and nodes
├── chains.py          # LLM chains for generation and reflection
├── .env               # API keys
├── pyproject.toml     # Poetry project configuration
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/poorviyadav04/reflection_agent.git
cd reflection_agent
```

Install dependencies using Poetry:

```bash
poetry install
```

Activate the environment:

```bash
poetry shell
```

---

## Environment Variables

Create a `.env` file and add your API key:

```
ANTHROPIC_API_KEY=your_api_key_here
LANGCHAIN_API_KEY=your_langsmith_key
```

---

## Run the Project

Execute the agent:

```bash
python main.py
```

The agent will generate an improved version of the input prompt using the reflection loop.

---

## Example Use Case

Input prompt:

```
Make this tweet better:
@LangChainAI

The new tool calling feature is underrated.
```

The agent will iteratively improve the tweet through reflection and revision.

---

## Learning Outcomes

Through this project, I explored:

* Building **agent workflows using LangGraph**
* Implementing **reflection-based reasoning**
* Creating **iterative LLM pipelines**
* Debugging agents using **LangSmith tracing**

---

## Future Improvements

* Add memory to the agent
* Introduce evaluation metrics
* Enable multi-agent collaboration
* Deploy as an API or web app

---

## Author

**Poorvi Yadav**
