---
icon: lucide/rocket
---

[![Image title](assets/images/logo.png){ align=right }](https://github.com/smashedr/zensical-test?tab=readme-ov-file#readme)

# Get Started

A Typed Python GitHub Actions Tookit similar to [actions/toolkit](https://github.com/actions/toolkit).

**To get started [install](#install) the tools and view the [usage](usage.md).**

If you run into any issues, [support](support.md) is available.

!!! danger

    This is an example site only.

    If you are looking for `actions-tools` visit:
    https://actions-tools.cssnr.com/

Test 1

## Install

From PyPI: https://pypi.org/p/actions-tools

=== "pip"

    ```shell
    python -m pip install actions-tools
    ```

=== "uv"

    ```shell
    uv add actions-tools
    ```

=== "requirements.txt"

    ``` text
    actions-tools
    ```

=== "pyproject.toml"

    ``` toml
    dependencies = ["actions-tools"]
    ```

With [PyGithub](https://github.com/PyGithub/PyGithub) (for GitHub API access).

=== "pip"

    ```shell
    python -m pip install actions-tools[github]
    ```

=== "uv"

    ```shell
    uv add actions-tools[github]
    ```

=== "requirements.txt"

    ``` text
    actions-tools[github]
    ```

=== "pyproject.toml"

    ``` toml
    dependencies = ["actions-tools[github]"]
    ```

Install from source.

```shell
git clone https://github.com/cssnr/actions-tools
python -m pip install actions-tools
```

Uninstall.

```shell
python -m pip uninstall actions-tools
```

&nbsp;

<!-- TODO: Mirror README.md usage here and update Usage for the docs site -->

[:lucide-notebook-pen: View the Usage](usage.md){ .md-button .md-button--primary }

```python
from actions import core, context

token = core.get_input("token", True)
g = core.get_github(token)  # (1)!
repo = g.get_repo(f"{context.repository}")
core.info(f"repo.name: {repo.name}")
```

1.  To use `get_github` install with the github extra:
    ```shell
    python -m pip install actions-tools[github]
    ```

**Make sure to view the full [Usage](usage.md) guide.**

&nbsp;

!!! question

    If you need help or run into issues, [support](support.md) is available!

!!! info

    This project is in active development.
    Please [let us know](https://github.com/cssnr/actions-tools/discussions/categories/feature-requests)
    what features you want to see.

!!! example "Documentation"

    This documentation site is a work in progress.
    See the [README.md](https://github.com/cssnr/actions-tools?tab=readme-ov-file#readme) for more details.
