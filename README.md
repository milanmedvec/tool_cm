# tool_cm

Small runc-based container image manager backed by Docker exports and OCI configs.

## Commands

- `cm` - create/list/run/remove local container images

## Dependencies

- bash
- docker
- runc
- jq
- tar
- mktemp/coreutils

## Install

```bash
./install.sh
```

Install to a custom prefix:

```bash
PREFIX="$HOME/.local" ./install.sh
```

## Usage

```bash
cm list
cm create NAME
cm run NAME
```

## Configuration

- Images are stored under `$HOME/.local/share/cm`.

## Notes

These scripts were extracted from a personal Arch Linux + i3 workspace. Review dependencies and paths before using them on another machine.
