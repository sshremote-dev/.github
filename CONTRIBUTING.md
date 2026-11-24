# Contributing

Issues and pull requests are welcome in every repository of this organization.

## Before you start

For anything larger than a small fix, open an issue first and say what you want to change, so the
approach can be agreed before the work is done.

## Building and testing

```sh
cargo build --release
cargo test
```

Linux needs `libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev libopus-dev libasound2-dev
pkg-config` and a C++ compiler. The ignored tests start the built program, draw windows or reach
other computers; the README of each repository says how to run them. A change to a platform's
code (Windows, macOS, a Linux desktop) should be tried on that platform.

Before sending a change:

- `cargo clippy --release --tests` has no warnings, on the targets you touched;
- the tests pass;
- behaviour that changed is described in the README or the docs on the site.

## Commits

One change per commit, its message a single sentence that starts with one of `feat:`, `fix:`,
`refactor:`, `style:`, `chore:`, `docs:` or `init:`, for example
`fix: keep the waker when the screen is recorded again`.

## Code

Match the style around you. Comments are short and say why, not what. New dependencies need a good
reason; most of what the program needs is already in its tree.

## License

By contributing you agree that your contribution is licensed under the MIT license of the
repository.
