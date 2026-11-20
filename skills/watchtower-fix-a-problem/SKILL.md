---
name: watchtower-fix-a-problem
description: Use when something is wrong on one of the user's computers and they want it found and fixed through the Remote Watchtower - a program that won't start, a service that is down, an error message, a failed job or backup, or a machine acting up while they are away from it.
---

# Find and fix a problem on a computer

## Find it first

1. Get the facts from the user in their words: which computer, what they expected, what happened instead, and when it
   last worked. Call `list_devices` if the computer isn't named or might be offline.
2. Look before you change anything. Read the program's own log or the error it printed, check whether its process is
   running, check disk space and the time of the last restart. Reading and searching run without asking on the default
   permission level.
3. Say what you found and what you think the cause is, in plain words, before proposing a fix. If you aren't sure,
   say what you would check next instead of guessing.

## Then fix it, one change at a time

- Propose the smallest change that would fix it, and say exactly what it does: the file and the lines, or the command.
- Changes wait for the owner's approval on their phone, depending on the computer's permission level. When a call says
  it is waiting, tell the user and stop. Don't reach for another tool to get around an approval or a block.
- Before editing a settings file, copy it next to itself with the date in the name, so the change can be put back.
- Make one change, then check whether the problem is gone. Don't stack several changes and hope.
- Restarting a program or a service is a change. Restarting the whole computer cuts the Watchtower's line to it until
  it is back: say so and get a clear yes first.
- Anything that can't be undone (deleting data, wiping a folder, reinstalling) needs the user's yes in the chat with
  the exact target named, even when the computer allows it.
- Never switch off security software, change the Watchtower's own settings, or move money to "fix" something.

## If it needs the screen

If the fix can only be made by clicking through a program, use the agent-hands skill and its rules. Files and commands
come first.

## Answering

Say what was wrong, what you changed, and how you confirmed it works now. If it isn't fixed, say what you ruled out and
what the user should check in person.
