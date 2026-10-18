# Homebrew tap for nethound

[nethound](https://github.com/michelsalib/nethound) shows which process (or container) listens on each
port, who can reach it, who is connected to it, and how everything on your machine connects.

```sh
brew install michelsalib/nethound/nethound
```

This installs the standalone binary from the GitHub release (macOS and Linux, arm64 and x64), with bash
and fish completion: commands, options, and for `who` and `kill` the ports listening now. For zsh, add
`eval "$(nethound completion zsh)"` to `~/.zshrc`, after `compinit`. Update with `brew upgrade nethound`.
Without root, other users' sockets show no process: `sudo nethound` shows them all.

nethound was called netbeagle up to 0.7.0, and so was this tap (`michelsalib/netbeagle`); `brew upgrade`
moves a netbeagle install to nethound.

`Formula/nethound.rb` is generated for each release by `scripts/packages.ts` in the nethound
repository, from the release's `SHA256SUMS`.
