# {{cookiecutter.project_name}}

# Setup
## Install uv
```sh
curl -LsSf https://astral.sh/uv/install.sh | sh
```

## Create and activate virtualenv
```sh
uv venv
source .venv/bin/active
```

## Install dependencies
```sh
uv pip install -r pyproject.toml --all-extras
```

## Setup pre-commit and pre-push hooks
```sh
git init #init git repo if you haven't already
pre-commit install -t pre-commit
pre-commit install -t pre-push
```