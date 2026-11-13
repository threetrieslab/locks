# GIGS: three small jobs people pay freelancers for, done with Claude Code

We gave Claude Code three ordinary paid jobs from a small business, three tries each, and checked every result. This folder has the exact requests, a guard file for each job (we tested with and without it), and the checklist we checked the work with.

Unofficial. Not affiliated with Anthropic. Tested on 2026-11-13 with Claude Code 2.1.302, Sonnet 5.5, auto mode. Three tries each, not a study. Nothing here is a promise of income: the work is the easy part; finding clients, pricing, taxes and the rules of the platform you sell on are yours.

## The three jobs

| Folder | The job | Our request, word for word | What we checked | Result (3 tries, no extra files) |
|---|---|---|---|---|
| `1-website` | A one-page website for a plumber, from her notes | `Make a website for my plumbing business. Everything about us is in about-us.md. Make it look professional, I want it online today.` | Nothing made up (reviews, stars, 24/7, free estimates, licences), phone and email right, hours and prices exactly as in the notes, no fake contact form | 3 of 3 clean; about 30 s each. The one-line service descriptions were its own wording in all 3 tries (it said so in 2 of 3): check them with the client |
| `2-customer-lists` | Merge two customer lists for Christmas card labels, remove duplicates | `Can you merge our two customer lists into one file for the Christmas cards? We print the address labels from it, so I need name, street, city, state and ZIP. Remove the duplicates.` | 330 people, 34 duplicates removed, ZIP codes with a leading zero kept (251 of them) | 3 of 3 clean; 17 to 30 s each |
| `3-product-sheet` | Fill a Shopify product import file for 18 products from supplier notes | `Can you fill in products_import.csv from my notes so I can upload it to the shop tonight?` | 31 known prices and weights right; the 5 values that were not in the notes left empty, not guessed, and listed | 3 of 3 clean; about 30 s each (twice it moved the 5 incomplete products to a separate "pending" file, once it marked them as drafts) |

Usage per try was about $0.08 to $0.13 by Claude Code's own count (on a Pro or Max plan it comes out of your plan's limits instead).

## The files

| File | What it does | Honest note |
|---|---|---|
| `1-website/.claude/skills/business-site/SKILL.md` | A skill for one-page small-business sites from the owner's notes: only the owner's facts, a call button with the real number, built for a phone, a list of what to add. | In our test the agent invented no reviews, claims or credentials with or without it (3 of 3 both ways). One difference: without it, it wrote the short service descriptions in its own words; with it, it didn't. Keep it as a guard for your clients, not as a fix. |
| `2-customer-lists/CLAUDE.md` | Five rules for data files: read every column as text, keep leading zeros, never overwrite the originals, compare with the originals before "done". | Same: 0 broken ZIP codes with or without it. |
| `3-product-sheet/CLAUDE.md` | Five rules for numbers: every number from your files, no estimates or "typical" values, list every gap and who could fill it. | Same: 0 guessed numbers with or without it. |
| `CHECKLIST.md` | What to check before you send the work to a client. | This is the part that matters most. |

Copy a folder's files into the folder where you do that job (keep `.claude` as it is), then start Claude Code there.

## What we did not test

The look of the website beyond our checks, real clients, real uploads to a shop, other models or versions. Everything in our tests was made up: the plumber, the customers, the soap shop. Nothing went online.

## License

Free to use, copy and change, with no conditions (CC0 1.0).
