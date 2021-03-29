# action-install-feelpp
github action to install feelpp on a debian/ubuntu runner
# Usage

See [action.yml](action.yml)

```yaml
uses: feelpp/action-install-feelpp@v1
with:
  dist: ubuntu
  flavor: focal
  install: libfeelpp1 feelpp-tools libfeelpp-dev
```

See [Feel++ documentation](https://docs.feelpp.org/user/0.109/install/index.html) for more information about the feelpp packages

- `dist`: type of distribution
  - values ubuntu, debian
  - default: ubuntu
- `flavor`: distribution flavor
  - values: buster, focal, bionic
  - default: focal
- `version`: distribution of feelpp
  - values: latest, stable
  - default: latest
- `repo`: feelpp deb  repository
  - default: https://dl.bintray.com/
- `repo-name`: name of the repository
  - default: feelpp
- `install`: feelpp debian packages to install
  - default: libfeelpp1 libfeelpp-dev feelpp-tools

see the action at work [here](https://github.com/feelpp/action-install-feelpp/actions) in docker and ubuntu bionic/focal distributions.

## Note on self-hosted runners

For self-hosted runners, make sure that the user executing the runners can run the following commads passwordless  eg using  sudo and `/etc/sudoers`: `apt`, `apt-key` and `add-apt-repository`
# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)