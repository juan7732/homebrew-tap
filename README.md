# homebrew-tap

Personal [Homebrew](https://brew.sh) tap for [`ergo`](https://github.com/juan7732/ergo),
a multi-repo VS Code workspace manager.

## Install

```sh
brew tap juan7732/tap
brew install ergo
```

Or in one line:

```sh
brew install juan7732/tap/ergo
```

Upgrade later with:

```sh
brew upgrade ergo
```

> A Homebrew-installed `ergo` defers self-update to Homebrew: running
> `ergo update` will tell you to `brew upgrade ergo` instead of replacing the
> managed binary.

## Optional runtime tools

`ergo` depends on `git` (installed automatically). A couple of commands shell
out to extra tools you may want as well:

- `gh` (GitHub CLI) — required by `ergo update` &nbsp;→&nbsp; `brew install gh`
- `code` (VS Code CLI) — required by `ergo open` / `ergo edit`
  (enable via VS Code's *Shell Command: Install 'code' command in PATH*)

## How this tap is maintained

The formula in [`Formula/ergo.rb`](Formula/) is **generated and committed
automatically** by [GoReleaser](https://goreleaser.com) whenever a `v*` tag is
pushed to the `ergo` repository. Do not edit it by hand — changes belong in
`ergo`'s `.goreleaser.yaml`.
