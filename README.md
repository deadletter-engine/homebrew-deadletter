# homebrew-deadletter

Homebrew tap for [deadletter](https://github.com/peixotomdb/deadletter) — local-first SMTP, Kafka, Redis, and webhook capture in a single Go binary.

## Install

```bash
brew tap deadletter-engine/deadletter
brew install deadletter
```

Or in one line:

```bash
brew install deadletter-engine/deadletter/deadletter
```

## Upgrade

```bash
brew upgrade deadletter
```

Or use the built-in in-place updater:

```bash
deadletter update
```

## Run as a background service

The formula ships a `brew services` definition, so you can run deadletter as a managed daemon:

```bash
brew services start deadletter      # launch on boot
brew services stop deadletter
brew services restart deadletter
```

Default service flags: `--smtp :1025 --http :8025`. Logs land in `$(brew --prefix)/var/log/deadletter.{log,err.log}` and state in `$(brew --prefix)/var/deadletter`.

## About this repo

This repository is **auto-generated** — every new tag on [peixotomdb/deadletter](https://github.com/peixotomdb/deadletter) triggers [GoReleaser](https://goreleaser.com) to:

1. Build darwin/linux × amd64/arm64 binaries
2. Publish release tarballs + `checksums.txt` on the main repo
3. Regenerate `Formula/deadletter.rb` here with fresh url + sha256
4. Commit and push

Do not edit `Formula/deadletter.rb` by hand — changes will be overwritten on the next release.

## License

MIT — same as [deadletter](https://github.com/peixotomdb/deadletter/blob/main/LICENSE).
