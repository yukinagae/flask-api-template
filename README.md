# flask-api-template

WIP: Flask API server template project

## Requirements

- python 3.7
- pipenv
- direnv

(optional)

- Docker
- docker-compose

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

## Start server

### On local

```bash
# MEMO: export and `flask run` seem to be unnecessary for flask-restful api
# export FLASK_APP=main.py
# export FLASK_DEBUG=1
# flask run
python main.py
```

### On docker

```bash
docker-compose up
```

(Build again if `Dockerfile` is being changed)

```bash
docker-compose build
```

## Play with tasks

List tasks

```bash
curl http://127.0.0.1:8080/todos
```

Get a task

```bash
curl http://127.0.0.1:8080/todos/todo3
```

Add a task

```bash
curl http://127.0.0.1:8080/todos -d "task=something new" -X POST -v
```

Update a task

```bash
curl http://127.0.0.1:8080/todos/todo3 -d "task=something different" -X PUT -v
```

Delete a task

```bash
curl http://127.0.0.1:8080/todos/todo2 -X DELETE -v
```
