# UV venv setup

## Install uv

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

## Check uv --version

```bash
uv --version
```

## Check available python versions in uv

```bash
uv python list
```

## Create a uv venv

```bash
uv venv --python 3.14.0 python-venv
# give the version you want after --python.
# python-venv is the custom venv name.
```

## Activate the venv

```bash
source python-venv/bin/activate
```

## Check python version and path

```bash
python --version
which python
```

## Install packages

```bash
uv pip install <package-name>
# Example:
uv pip install numpy
```

## Save installed venv packages name into a text file

```bash 
uv pip freeze > requirements.txt
```

## Install the packages from the text file

```bash
uv pip install -r requirements.txt
```

## Clear uv cache

```bash
uv cache clean
```