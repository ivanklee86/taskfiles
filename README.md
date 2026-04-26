# taskfiles

[Remote taskfiles](https://taskfile.dev/docs/experiments/remote-taskfiles) for [task](https://taskfile.dev/).  (aka Ivan likes DRY)

## Standards

- Variables shall be defined in the format `[Filename]_[Var]` in MACRO_CASE (e.g. `UV_UNIT_TESTS`).

## Layout
```
.
├── LICENSE
├── README.md
├── languages
│   └── python
│       └── uv.yaml
└── tools
    └── gantry.yaml
```

## Usage

In your repository, create a `Taskfile.yaml` with the following contents:

```
version: '3'

includes:
  gantry: https://github.com/ivanklee86/taskfiles.git//tools/gantry.yaml

# Your other stuff here.
```

Your commands will be available from Taskfiles.

```
vscode ➜ /workspaces/terraform_modules (main) $ task gantry:build:write
The Taskfile at "https://github.com/ivanklee86/taskfiles.git//tools/gantry.yaml" has changed since you last used it!
--- Make sure you trust the source of this Taskfile before continuing ---
Continue? [y/N]: y
task: [gantry:build:write] gantry build --config gantry.yaml --write
🚀 Starting to build devcontainer with 1 overlay(s) → devcontainer.json
🔗 Overlay 1/1: https://github.com/ivanklee86/devcontainers
Enumerating objects: 37, done.
Counting objects: 100% (37/37), done.
Compressing objects: 100% (23/23), done.
Total 37 (delta 3), reused 21 (delta 1), pack-reused 0 (from 0)
✅ Wrote devcontainer.json
vscode ➜ /workspaces/terraform_modules (main) $ 
```