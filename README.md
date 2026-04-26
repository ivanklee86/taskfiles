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
