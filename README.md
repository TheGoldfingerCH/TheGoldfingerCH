# Hey, I'm Nicolas 👋

**Data Science & AI graduate from Le Wagon | Building practical AI and data projects in public 🚀**

> I am specializing in AI while keeping strong data foundations: clear problem framing, measurable results, and honest reporting.

<p align="left">
  <a href="https://www.python.org"><img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"></a>
  <a href="https://pandas.pydata.org"><img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"></a>
  <a href="https://numpy.org"><img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"></a>
  <a href="https://scikit-learn.org"><img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn"></a>
  <a href="https://xgboost.readthedocs.io"><img src="https://img.shields.io/badge/XGBoost-EC6B23?style=for-the-badge&logo=xgboost&logoColor=white" alt="XGBoost"></a>
  <a href="https://facebook.github.io/prophet/"><img src="https://img.shields.io/badge/Prophet-0A66C2?style=for-the-badge&logo=plotly&logoColor=white" alt="Prophet"></a>
  <a href="https://huggingface.co/GoldfingerCH"><img src="https://img.shields.io/badge/Hugging%20Face-FFCC4D?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face"></a>
  <a href="https://www.tensorflow.org"><img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow"></a>
  <a href="https://www.docker.com"><img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"></a>
  <a href="https://streamlit.io"><img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit"></a>
  <a href="https://jupyter.org"><img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter"></a>
  <a href="https://modelcontextprotocol.io"><img src="https://img.shields.io/badge/MCP-000000?style=for-the-badge&logo=anthropic&logoColor=white" alt="MCP"></a>
  <a href="https://github.com/NousResearch/hermes-agent"><img src="https://img.shields.io/badge/Hermes-6B46C1?style=for-the-badge&logo=ghost&logoColor=white" alt="Hermes"></a>
</p>

## 🔥 Currently Building

- Local LLM serving on NVIDIA DGX Spark: NVFP4 quantization and vLLM packaging
- Bilingual (FR/EN) refusal evals to measure LLM behaviour after weight-space edits
- An AI-focused public portfolio with clean, reproducible, recruiter-friendly projects

## 🎯 Current Focus

- 🤖 Going deeper into **AI** (ML + GenAI workflows, model compression, evals)
- 📊 Strengthening core **Data Science** skills (EDA, modeling, evaluation, storytelling)
- 🧱 Building a clean, recruiter-friendly GitHub + [Hugging Face](https://huggingface.co/GoldfingerCH) presence

## 🏆 Highlighted Projects

### 1) Qwen3.8-27B NVFP4
- **Problem:** Serve a 27B Qwen3.8 checkpoint efficiently on NVIDIA Blackwell / DGX Spark (GB10).
- **Approach:** Weight-space edit (abliteration on layers 18–51, not a fine-tune), then oneshot NVFP4 quantization with `llm-compressor` (`compressed-tensors`, ~18 GB) for vLLM.
- **Stack:** Qwen3.8, NVFP4, llm-compressor, vLLM, DGX Spark
- **Result:** Public Hugging Face checkpoint aimed at local Spark inference (context up to 262k, FP8 KV cache).
- **Model:** https://huggingface.co/GoldfingerCH/Qwen3.8-27B-abliterated-NVFP4

### 2) Éval refus FR
- **Problem:** Measure refusal vs compliance after abliteration, in French as well as English.
- **Approach:** Bilingual eval set: French translation of user prompts (GX10 qwen-coder, translate-only), Qwen3Guard labels, no assistant completions — not a fine-tune corpus.
- **Stack:** Hugging Face Datasets, FR/EN, Qwen3Guard labels
- **Result:** Deduplicated research eval published on Hugging Face.
- **Dataset:** https://huggingface.co/datasets/GoldfingerCH/qwen38-27B-abliterated-refusal-eval-fr

### 3) AI_for_Finance
- **Problem:** Build a minimal and reusable finance-oriented ML prediction service.
- **Approach:** Expose a prediction API with FastAPI and package the project for local and cloud deployment.
- **Stack:** Python, FastAPI, Docker, Jupyter Notebook
- **Result:** Public service deployed with documented endpoints (`/` and `/predict`) and Swagger docs.
- **Repo:** https://github.com/TheGoldfingerCH/AI_for_Finance

### 4) llm-code-bench
- **Problem:** Measure how reliably LLMs can recall specific code sections when given large source files as context.
- **Approach:** Build a CLI benchmark that embeds JS/Python source files in the context window, asks models to reproduce named functions verbatim, and scores results line-by-line with LCS alignment.
- **Stack:** Python, Plotly, OpenAI-compatible API (Ollama, LM Studio, OpenAI…)
- **Result:** Modular benchmark framework with automated scoring and comparative dashboards across models and corpus sizes.
- **Repo:** https://github.com/TheGoldfingerCH/llm-code-bench

### 5) mcp-imap
- **Problem:** AI assistants like Hermes or Claude Desktop have no native access to email — reading, searching, and sending mails requires leaving the chat entirely.
- **Approach:** Build a zero-dependency MCP server using Python's built-in `imaplib` and `smtplib` — no third-party packages, no supply chain risk, works with any IMAP/SMTP provider.
- **Stack:** Python (stdlib only), MCP protocol, IMAP/SMTP
- **Result:** A drop-in MCP tool giving any AI assistant (Hermes, Claude Desktop, Cursor) full email access — list, read, search, send, move — in a single 200-line file.
- **Repo:** https://github.com/TheGoldfingerCH/mcp-imap

## 🧠 How I Build

- Start from a clear real-world problem
- Compare baseline vs improved approaches
- Document assumptions, trade-offs, and limitations
- Prioritize reproducibility (clear README, setup, project structure)

## 🛠 Tech Stack

- **Languages:** Python, SQL
- **Data:** Pandas, NumPy, Matplotlib, Seaborn
- **ML/AI:** scikit-learn, XGBoost, Linear Regression, Prophet, RNN, Hugging Face, TensorFlow, vLLM
- **Tools:** Git, Jupyter, Docker, Streamlit, llm-compressor

## 📈 Profile Goals (Next 90 Days)

- Publish 3 strong Data/AI repositories with polished READMEs
- Show measurable progress over time (iterations > one-shot demos)
- Document limitations honestly and propose realistic next steps

## 🎓 Background

- Data Science & AI Bootcamp - **Le Wagon**
- Continuous learning through hands-on projects and open sharing

## 💼 Open To

Junior Data Scientist, ML/AI internship, or entry-level Data/AI roles.  
Also open to collaboration on practical AI/data projects.

## 📫 Let's Connect

- Portfolio: [allrun.ch](https://allrun.ch)
- Hugging Face: [GoldfingerCH](https://huggingface.co/GoldfingerCH)
- LinkedIn: [nicolas-geng](https://www.linkedin.com/in/nicolas-geng/)
- Email: [contact@allrun.ch](mailto:contact@allrun.ch)
