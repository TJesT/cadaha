# What is CaDaHa?
**Ca**tWar **Da**ta **Ha**ndler - service for data collection in browser-game CatWar.
Main purpose - collect various statistics for futher analysis

# DEV guide
## Installation
### MacOS
#### 1. Install python3.12
NOTE: In the end of script execution python3.12 installer will be launched.
      You need to continue installation through installer and then manually remove it.
```bash
curl -O https://www.python.org/ftp/python/3.12.7/python-3.12.7-macos11.pkg && open python-3.12.7-macos11.pkg
```
#### 2. Install poetry 1.8.4
```bash
curl -sSL https://install.python-poetry.org | python3.12 - --version 1.8.4
```
## Development
### Configure poetry
```bash
poetry config virtualenvs.create true --local && poetry config virtualenvs.in-project true --local
```
### Create local environment with dependencies
```bash
poetry install --with dev
```
### Activate virtual env
```bash
source .venv/bin/activate
```
### Linting
```bash
mypy cadaha
```
```bash
ruff check cadaha tests --fix-only
```
## Testing
```bash
pytest
```