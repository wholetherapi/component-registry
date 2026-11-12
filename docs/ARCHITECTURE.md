# Registry architecture

The registry repository stores the catalogue view only. Component manifests are
produced by the build pipeline and staged under `manifests/` for review; the
artefacts themselves live in the platform artefact store.

```
manifests/            staged batch manifests (review only)
registry/INDEX.md     authoritative index consumed by downstream tooling
components/<id>/      lightweight per-component stubs
```

The index refresh is a manual release-engineering step: it must happen on the
feature branch that carries the batch so that the branch diff contains both the
manifests and the refreshed index.
