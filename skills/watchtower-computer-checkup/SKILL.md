---
name: watchtower-computer-checkup
description: Use when the user asks how their computers are doing through the Remote Watchtower - which are online, disk space, memory, uptime, what is using a machine, or a routine health check across all of them.
---

# Computer checkup

A read-only look at the user's computers. Nothing here changes a machine.

## Steps

1. Call `list_devices`. It already gives each computer's online state, permission level, operating system, memory, disk
   and uptime. For a quick "are they all up?" this one call is the whole answer.
2. For a computer the user asks about in more depth, look only as far as the question needs:
   - Disk filling up: list the largest folders under the user's home or the drive they named.
   - Slow machine: `list_processes`, and name the few using the most memory or processor.
   - "Did it restart?": uptime from `list_devices`, then the system's own restart record if they want the reason.
3. Use look-only commands (`dir`, `ls`, `systeminfo`, `tasklist`, `uptime` and the like). They run without asking on
   the default permission level. If a command would change anything, it doesn't belong in a checkup.
4. An offline computer can't be checked. Say it is offline and when it was last seen, and suggest running its install
   line again from the dashboard if it should be on. Don't retry in a loop.

## Answering

Lead with anything that needs attention: a computer that is offline, a disk above about 90 percent, memory that is
nearly full, or a machine that restarted unexpectedly. Then one line per computer. With more than three computers, a
small table (computer, online, disk free, memory, up since) reads faster than sentences.

Don't suggest fixes that delete or stop things unless the user asks what to do. If they do, say exactly what you would
remove or stop and get their yes first.
