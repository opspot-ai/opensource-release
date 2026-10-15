# Open-source Release

A portable, instruction-only skill for preparing sanitized open-source repositories from existing projects under explicit owner authority. It supports sanitation-only releases and optional product-readiness work when that scope is requested.

## Install

From this repository root, run the following after cloning or downloading the repository. It refuses to replace an existing skill directory or symlink.

```sh
target="${CODEX_HOME:-$HOME/.codex}/skills/opensource-release"
if [ -e "$target" ] || [ -L "$target" ]; then
  printf 'Refusing to overwrite existing path: %s\n' "$target" >&2
  exit 1
fi
mkdir -p "$(dirname "$target")"
cp -R "skills/opensource-release" "$target"
```

## Use

Invoke the installed skill with **`$opensource-release`**. Provide the named projects, the requested release scope, owner authorization, rights and licensing decisions, and any publication boundary that applies.

Read [the skill instructions](skills/opensource-release/SKILL.md) for the workflow and templates. This package contains instructions and example templates; it does not run scans, create repositories, activate host settings, or publish. Installation alone does not prove that a host loaded the skill or that any release is usable, secure, or accepted.

## License

MIT. See [LICENSE](LICENSE).
