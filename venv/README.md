# Use python built-in venv module to create a virtual environment

Basic workflow for using `venv`:
1. `python -m venv .venv`
2. `source .venv/bin/activate` (macOS/Linux)
3. edit `pyproject.toml` to add dependencies
4. `pip install -e .`

---

- Create a virtual environment named `venv`
```bash
python -m venv .venv
```

- Activate the virtual environment
```bash
source .venv/bin/activate  # On macOS/Linux
.venv\Scripts\activate  # On Windows
source .venv/Scripts/activate  # On Windows powershell
```

- Install Flask in the virtual environment
```bash
pip install Flask
```

- Run the application using `python main.py`
```bash
python main.py
```

- Export the packages installed in the virtual environment to a requirements file
```bash
pip freeze > requirements.txt
```

It will generate a `requirements.txt` file that lists all the packages installed in your virtual environment, including their versions.

```text
blinker==1.9.0
click==8.2.1
colorama==0.4.6
Flask==3.1.1
itsdangerous==2.2.0
Jinja2==3.1.6
MarkupSafe==3.0.2
Werkzeug==3.1.3
```

- `pyproject.toml`:

However, using `freeze` will include all packages, including those that are not directly used in your project. To avoid this, you can use `pyproject.toml` to manage your dependencies more cleanly.

- install environment:
```bash
pip install -e .
```