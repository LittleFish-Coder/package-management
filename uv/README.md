# Use `uv` to create a virtual environment

Basic workflow for using `uv`:
1. `uv add <package>`

---

- Install packages using `uv`:
```bash
uv add flask
```

This command will automatically create a virtual environment and add the specified package to `pyproject.toml`.

- Sync the virtual environment(install dependencies from `pyproject.toml`):
```bash
uv sync
```

- Run the application:
```bash
source .venv/bin/activate  # On macOS/Linux
.venv\Scripts\activate  # On Windows
source .venv/Scripts/activate  # On Windows powershell

python main.py
```

- Directly run the application without activating the virtual environment:
```bash
uv run main.py
```