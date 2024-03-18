# Python Project Template Cookiecutter

This projects goal is to kick start the process of creating a best practices python project.
It utilizes [cookiecutter](https://github.com/audreyr/cookiecutter) to copy the template.

## Features

- Formatting, import sorting, and linting with [ruff](https://github.com/astral-sh/ruff)
- Testing with [pytest](https://docs.pytest.org/en/latest/)
- Code coverage with [pytest-cov](https://pytest-cov.readthedocs.io/en/latest/index.html)
- Static type linting with [mypy](http://mypy-lang.org/)
- Git hooks that run all the above with [pre-commit](https://pre-commit.com/)
- Runtime enforced static type checking and data validation with [pydantic](https://pydantic-docs.helpmanual.io/)
    - This works by implementing pydantic based models.
    - This also includes enhanced mypy linting with the pydantic-mypy plugin

## Quickstart

```sh
# Install pipx if cookiecutter isn't installed
python3 -m pip install --user pipx
# You may need to manually add the script directory to PATH
# pip should tell you the install location
# Restart terminal
pipx ensurepath
# Restart terminal again

# Install cookiecutter with pipx
pipx install cookiecutter

# Use cookiecutter to create project from this template
cookiecutter gh:theandrewjackson/python-project-template

# Enter project directory
cd <repo_name>

# Initialise git repo
git init

# Install uv
curl -LsSf https://astral.sh/uv/install.sh | sh

## Create and activate virtualenv
uv venv
source .venv/bin/active

# Install dependencies
uv pip install -r pyproject.toml --all-extras

# Setup pre-commit and pre-push hooks
pre-commit install -t pre-commit
pre-commit install -t pre-push
```
