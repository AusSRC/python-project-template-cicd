# python-project-template-cicd

A small python project template that utilises the `python-templates` submodule to show how AusSRC projects can setup linting, testing, and CI/CD pipelines.

## Setup

```bash
git submodule update --init --recursive
python3 -m venv .venv
source .venv/bin/activate
pip install ".[dev]"
```

## Lint and test

```bash
make lint
make test
```

Both commands are provided by the `python-templates` submodule and imported through the project `Makefile`.

## CI/CD

- `.github/workflows/ci.yml` runs linting and tests with `make lint` and `make test`.
- `.github/workflows/release.yml` builds Python artifacts and uploads them to the GitHub Actions artifact registry.
