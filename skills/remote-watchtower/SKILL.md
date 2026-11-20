---
name: remote-watchtower
description: Use when the user wants to do something on one of their own computers through the Remote Watchtower - find, read, write or edit files, search folders, run a command, check a process, or see which computers are online and healthy.
---

# Remote Watchtower

The Remote Watchtower reaches computers the user has added to their own account. Every tool runs on one of them.

## Before the first call

1. Call `list_devices` to see the user's computers, whether each is online, its permission level, and its OS, memory,
   disk and uptime.
2. Pass `device` with every other call, using a name exactly as `list_devices` shows it. If the user has more than one
   computer and didn't say which, ask - don't guess.
3. If a computer is offline, say so plainly and suggest they run its install line again from the dashboard. Don't
   retry in a loop.

## Doing the work

- Prefer looking before changing: list or search, read, then write or edit.
- Use full paths. On Windows, paths look like `C:\Users\name\Documents`; on Mac and Linux, `/Users/name` or `/home/name`.
- Read large files in pieces (`offset` and `length`) instead of all at once.
- For a long command, `start_process` returns a process id; read more with `read_process_output`.
- A call that takes longer than about a minute comes back with a ticket. Pass it to `get_tool_result` to collect the
  result.

## Approvals and limits - the user decides

- Some calls wait for the user's approval on their phone (writes, edits, moves and commands, depending on the computer's
  permission level). When a call says it is waiting for approval, tell the user it is waiting on their phone and stop.
  Don't try another tool to get around it.
- A denied or blocked call is final for that request. Say what was blocked and why, in one line.
- Before anything that can't be undone (deleting, overwriting, killing a process), say exactly what will happen and get
  the user's yes in the chat first, even when the computer allows it.
- Never run commands that move money, change the Watchtower's own settings, or turn off security software, and never
  copy passwords, keys or tokens into the chat.

## Answering

Report only what the user asked for: the answer, the file's relevant lines, or what changed. Leave out raw logs and
long listings unless they asked for them.
