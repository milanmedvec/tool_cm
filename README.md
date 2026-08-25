# tool_cm

Small runc-based container image manager backed by Docker exports and OCI configs.

## Commands

- `cm` - create/list/run/remove local container images

## Dependencies

Required commands:
- `bash`
- `docker`
- `runc`
- `jq`
- `tar`
- `mktemp`

Check required commands in your shell:

```bash
need() {
    command -v "$1" >/dev/null || echo "missing: $1"
}

for cmd in bash docker runc jq tar mktemp; do
    need "$cmd"
done
```

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
