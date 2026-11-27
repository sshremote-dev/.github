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

On Debian or Ubuntu, Linux needs a C++ compiler and `pkg-config cmake nasm libgstreamer1.0-dev
libgstreamer-plugins-base1.0-dev libasound2-dev libxkbcommon-dev libwayland-dev` (the
app's CI workflow lists the same). The ignored tests start the built program, draw windows or reach
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

## Translations

SSH Remote speaks 53 languages. The English text is in the code; each other language is
`assets/lang/<code>.json` in the sshremote repository, a table from the English text to the
language's own. The tables were translated by machine and reviewed twice, but not yet by people who
speak each language, so corrections from them are especially welcome:

- a wrong word or sentence: open a **Translation** issue (the app links to it from Settings >
  Appearance > Language), or change the table and send a pull request;
- keep every `{}` (or `{0}`, `{1}` to put values in another order), `<b>`/`<a>` tags, leading and
  trailing spaces, key names (Ctrl, Alt, Shift) and product names as they are;
- `python3 scripts/lang.py check` must say 0 missing and 0 slots wrong for the language;
  `scripts/lang.py todo CODE` and `scripts/lang.py pairs CODE` list what to translate or review.

A new language is a new table with the same keys, and a line in the list in `src/lang/mod.rs`.

## License

By contributing you agree that your contribution is licensed under the MIT license of the
repository.
