<p><img src="https://raw.githubusercontent.com/lenar2/luch/main/website/assets/luch-ray.svg" alt="" width="36"></p>

# LUCH for Cursor
### When the next step lives outside the editor.

Cursor helps you reason about code. With **an enabled LUCH account and explicit grants**, it can also reach a selected browser, permitted file or server to inspect the situation — then bring an actual result back into your work.

[**A real LUCH outcome**](https://github.com/lenar2/luch/blob/main/docs/REAL_WORK.md) · [**Install in Cursor**](#connect-in-cursor) · [Русский](README.ru.md) · [LUCH home](https://github.com/lenar2/luch)

> **Access is limited:** public source is available, but a fresh Cursor user's OAuth sign-in, end-to-end access and cross-tenant isolation have not been independently verified. Installing the plugin never pairs a machine or enrolls an account.

## An actual problem, investigated and changed

The founder said that LUCH's website spoke to engineers rather than people and required the Mac to stay untouched. The assistant inspected the live site and source, prepared a revision, tested pages and released the authorized change. Here is the [exact commit](https://github.com/lenar2/luch/commit/06daa8d6b89a3dfd65e74628b895879e79a0c931) and the [record of checks](https://github.com/lenar2/ai-factory-evidence/issues/4009#issuecomment-6692683064).

**This is evidence of LUCH with authorized server and GitHub tools in the founder's environment — not a claim that Cursor executed the case.** The [creative audit](https://github.com/lenar2/ai-factory-evidence/issues/4009#issuecomment-6705944671) found that the design still needed work.

## What Cursor and LUCH could do together

| Your goal | Permitted operation | Result to inspect |
| --- | --- | --- |
| “Why did this site break?” | Read a permitted website and compare approved source | An explanation with links |
| “Does my server actually respond?” | Run a bounded command on the server you selected | Observed diagnostic output |
| “Prepare the fix, but don't release it.” | Read authorized files or repository context | A reviewable change, **not** deployment |

These are possible tasks; capability and permission scopes vary by account and device.

## Connect in Cursor

**1 · Check access first.** [Service status](https://luch.lenarsalimov.ru/en/status/). The hosted Core currently operates for enabled test/reviewer accounts. A public client is not a self-service signup.

**2 · Install the local plugin** (in a supported Cursor version).

```bash
mkdir -p ~/.cursor/plugins/local
git clone https://github.com/lenar2/luch-cursor.git ~/.cursor/plugins/local/luch
# If already installed, update that existing checkout instead of cloning again.
```

Reload Cursor, open **Customize → Plugins**, and confirm the LUCH MCP server and the 12 included skills are detected.

**3 · Authorize only if enabled.** Use Cursor's host-supported OAuth flow for the protected LUCH MCP endpoint. Verify available tools. Never enter passwords or access tokens in chat.

**4 · Start read-only.** For example, “Find which of my authorized devices are available.” Inspect the actual result before asking it to make a change.

If your account is not enabled, stop here; do not borrow credentials or connect to the founder's devices.

<details><summary>Developer and reviewer details</summary>

- Cursor Plugin manifest: [`.cursor-plugin/plugin.json`](.cursor-plugin/plugin.json); public MCP configuration: [`mcp.json`](mcp.json); twelve permission-aware skills: [`skills/`](skills/).
- HTTPS endpoint `https://api.lenarsalimov.ru/luch/core/mcp`; protected OAuth access required.
- A proper new-tenant acceptance test includes OAuth sign-in, authorized demo-device discovery, a synthetic file read, explicitly approved demo-device rename, forbidden-path denial and revocation. These tests are **not** claimed as passed for independent new Cursor users.
- The repository provides client source only, not the hosted backend, private accounts, device secrets or access to third-party machines.

[Security](SECURITY.md) · [Apache-2.0](LICENSE) · [Support](https://luch.lenarsalimov.ru/support/) · [Privacy](https://luch.lenarsalimov.ru/privacy/)

</details>
