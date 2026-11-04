# LUCH for Cursor — v0.1.6

**LUCH is an independent platform, not a Cursor-only product.** Discover its capabilities and all AI clients at the [LUCH product hub](https://github.com/lenar2/luch) or [global website](https://luch.lenarsalimov.ru/). This repository contains only the Cursor adapter.

LUCH is a Cursor Plugin with 12 permission-aware skills and one HTTPS Streamable HTTP MCP server. It helps an authorized agent work with explicitly linked browsers, files, services, and devices.

## Availability
The client code is public; **hosted LUCH access is currently limited to enabled reviewer/test accounts**. Independent Cursor-host OAuth sign-in, multi-tenant isolation, and a full three-scenario in-app E2E test have not yet been verified. Installing this client does not enroll a new LUCH user, pair a device, or grant permission to the publisher's private machines. Never bypass account or device authorization.

## Installation and local verification
1. Download or clone https://github.com/lenar2/luch-cursor
2. Copy the plugin to `~/.cursor/plugins/local/luch`, including `.cursor-plugin/plugin.json`, `skills/` and `mcp.json`.
3. Reload the Cursor window and open Customize / Plugins. Check that one LUCH MCP server and the 12 documented skills are detected.
4. Connect the MCP server only through the host's supported OAuth process **using an explicitly authorized account**. Check available tools and begin with read-only operations. Do not send access tokens or passwords to a chat.
5. For a real end-to-end verification, test on a synthetic reviewer tenant: authorized demo device discovery, authorized demo-file read and explicitly approved demo-device rename, with forbidden-path and cross-tenant access denied. Capture evidence privately without secrets.

## Included
- `.cursor-plugin/plugin.json` — Cursor Plugin manifest
- `mcp.json` — HTTPS public OAuth MCP endpoint at `https://api.lenarsalimov.ru/luch/core/mcp`
- `skills/*/SKILL.md` — 12 permission-aware skills
- `LICENSE` — Apache-2.0 license for this client only
- `SECURITY.md` — vulnerability disclosure

The privately hosted LUCH server, user data, accounts and connected devices are **not included** in this open-source client.

## Service / support
- Website: https://luch.lenarsalimov.ru/
- Privacy: https://luch.lenarsalimov.ru/privacy/
- Terms: https://luch.lenarsalimov.ru/terms/
- Support: https://luch.lenarsalimov.ru/support/
- Private security disclosure: https://github.com/lenar2/luch-cursor/security/advisories/new
