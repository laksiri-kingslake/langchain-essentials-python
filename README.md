## LangChain Essentials: LangChain Official Guide - Python

### Setup Environment
```bash
# Initialize uv
uv init

# Install dependencies
uv add ipykernel 
```
### Lession 1: Fast Agent

1. Install dependency packages

```bash
uv add langchain
uv add langchain-openai
uv add python-dotenv
uv add langchain_community
uv add langchain-ollama

touch utils.py
```

2. Relevant .ipynb file: L01-fast-agent.ipynb

### Try with LangGraph Studio

1. Create agent (sql_agent.py)

2. Create langgraph config (langgraph.json)

3. Install langgraph cli
```bash
uv pip install --upgrade "langgraph-cli[inmem]"
```

4. Make sure agent works - no need to keep it running while using langgraph studio
```bash
uv run sql_agent.py

# it should not give errors
```

5. Run langgraph studio
```bash
uv run langgraph dev
```

### Useful debug options
```bash
# should we want to findout the source of a function
import inspect
print(inspect.getsourcefile(doublecheck_env))

# filter all pip packages with langchain name
uv pip list | grep langchain

```

### Reference
1. [Quickstart: Langchain Essentials - Python](https://academy.langchain.com/courses/langchain-essentials-python)