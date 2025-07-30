# Python Package Management Comparison

This repository demonstrates two approaches to Python package management: traditional `venv` vs modern `uv`.

## 📁 Repository Structure

```
package-management/
├── venv/          # Traditional approach with built-in venv
│   ├── README.md  # 6-step tutorial
│   ├── main.py    # Sample Flask application
│   └── requirements.txt  # Generated dependency file
│
├── uv/            # Modern approach with uv tool
│   ├── README.md  # 3-step tutorial  
│   ├── main.py    # Sample Flask application
│   └── pyproject.toml    # Auto-generated project config
│
└── README.md      # This overview
```

## 🚀 Quick Comparison

### Traditional Approach (venv/)
```bash
python -m venv .venv
source .venv/bin/activate
pip install Flask
python main.py
pip freeze > requirements.txt
```

### Modern Approach (uv/)  
```bash
uv init --python 3.11
uv add Flask
uv run main.py
```

## 📊 Step-by-Step Comparison

| Step | Traditional (venv) | Modern (uv) |
|------|-------------------|-------------|
| **Initialize** | - | `uv init --python 3.11` |
| **Create Environment** | `python -m venv .venv` | *automatic* |
| **Activate** | `source .venv/bin/activate` | *not needed* |
| **Install Package** | `pip install Flask` | `uv add Flask` |
| **Run Application** | `python main.py` | `uv run main.py` |
| **Save Dependencies** | `pip freeze > requirements.txt` | *automatic* |
| **Deactivate** | `deactivate` | *not needed* |
| **Total Steps** | **6 steps** | **3 steps** |

## 📚 Tutorials

- **[venv/ Tutorial](./venv/README.md)** - Traditional 6-step workflow
- **[uv/ Tutorial](./uv/README.md)** - Modern 3-step workflow

## 🎯 Which Should You Use?

**Use venv if:**
- Learning Python fundamentals
- Working on legacy projects
- Team uses traditional tools

**Use uv if:**
- Want speed and convenience  
- Starting new projects
- Want modern best practices
- Need Python version management

---