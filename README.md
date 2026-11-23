# PLIDOagent

Course materials for the "Agentic AI" course, built around a running example: a philosophy
professor who writes an assignment, has it answered by several LLMs, and grades the results.

## Course structure

* [`Part_0_introduction.ipynb`](Part_0_introduction.ipynb) — Part 0: welcome, roadmap, and core concepts of Large Language Models.
* [`Part_1_philosopher.ipynb`](Part_1_philosopher.ipynb) — Part 1: setting up the working environment (uv, Ollama, API keys for Rennes, ILaaS, and Google Gemini) and querying different LLM servers through a common OpenAI-compatible API.
* [`Part_2_network_professor.ipynb`](Part_2_network_professor.ipynb) — Part 2: concurrent LLMs with `asyncio`, push notifications, chat interface with Gradio, and chaining agents together.
* [`Part_3_tokenization.ipynb`](Part_3_tokenization.ipynb) — Part 3: tokens, Byte-Pair Encoding (BPE), control tokens, and the context window.
* [`Part_4_embeddings.ipynb`](Part_4_embeddings.ipynb) — Part 4: vector embeddings, cosine distance, word analogies, neural network weights, and quantization.
* [`Part_5_nobel_prize.ipynb`](Part_5_nobel_prize.ipynb) — Part 5: frozen knowledge cutoffs, live tools, and agent tool-calling decisions.
* [`Part_6_taf_advisor.ipynb`](Part_6_taf_advisor.ipynb) — Part 6: Model Context Protocol (MCP) clients, web scraping, and persistent memory.
* [`Part_7_RAG_time.ipynb`](Part_7_RAG_time.ipynb) — Part 7: sentence embeddings, mean-pooling, self-attention, and PyTorch tensors.
* [`Part_8_chunk_happens.ipynb`](Part_8_chunk_happens.ipynb) — Part 8: RAG document chunking, indexing the 218-page IoT book, LangChain, and Chroma vector database.
* [`Part_9_reality_bites.ipynb`](Part_9_reality_bites.ipynb) — Part 9: real-world web corpora, PASS fiches extraction, and OpenAlex publication profiling.
* [`Part_10_mcp.ipynb`](Part_10_mcp.ipynb) — Part 10: MCP vs. code reasoning (`smolagents` `CodeAgent`), querying Linky smart meter telemetry in MongoDB, electric vehicle charging detection, and token explosion benchmarks.
* [`Appendix_models.ipynb`](Appendix_models.ipynb) — Appendix: auto-updating reference of all LLM models used across the course.

## Do I need uv to open the notebooks?

No. A `.ipynb` file is plain text (JSON), so you can **read** it without installing anything:

* on GitHub/GitLab it renders directly in the browser,
* in VS Code, the built-in notebook viewer displays it even before any Python environment is set up.

You only need **uv** (and a Python environment) to actually **run** the code cells and query the
LLMs. The exact steps are given inside `Part_1_philosopher.ipynb` (section "Working Environment");
in short:

1. Install uv: `curl -LsSf https://astral.sh/uv/install.sh | sh`
2. `uv self update` to check the installation
3. `uv sync` to create the `.venv` and install the dependencies listed in `pyproject.toml`
4. In VS Code / Jupyter, select the resulting virtual environment as the notebook's kernel
5. Create a `.env` file at the root of the project with your API keys (`RENNES_API_KEY`,
   `ILAAS_API_KEY`, `GOOGLE_API_KEY`, ...) — see the notebook for where to obtain them
