# pipenv_tools

The missing tools for `Pipenv`

## Install

`pipenv install pipenv_tools`

## The Tools

### build

`pipenv tools prepare_setup --options --params`

This command will parse the contents of your `Pipfile` and generate a
`setup.py` file and other required artifacts.

If passing `--plain` only a `setup.py` will be created, but by default it creates

`setup.py`, `setup.py`, `pyproject.toml` and `MANIFEST.in` files.

> NOTE: by default the `MANIFEST.in` will be generated according to your VCS files `.gitignore` for example. Or taking argument from your Pipfile.

### Publish

`pipenv tools publish --options`

Uses `twine` to release your package to PyPI but before it will execute a `check`
for `safety` issues and also if `--bump minor|major|fix` is passed it will also
invoke `pipenv tools bumpversion`

