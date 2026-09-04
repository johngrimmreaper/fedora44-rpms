# Reaper Fedora 44 RPM Repository

Public, signed RPM package repository. Package signatures and repository metadata are cryptographically verified by the published repository configuration.

## Browse the repository

**[https://johngrimmreaper.github.io/fedora44-rpms/](https://johngrimmreaper.github.io/fedora44-rpms/)**

## Configure the repository

Repository signing-key fingerprint:

```text
E4C3D7CD300357A507C2B237FF303241B8B8606D
```

### Reaper Fedora 44 RPM Repository - fedora-44 - stable

Repository ID: `reaper-fedora44-stable-fedora-44-stable`

```bash
sudo rpm --import https://johngrimmreaper.github.io/fedora44-rpms/RPM-GPG-KEY
sudo curl -fsSL https://johngrimmreaper.github.io/fedora44-rpms/repo/reaper-fedora44-stable-fedora-44-stable.repo -o /etc/yum.repos.d/reaper-fedora44-stable-fedora-44-stable.repo
sudo dnf makecache --refresh
```

RPM signatures: on; repository metadata signatures: on.

---

This README is generated automatically from the published repository snapshot.
