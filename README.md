# Ctrl+C



## Installation

```bash
pip install ctrlc
```

## Basic Usage
```bash
ctrlc run
```

## Flags & Options

- `--ignore-files [none|all]`

    - none: don’t respect any .gitignore/.contextignore.

    - all: always respect both if present.

- `--threshold <bytes>`

    Skip files larger than this size (in bytes).

- `--compress [none|gzip|zip]`

    Output compression. Default none.

## Configuration

Create optional `pyproject.toml` section `[tool.ctrlc]` or `.contextignore` in root.

```
[tool.ctrlc]
ignore_files = "all"
threshold = 1048576
template = "default"
```

## Example Usage
```bash
ctrlc run --compress gzip --threshold 1000000
```