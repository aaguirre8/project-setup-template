# project-setup-template
This is a general template to setup new projects

## Setup Project

1. Create and source virtual env

```bash
```
python -m venv ProjectEnv
ProjectEnv/Scripts/activate.bat

2. Create scaffold

```bash
touch Makefile && touch requirements.txt && touch hello.py && touch test_hello.py
```

3. Populate Makefile

```bash
install:
    pip install --upgrade pip &&\\
        pip install -r requirements.txt

test:
    python -m pytest -vv --cov=hello --cov=hellocli test_hello.py

lint:
    pylint --disable==R,C hello.py hellocli.py

all: install lint test
```



