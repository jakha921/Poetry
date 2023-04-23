# Poetry

### Commands

Poetry provides a number of commands to help you manage your project. The most common commands are:

* `poetry init`: Initialize a new project
* `poetry add <package>`: Add a dependency to your project
* `poetry install`: Install dependencies
* `poetry run <script>`: Run a script
* `poetry shell`: Run a shell
* `poetry update`: Update dependencies
* `poetry remove <package>`: Remove a dependency from your project

Poetry is a dependency manager for Python. It allows you to declare the libraries your project depends on and it will
manage (install/update) them for you.

## Installation

You can install Poetry through `pip`:

    pip install poetry

## Usage

### Creating a initial `pyproject.toml` file

    poetry init

### Adding a dependency

    poetry add requests

### Installing the dependencies

    poetry install

### Running a script

    poetry run python script.py

### Building a package

    poetry build

### Publishing a package

    poetry publish --build

### Exporting the dependencies to a `requirements.txt` file

    poetry export -f requirements.txt > requirements.txt

### Importing a dependency from a `requirements.txt` file

    poetry add -D -E <package>

---

### Installation and Setup

1. Install Poetry: `pip install poetry`
2. Initialize Poetry: `poetry init`
3. Add dependencies: `poetry add <package>` or `poetry add <package> --dev`
4. Install dependencies: `poetry install`
5. Run scripts: `poetry run <script>`
6. Run shell: `poetry shell` (exit with `exit`)
7. Update dependencies: `poetry update`
8. Remove dependencies: `poetry remove <package>`
9. Build package: `poetry build`
10. Publish package: `poetry publish`
11. Export dependencies: `poetry export -f requirements.txt > requirements.txt`
12. Import dependencies: `poetry add -D -E <package>`
13. Lock dependencies: `poetry lock`
14. Show dependencies: `poetry show`
15. Show package: `poetry show <package>`
16. Show version: `poetry --version`
17. Show help: `poetry --help`
18. Show tree: `poetry show --tree`
19. Show latest: `poetry show --latest`
20. Show outdated: `poetry show --outdated`

### Poetry scripts

Poetry scripts are defined in the `tool.poetry.scripts` section of the `pyproject.toml` file. For example:

```toml
[tool.poetry.scripts]
my_module_runner = "my_package:main"
```


### Configuration

Poetry uses a `pyproject.toml` file to store configuration. The default configuration is:

```toml
[tool.poetry]
name = "my-package"
version = "0.1.0"
description = ""
authors = ["Your Name <username> <email>"]

[tool.poetry.dependencies]
python = "^3.6"

[tool.poetry.dev-dependencies]

[build-system]
requires = ["poetry-core>=1.0.0"]
build-backend = "poetry.core.masonry.api"
```


