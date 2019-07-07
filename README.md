# flask-api-template

WIP: Flask API server template project

## Requirements

- python 3.7
- pipenv
- direnv

## Installtion

Install a specified Python version and setup a virtual enviornment

```bash
pipenv install --python=3.7
pipenv install -e .
```

direnv

```bash
$ echo 'layout_pipenv' > .envrc && direnv allow
direnv: loading .envrc
direnv: export +PIPENV_ACTIVE +VIRTUAL_ENV -DYLD_LIBRARY_PATH ~PATH
$ python --version
Python 3.7.3
```
