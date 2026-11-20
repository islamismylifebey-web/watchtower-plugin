# Remote Watchtower for Claude

![Remote Watchtower](assets/logo.png)

Remote Watchtower connects Claude to the computers you add to your own Watchtower account (Windows, Mac or Linux), so it can read and search files, write and edit them, run commands and check what's running on them from anywhere. On plans that include agent hands, it can also look at a computer's screen and use its mouse and keyboard inside a session you approve. The Watchtower watches every computer from the cloud and alerts you when one goes quiet.

This plugin gives Claude the Watchtower's remote MCP server plus four skills that teach it to use the Watchtower safely and well.

## What's in this plugin

- **MCP server:** `https://watchtower.galorweb.works/mcp` (Streamable HTTP). Sign-in is OAuth 2.0: Claude opens the Watchtower's sign-in page, you sign in and approve Claude, and you can cut Claude off any time under Connected apps in your Watchtower dashboard.
- **Skills:**
  - `remote-watchtower`: everyday work on your computers: find, read, write and edit files, search, run a command, check a process.
  - `watchtower-computer-checkup`: a read-only health check across your computers (online, disk, memory, uptime, what's using a machine).
  - `watchtower-fix-a-problem`: find the cause first, then fix one approved change at a time.
  - `watchtower-agent-hands`: how to use the screen, mouse and keyboard: look before every action, stop before any click that submits, pays or deletes, never type passwords.

The plugin contains no code, hooks or scripts. It runs nothing on your machine by itself.

## What it sends and where

Everything goes to one place: the Remote Watchtower service at `watchtower.galorweb.works`, run by GALOR WebWorks. Each tool call Claude makes travels from Claude to the Watchtower and on to the computer you named, and the result comes back the same way. The Watchtower doesn't keep the files, command output or screenshots your tools return. See the [privacy policy](https://watchtower.galorweb.works/privacy).

## Before you start

1. [Create a free Watchtower account](https://watchtower.galorweb.works/signup) (10,000 tool calls a month, up to 3 computers).
2. In your dashboard press **Add a computer** and run the one install line it shows on each computer you want Claude to reach.
3. Install this plugin, and sign in when Claude asks.

## You stay in control

Each computer has its own permission level: ask for everything, ask for risky actions only (the default), or full access. A call that needs your yes waits for Approve or Deny on your phone. A never list blocks what a computer must never do, and no connected app can change the Watchtower's own permissions.

## Try it

- "Which of my computers are online, and how much disk space does each have left?"
- "Find the newest PDF in Documents on my office computer and summarize it."
- "On my work PC, check what's using the most memory right now."

## Help

- Documentation: https://watchtower.galorweb.works/docs
- Support: https://watchtower.galorweb.works/support (m.penningtonbey@galorweb.works)
- Plans: https://watchtower.galorweb.works/plans

## License

PolyForm Strict 1.0.0: free to use for any noncommercial purpose; no redistribution or changes. See [LICENSE](LICENSE). The Remote Watchtower service has its own [terms](https://watchtower.galorweb.works/terms).
