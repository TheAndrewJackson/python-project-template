# {{cookiecutter.project_name}}

# Setup
## Install dependencies
```sh
poetry install
```

## Setup pre-commit and pre-push hooks
```sh
poetry run pre-commit install -t pre-commit
poetry run pre-commit install -t pre-push
```