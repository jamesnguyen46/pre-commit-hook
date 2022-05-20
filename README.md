# Pre-commit Hook

My custom hook for [pre-commit](https://pre-commit.com/).

## Usage

```yaml
- repo: https://github.com/jamesnguyen46/pre-commit-hook
  rev: v0.0.1
  hooks:
  - id: validate-python-file-name
    name: validate python file name
```

## Hooks

- `validate-python-file-name` id
  - Check whether python file path is valid or not. File path is valid when only includes lower characters and not contains `space` character and `hyphen` symbol.
  - Example :
    - `"src/python/command_line.py"` ✅
    - `"src/python/command-line.py"` ❌
    - `"src/python/command line.py"` ❌
    - `"src/Python/command-line.py"` ❌

