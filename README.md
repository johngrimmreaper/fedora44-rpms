# Reaper Fedora 44 RPM Repository

Public, signed **stable RPM repository for Fedora Linux 44**, containing packages maintained and published through the Reaper RPM build infrastructure.

# 🌐 Browse the repository

## **[https://johngrimmreaper.github.io/fedora44-rpms/](https://johngrimmreaper.github.io/fedora44-rpms/)**

The published site provides the complete package inventory, RPM metadata, repository descriptors, signing key, package browser, and current repository usage information.

> The Fedora 44 stable channel currently has no published RPM snapshot. The consumer URL and configuration below are the canonical endpoints and become active with the first stable publication.

## Configure the repository

RPM package signatures and repository metadata signatures are enabled for published snapshots.

Repository signing-key fingerprint:

```text
E4C3 D7CD 3003 57A5 07C2 B237 FF30 3241 B8B8 606D
```

After the first stable publication, install the repository signing key and repository descriptor, then refresh DNF metadata:

```bash
sudo rpm --import https://johngrimmreaper.github.io/fedora44-rpms/RPM-GPG-KEY
sudo curl -fsSL https://johngrimmreaper.github.io/fedora44-rpms/repo/reaper-fedora44-stable-fedora-44-stable.repo -o /etc/yum.repos.d/reaper-fedora44-stable-fedora-44-stable.repo
sudo dnf makecache --refresh
```

The generated repository descriptor enables both `gpgcheck=1` for RPM package signatures and `repo_gpgcheck=1` for signed repository metadata.

## Repository architecture

The `main` branch contains repository documentation. Published RPMs, signed `repodata/`, repository descriptors, the public signing key, and the generated static package browser are deployed to the `gh-pages` branch by `rpm-builder`.

Paired private build-control repository: `johngrimmreaper/fedora44-rpm-packaging`.

The published deployment branch is disposable generated state and can be rebuilt from the private controller. Legacy RPM binaries from `johngrimmreaper/rpm-packages` are intentionally not copied into this repository.
