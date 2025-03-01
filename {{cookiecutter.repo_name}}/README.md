# {{cookiecutter.project_name}}

{{cookiecutter.description}}

## Project Structure

```text
{{cookiecutter.repo_name}}
|-- bin                          # CLI scripts
|-- notebooks
|   |-- *.ipynb                  # Jupyter notebooks
|   `-- ipython_config.py        # IPython magic to let *.ipynb treat src/ as PYTHONPATH
{% if cookiecutter.package_name != "" -%}
|-- setup.py                     # To install {{cookiecutter.repo_name}} as a Python module
{% endif -%}
|-- src                          # Python modules developed in this project
{% if cookiecutter.package_name != "" -%}
|   `-- {{cookiecutter.repo_name}}
{% endif -%}
`-- tests                        # Unit tests

# Miscellaneous files
|-- .editorconfig                # Editor config (for IDE / editor that support this)
|-- .gitattributes               # .gitattributes
|-- .gitignore                   # .gitignore
|-- .pre-commit-config.yaml      # Precommit hooks
|-- .vscenv                      # Dot env with PYTHONPATH config (for IDE /editor that support this)
|-- LICENSE                      # License
|-- README.md                    # Template document
|-- ipython_config.py            # A copy of ipython_config.py (same as notebook/ipython_config.py)
|-- pyproject.toml               # Setting for Python code formatter
`-- tox.ini                      # Settings for select Python toolchains
```

## Credits

This project was initialized by {{cookiecutter.author_name}} using:

```bash
cookiecutter https://github.com/aws-samples/python-data-science-template
```

## License

This library is licensed under the {{cookiecutter.open_source_license}}. See the
`LICENSE` file.
