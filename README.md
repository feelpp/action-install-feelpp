# action-install-feelpp
github action to install feelpp on a debian/ubuntu runner
# Usage

See [action.yml](action.yml)

```yaml
uses: feelpp/action-install-feelpp@main
with:
  dist: ubuntu
  flavor: focal
  install: feelpp,feelpp-tools
```

- dist: type of distribution
  - values ubuntu, debian
  - default: ubuntu
- flavor: distribution flavor
  - values: buster, focal, bionic
  - default: focal
- version: distribution of feelpp
  - values: latest, stable
  - default: latest
- repo: feelpp deb  repository
  - default: https://dl.bintray.com/
- repo-name: name of the repository
  - default: feelpp
- install: feelpp debian packages to install
  - default: libfeelpp1 libfeelpp-dev feelpp-tools


# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)