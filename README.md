# Component Registry

The component registry is the platform catalogue of reusable runtime, storage,
network and integration components. Each tracked component has exactly one row
in the registry index; the index is the authoritative record used by release
engineering, procurement and the dependency audit.

Layout:

- `registry/INDEX.md` - the component index (see `registry/README.md` for the column and ordering rules)
- `registry/README.md` - index conventions
- `docs/ARCHITECTURE.md` - how the registry is assembled
- `components/<id>/README.md` - one stub per tracked component

New or changed components arrive as manifests under `manifests/` on a feature
branch. The batch is reviewed first, then the index is refreshed on that branch
before the batch is merged.
