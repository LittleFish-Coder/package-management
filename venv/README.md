# Traditional Python Virtual Environment with venv

## Step-by-Step Tutorial

### 1. Create virtual environment
```bash
python -m venv .venv
```

### 2. Activate virtual environment
```bash
source .venv/bin/activate          # macOS/Linux
# .venv\Scripts\activate           # Windows
```
You'll see `(.venv)` in your terminal prompt.

### 3. Install packages
```bash
pip install Flask
```

### 4. Run application
```bash
python main.py
```

### 5. Generate requirements.txt
```bash
pip freeze > requirements.txt
```

### 6. Deactivate environment
```bash
deactivate
```

## For Future Package Installation

```bash
# Activate environment
source .venv/bin/activate

# Install new package
pip install package-name

# Update requirements.txt
pip freeze > requirements.txt

# Deactivate when done
deactivate
```

## Setting up from existing requirements.txt

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python main.py
```