# Three Tries: free locks

Small plain-text files that stop an AI coding agent from making one specific mistake. Each lock comes from a real test: three tries without it, three tries with it, and the numbers are in its README.

Unofficial. Not affiliated with or endorsed by Anthropic. Claude and Claude Code are Anthropic's products; we name them only to say what we tested.

| Lock | What it stops | Tested |
|---|---|---|
| [TIDY](tidy/) | The agent deleting files when you ask it to clean up or free up space. Doubtful files go to a review folder instead, and you decide. | 2026-11-12, Claude Code 2.1.302 |
| [RULES](rules/) | A new chat getting your facts wrong (prices, names, where files go). One file the agent reads at the start of every chat. | 2026-11-12, Claude Code 2.1.302 |
| [TRAPS](traps/) | The agent running something that overwrites your real data (in our test: the shop's own tests wiped its order book). Five rules, plus three test folders to try your own agent on. | 2026-11-13, Claude Code 2.1.302 |

## How to use

1. Open the lock's folder and read its README first. It says what the lock does and what it does not do.
2. Copy the files into your project folder, keeping the folder structure (`.claude/settings.json` must stay inside `.claude`).
3. Start Claude Code in that folder.

Nothing to install and nothing to run: these are text files. The one exception is `traps/traps.py`, a small Python script that builds test folders on your own computer; read it before you run it.

## What a lock is not

A lock is not a wall. It changes what the agent tries, and some locks also let Claude Code itself block the usual form of a command. Keep a copy of anything you care about.

## License

Free to use, copy and change, with no conditions (CC0 1.0).
