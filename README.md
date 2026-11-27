# jq-snap
Snap packaging for the jq command-line JSON processor

This repository packages [jq](https://github.com/jqlang/jq) release
[1.8.2](https://github.com/jqlang/jq/releases/tag/jq-1.8.2) as a `core24` snap.
The snap builds for amd64, arm64, armhf, ppc64el, riscv64 and s390x,
and uses Ubuntu's Oniguruma library for regular expressions.

## Building

```sh
snapcraft pack
sudo snap install --dangerous jq_1.8.2_amd64.snap
jq --version
```

A GitHub Actions workflow (`.github/workflows/build.yml`) builds the snap for
amd64 on every push and pull request, installs it and checks that `jq` is
callable.
