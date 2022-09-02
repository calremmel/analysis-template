# analysis-template
A general template for analytics projects.

# Getting Started

## 1. Generate Project

If you do not have cookiecutter installed, do so with:

```
> pip install cookiecutter
```

Next, generate your project:

```
> cookiecutter https://github.com/calremmel/analysis-template.git
```

## 2. Create Virtual Environment

## 3. Configure Project

To make your packages in `src` importable from anywhere:

```
> pip install -e .
```

Next, in order to name your package:

```
> mv src new_package_name
```

## 3. Configure Jupyter

### Paired Markdown for Version Control

To auto-generate paired Markdown files for version-controlling notebooks:

1. Open command palette with `Cmd Shift C`
2. Select `Pair Notebook with Markdown`

### Keyboard Shortcut for Restarting and Running All

To enable a shortcut for "Restart Kernel and Run All Cells":

1. Open Advanced Settings with `Cmd ,`
2. Select `JSON Settings Editor` in top-right corner
3. Select `Keyboard Shortcuts` on left sidebar
4. Copy in the following under `User Preferences` inside the curly brackets:

```
"shortcuts": [
        {
            "args": {},
            "command": "runmenu:restart-and-run-all",
            "keys": [
                "Cmd Shift Enter"
            ],
            "selector": "[data-jp-code-runner]"
        }
]
```

Feel free to replace `Cmd Shift Enter` with whatever you like.

### Format Notebooks with both isort and black

To autoformat notebooks with both `isort` and `black`:

1. Open Advanced Settings with `Cmd ,`
2. Select `JSON Settings Editor` in top-right corner
3. Select `Jupyterlab Code Formatter` on left sidebar
4. Copy in the following under `User Preferences` replacing the `"python"` line under `"default_formatter"`

```
"python": ["isort", "black"]
```