# Python Project Template Cookiecutter

This projects goal is to kick start the process of creating a best practices python project.
It utilizes [cookiecutter](https://github.com/audreyr/cookiecutter) to copy the template.


## TODO
- Update pytest to use pyproject.toml
- Add mypy configuration and link pydantic with it


## Features

- Formatting with [black](https://github.com/psf/black)
- Import sorting with [isort](https://github.com/timothycrosley/isort)
- Testing with [pytest](https://docs.pytest.org/en/latest/)
- Code coverage with [pytest-cov](https://pytest-cov.readthedocs.io/en/latest/index.html)
- Static typing with [mypy](http://mypy-lang.org/)
- Linting with [flake8](http://flake8.pycqa.org/en/latest/)
- Git hooks that run all the above with [pre-commit](https://pre-commit.com/)

## Quickstart

Install Poetry: [instructions](https://python-poetry.org/docs/#installation)

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

# Configure Poetry to install the virtual env in your project directory.
# This allows editors like pycharm and vscode to see what packages are installed. Poetry defaults to false.
poetry config virtualenvs.in-project true

# Set the target python version in the pyproject.toml file.
# Put the dependency under the [tool.poetry.dependencies] section.
# It's set to python 3.8 by default.
python = "^3.8"


# Install dependencies
poetry install

# Setup pre-commit and pre-push hooks
poetry run pre-commit install -t pre-commit
poetry run pre-commit install -t pre-push
```
