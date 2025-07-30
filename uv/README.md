# Modern Python Package Management with uv

## Step-by-Step Tutorial

### 1. Initialize project with Python version
```bash
uv init --python 3.11
# or just: uv init
```
This creates `pyproject.toml` with specified Python version.

### 2. Install packages
```bash
uv add Flask
```
This automatically:
- Creates `.venv` virtual environment with specified Python version
- Installs Flask
- Updates `pyproject.toml`

### 3. Run application
```bash
uv run main.py
```

That's it! No activation or deactivation needed.

## For Future Package Installation

```bash
# Install new package
uv add package-name

# Run your application
uv run main.py
```

## Setting up from existing pyproject.toml

```bash
uv sync
uv run main.py
```

## Why uv is simpler

- ✅ No manual virtual environment creation
- ✅ No activation/deactivation needed  
- ✅ Dependencies saved automatically to `pyproject.toml`
- ✅ 10-100x faster than pip