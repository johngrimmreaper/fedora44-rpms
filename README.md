# fedora44-rpms

Public generated **stable Fedora 44 RPM repository**.

Paired private build-control repository: `johngrimmreaper/fedora44-rpm-packaging`.

The `main` branch contains only repository documentation. Published RPMs,
SRPMs, signed `repodata/`, repository descriptors, the public signing key,
generated provenance and the static package browser are generated onto the
`gh-pages` deployment branch by `rpm-builder`.

There are currently no real stable Fedora 44 package profiles in the migration
inventory. This repository therefore starts empty and is ready for future
stable Fedora 44 packages.

Legacy RPM binaries from `johngrimmreaper/rpm-packages` are intentionally not
copied into this repository.

Expected Pages URL after first publication:

`https://johngrimmreaper.github.io/fedora44-rpms/`
