# DEVELOPMENT

We follow standard, `make` based commands for performing build operations.

# PREREQUISITES

* a UNIX-like environment (e.g. [WSL](https://learn.microsoft.com/en-us/windows/wsl/))
* [bash](https://www.gnu.org/software/bash/) 4+
* [findutils](https://pubs.opengroup.org/onlinepubs/9799919799/utilities/find.html)
* [Go](https://go.dev/)
* [Jellyfin](https://jellyfin.org/)
* [make](https://pubs.opengroup.org/onlinepubs/9799919799/utilities/make.html)
* GNU compatible [readlink](https://www.gnu.org/software/coreutils/manual/html_node/readlink-invocation.html)
* [ShellCheck](https://www.shellcheck.net/) 0.11.0+
* Provision additional dev tools with `make -f install.mk`

## Recommended

* [asdf](https://asdf-vm.com/)

## Postinstall

Register output of `go env GOBIN` to `PATH` environment variable.

Register `<git-clone-directory>/bin` to `PATH` environment variable.

Set environment variable `FISHNET_JELLYFIN_HOME` to a parent directory containing your libraries (e.g. `$HOME/jellyfin`).

# TASKS

We automate engineering tasks.

## Security Audit

```sh
make audit
```

## Lint

```sh
make
```
