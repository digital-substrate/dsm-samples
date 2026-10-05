# DSM Language Samples

Reference models in the **Digital Substrate Model (DSM)** language, used to demonstrate modeling patterns and exercise the [dsm-jetbrains](https://github.com/digital-substrate/dsm-jetbrains) and [dsm-vscode](https://github.com/digital-substrate/dsm-vscode) IDE plugins.

## Documentation

Full documentation: https://docs.digitalsubstrate.io/dsm/samples/

Part of the [DevKit ecosystem](https://docs.digitalsubstrate.io/).

## Contents

### `Tuto/` — the tutorial model

The model the documentation's tutorials use: a `User` with its login, identity, account,
avatar and portrait. `Tuto/kibo.toml` generates it with kibo 2 — a Python package and a TypeScript package
in `Tuto/generated/`:

```sh
python3 tools/kibo_project.py generate dsm-samples/Tuto/kibo.toml   # from the DevKit's root
```

### `Ge/` — Graph modeling

A complete graph topology system demonstrating:

- Concept definitions (`Graph`, `Vertex`, `Edge`)
- Attachment system for topology and visual attributes
- Attachment function pools for collaborative editing:
  - `ModelGraph` — topology editing (newVertex, newEdge, deleteSelection)
  - `ModelSelection` — selection management (selectAll, deselectAll)
  - `ModelIntegrity` — data integrity restoration
- Mutable operations with proper return types (`key<T>`, `void`)
- Query functions for state inspection

### `Re/` — 3D rendering system (Raptor)

A rendering engine data model covering:

- Camera (depth of field, motion blur)
- Material system with inheritance (matte, mirror, multilayer)
- Lighting, textures, environment
- Sensors and timeline management
- Bezier paths, kinematics, clipping planes

## Validation

These samples can be validated using [`dsm_util.py`](https://github.com/digital-substrate/dsviper-tools) — the semantic validator for `.dsm` files. Any DSM consumer that implements `spec/dsm-json.md` can also process them.

## License

This project is licensed under the MIT License — see [LICENSE](LICENSE).
