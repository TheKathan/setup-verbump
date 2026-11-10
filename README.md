<p align="center">
  <a href="https://github.com/TheKathan/setup-verbump/releases"><img alt="latest release" src="https://img.shields.io/github/v/release/TheKathan/setup-verbump"></a>
  <a href="https://pypi.org/project/verbump-cli/"><img alt="verbump-cli on PyPI" src="https://img.shields.io/pypi/v/verbump-cli?label=verbump-cli"></a>
  <img alt="license" src="https://img.shields.io/github/license/TheKathan/setup-verbump">
  <img alt="runners: Linux, macOS" src="https://img.shields.io/badge/runners-Linux%20%7C%20macOS-555">
</p>

# Setup verbump CLI

Installs [verbump](https://github.com/TheKathan/verbump), version and changelog bumps for repos, and puts `verbump` on the PATH.

```yaml
- uses: TheKathan/setup-verbump@v1
- run: verbump status
```

verbump is installed from PyPI (`verbump-cli`) into its own virtualenv, and only the `verbump` command goes on the PATH. The job's `python3`, `pip` and other tools stay as they were, whatever the repo's stack.

| Input | Default | Meaning |
|---|---|---|
| `version` | `1` | `1` for the latest 1.x, an exact version such as `1.0.1`, or any pip requirement for `verbump-cli`. |
| `python-version` | `3.12` | Python for verbump's virtualenv (3.11+). It is not put on the PATH. |

| Output | Meaning |
|---|---|
| `version` | The installed verbump version, e.g. `1.0.1`. |
| `path` | Full path of the `verbump` command. |

To release with verbump in a workflow, use [verbump-release](https://github.com/TheKathan/verbump-release); to preview a pull request's release, [verbump-check](https://github.com/TheKathan/verbump-check). Both call this action.

Runs on Linux and macOS runners. MIT licensed.
