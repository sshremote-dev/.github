# SSH Remote

**One workspace for all your servers and projects.** Split terminals across hosts, read an AI
agent's answer as Markdown, open a host's files or desktop in the next pane, all over the SSH login
you already have. No account, no open port, nobody in between.

[Website](https://sshremote.dev) · [Download](https://sshremote.dev/#download) ·
[Docs](https://sshremote.dev/docs.html) · [In the browser](https://web.sshremote.dev)

## What is this?

A developer who looks after many machines ends up with a pile of terminal windows, a remote desktop
app, an SFTP client and an AI agent scrolling away in one of those terminals. SSH Remote puts all of
it in one window: each tab is a computer, split into panes, and each pane is that computer's
terminal, its screen or its files. It needs nothing on the server but the same single program,
started over SSH. For a PC that SSH cannot reach, remote access by ID connects through a relay that
only copies bytes sealed end to end.

It runs on Windows, macOS and Linux (GNOME, KDE Plasma, Sway, Hyprland, COSMIC and X11 desktops),
is written in Rust and is open source under the MIT license.

## Repository map

| Repository | Description |
|---|---|
| [sshremote](https://github.com/sshremote-dev/sshremote) | The app: the window, the host agent, the terminal viewer, the browser gateway, the MCP server, the website and the release scripts |
| [sshremote-relay](https://github.com/sshremote-dev/sshremote-relay) | The relay behind remote access by ID |
| [sshremote-extensions](https://github.com/sshremote-dev/sshremote-extensions) | The extensions of the signed registry |
| [.github](https://github.com/sshremote-dev/.github) | This profile and the organization's community files |

## Getting started

Download the program for your system from [sshremote.dev](https://sshremote.dev/#download), put the
same file on each host, and run `sshremote`. The [docs](https://sshremote.dev/docs.html) cover SSH
hosts, remote access by ID, the workspace, the MCP server for AI agents and writing extensions.
