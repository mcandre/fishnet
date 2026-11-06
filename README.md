# fishnet: Jellyfin normalizer

[![Lint](https://github.com/mcandre/fishnet/actions/workflows/lint.yml/badge.svg)](https://github.com/mcandre/fishnet/actions/workflows/lint.yml) [![license](https://img.shields.io/badge/license-BSD-0)](LICENSE.md)

# SUMMARY

fishnet normalizes multimedia directories for Jellyfin.

This helps to work around low level Jellyfin glitches, such as NFO metadata file generation. Especially when the Jellyfin service runs as a different UNIX user account than the account adding videos.

# EXAMPLES

```console
$ fishnet
```

# DOWNLOAD

```sh
git clone https://github.com/mcandre/fishnet.git ~/src/github.com/mcandre/fishnet
```

* [bash](https://www.gnu.org/software/bash/) 4+
* [findutils](https://pubs.opengroup.org/onlinepubs/9799919799/utilities/find.html)
* [git](https://git-scm.com/)
* [Jellyfin](https://jellyfin.org/)
* GNU compatible [readlink](https://www.gnu.org/software/coreutils/manual/html_node/readlink-invocation.html)

## Postinstall

Register `"$HOME/src/github.com/mcandre/fishnet/bin` to `PATH` environment variable.

Set environment variable `FISHNET_JELLYFIN_HOME` to a parent directory containing your libraries (e.g. `$HOME/jellyfin`).

For details on building from source, see [DEVELOPMENT](DEVELOPMENT.md).

# ABOUT

fishnet streamlines multimedia files and folders for better integration with Jellyfin.

## Features

* Recurses over directories
* Fixes path ownership
* Fixes path chmod permissions

## Tips

* Re-run refresh metadata in `Scan for new and updated files` and/or `Search for missing metadata` modes as needed.
* Ensure the `jellyfin` user is a member of a `jellyfin` group.
* Review Jellyfin logs to gather further troubleshooting details.

🏸
