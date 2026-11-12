# Registry index conventions

- The index lives at `registry/INDEX.md`.
- Every tracked component has exactly one data row with five columns:
  `| id | name | tier | owner | version |`.
- `id` is the lowercase component identifier. `name` is the display name exactly
  as written in the component manifest. `tier` is one of `core`, `extension`,
  `experimental` or `integration`. `owner` is the owning team slug. `version`
  is the component version currently recorded for the registry.
- Data rows are sorted by `id` in ascending case-insensitive order.
- The line `_N components tracked._` must always equal the number of data rows.
- A component is indexed only while its manifest `status` is `active`.
  Manifests that are `deprecated` or `retired` stay in the repository but are
  not indexed.
- A manifest whose `id` is already indexed does not create a second row and
  does not change the existing row.
