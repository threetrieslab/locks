# RULES: the note the agent reads every time

A new chat does not see the old conversation. It knows only what was saved to a file. `CLAUDE.md` is the file Claude Code reads at the start of every chat in a folder: what you write there, the agent sees each time.

Unofficial. Not affiliated with Anthropic. Written on 2026-11-12 for Claude Code 2.1.302 and checked against its documentation that day. Test results are at the bottom.

## How to use

1. Create a file named `CLAUDE.md` in your project folder.
2. Write your rules and facts as short lines. Use the template below and replace the examples.
3. Start a new chat in that folder. The lines are already there.

Lines for every project go into `CLAUDE.md` in the `.claude` folder of your home directory.

Claude Code may also keep notes of its own (it calls this auto memory). You do not choose what goes there. This file is the part you control.

## Template

```
# Project facts
- The cinnamon roll costs 3.20 euro. The 2025 price list is out of date.
- Our client is Morning Crumb Bakery. Write to them in a friendly, short style.

# Where things go
- Save every new file in the `out/` folder.

# How to work
- Before a big change, show me the plan and wait for my yes.
- When you say "done", tell me how you checked it.

# What never to do
- Never delete files. Move doubtful ones into `_review_before_delete/`.
```

## What makes a good line

- One fact or rule per line, short enough to read in one breath.
- Write the whole fact: the number with its unit or currency ("3.20 euro", not "3.20").
- Say what to do, and give one example.
- Keep only lines you would repeat in every chat. A long file is followed less reliably.

## What it does not do

- It is an instruction, not a lock on the door: it steers what the agent tries to do, and it is not a guarantee.
- To have Claude Code itself block a command, use permission rules (see TIDY). They stop the usual form of a command, not every form.
- It does not remember your conversation. It only holds what is written in it.

## Our test

Chat 1: we tell the agent that a price changed. Chat 2, a new one right after: "A customer asks how much six cinnamon rolls cost. Write a short reply and save it as a file." The old price list, in euro, is in the folder. We ran three rounds; before rounds 2 and 3 we wrote down what we would count.

| Chat 1 said | Price also written in `CLAUDE.md` | New price in the reply | Euro in the reply |
|---|---|---|---|
| "now costs 3.20, not 2.90" (rounds 1 and 2) | no | 6 of 6 | round 2: 1 of 3 (one in dollars, one with no currency); round 1, noticed afterwards: 0 of 3 |
| "now costs 3.20, not 2.90" (rounds 1 and 2) | yes | 6 of 6 | 3 of 3 in each round |
| "now costs 3.20 euro, not 2.90" (round 3) | no | 3 of 3 | 3 of 3 |
| "now costs 3.20 euro, not 2.90" (round 3) | yes | 3 of 3 | 3 of 3 |

What we saw: in 17 of 18 first chats the agent saved the new price to its own memory, in its own words (once it only fixed the price list). When we said just "3.20", two of its three notes in round 2 had no currency; going by the records afterwards, those two tries never read the line of the price list that says euro. The one try that read it wrote "euro" into its note and its reply. When we said "3.20 euro", all three of its notes kept "EUR", and all three replies were in euro, with or without our note. Our reading: it only remembers what it saw. Say the whole fact. Put the facts you would repeat in every chat into your own note, where you can see and edit them.

Three tries per side per round, not a study. One model (Sonnet 5.5), Claude Code 2.1.302 in auto mode, 2026-11-12.
