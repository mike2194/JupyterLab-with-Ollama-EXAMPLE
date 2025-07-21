# Example [JupyterLab](https://jupyter.org/) environment with [Ollama](https://ollama.com/)

## Jupyter Setup

### for python virtual-env, make use of [uv](https://docs.astral.sh/uv/getting-started/installation/)

- `uv init lockout-tagout-exercise.python`
- `uv venv`
- add packages: jupyterlab
  `uv add jupyterlab jupyter-ai`
- add packages: for model providers
  `uv add langchain-ollama langchain-openai huggingface_hub ipywidgets pillow`
- activate venv
  `source .venv/bin/activate`
- start JupyterLab
  `jupyterlab`
  or, to be explicit:
  `./.venv/bin/python -m jupyterlab`

+ NOTE:
  if you see errors during startup about missing packages, you may need to add them (as i did, even though jupyterlab worked fine from system python):
    ```
    uv add jupyter_server_fileid jupyter_server_ydoc nbclassic notebook`
    deactivate
    source .venv/bin/activate
    jupyter-lab
    ```


