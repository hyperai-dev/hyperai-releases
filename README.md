# hyperai-releases

Public release artifacts for the [`hyperai`](https://hyperfx.ai) CLI.

The CLI source lives in a private monorepo (`hyperai-dev/hyperai-clients`).
Tagged binary releases are pushed here so anyone can `curl` them without
needing access to the source.

## Install

Run the installer. It picks the archive for your OS and CPU, checks its SHA-256 and installs `hyperai` to `$HOME/.local/bin`:

```bash
curl -fsSL https://raw.githubusercontent.com/hyperai-dev/hyperai-releases/main/install.sh | sh
```

Manual download: each release has `hyperai_<version>_<OS>_<arch>.tar.gz` for macOS and Linux (`macOS` or `linux`, `arm64` or `x86_64`), `hyperai_<version>_windows_x86_64.zip` for Windows, and `checksums.txt`. The latest release: https://github.com/hyperai-dev/hyperai-releases/releases/latest

## Verify

```bash
hyperai --help
hyperai --version
```

## Other install channels

- Python: `uv tool install hyperai-cli` or `pipx install hyperai-cli`
- TypeScript / Node: `npm install -g @hyperai/cli`

All channels ship the same `hyperai` command from the same source.
