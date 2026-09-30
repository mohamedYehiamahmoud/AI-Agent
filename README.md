# Local Multi-Agent Data Science Mentor

A small educational project demonstrating a multi-agent workflow built with **CrewAI** and a locally hosted **Llama 3** model through **Ollama**.

The workflow uses two agents to turn a broad data-science topic into a structured learning roadmap.

## Architecture

```text
                     +----------------+
Topic -------------> | Mentor Agent   |
                     +-------+--------+
                             |
                             v
                     Gather information
                             |
                             v
                     +-----------------------+
                     | Content Strategist    |
                     +-----------+-----------+
                                 |
                                 v
                         Structured roadmap
```

### Agents

**Mentor**

Collects relevant information about the requested topic and provides the knowledge used by the workflow.

**Tech Content Strategist**

Transforms the collected information into a clearer, more useful roadmap.

## Stack

- Python
- CrewAI
- LangChain Community
- Ollama
- Llama 3
- Jupyter Notebook

## Run Locally

### 1. Install Ollama

Install Ollama from the official documentation:

https://ollama.com/

Then pull the model:

```bash
ollama pull llama3
```

### 2. Install Python dependencies

```bash
pip install crewai langchain-community jupyter
```

### 3. Run the notebook

Open `crewai.ipynb` in Jupyter:

```bash
jupyter notebook
```

Run the cells in order.

## What This Project Demonstrates

- defining specialized AI agents
- assigning goals and backstories to agents
- composing multiple agents into a sequential workflow
- using a local LLM instead of a hosted API
- separating research and content-generation responsibilities

## Limitations

This is an educational prototype rather than a production agent system. The current workflow uses a simple sequential process and does not include production concerns such as evaluation, tracing, retries, persistent state, or isolated tool execution.

## License

MIT
