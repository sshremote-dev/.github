# Security

SSH Remote reaches other computers, so its security matters more than most programs'. Thank you for
taking the time to report a problem.

## Reporting

Please report a vulnerability privately, through **Report a vulnerability** on the Security tab of
the repository it concerns ([sshremote](https://github.com/sshremote-dev/sshremote/security),
[sshremote-relay](https://github.com/sshremote-dev/sshremote-relay/security) or
[sshremote-extensions](https://github.com/sshremote-dev/sshremote-extensions/security)). Do not
open a public issue for it.

Say what is affected (the version from `sshremote --version`, the platform), what an attacker can
do, and how to reproduce it. We answer within a few days, keep you told as we fix it, and credit you
in the release notes unless you would rather not be named.

## Scope

- The app: the window, the host agent, the terminal viewer, the browser gateway and the MCP server.
- Remote access by ID: the password proof (SPAKE2), the sealed stream (ChaCha20-Poly1305), the
  relay and the direct paths.
- Updates and the extension registry: their signatures and how they are checked.

The servers at sshremote.dev, relay.sshremote.dev and web.sshremote.dev are in scope as well.

## Supported versions

Fixes go into the latest release; the program updates itself (`sshremote update`).
