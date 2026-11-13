---
name: business-site
description: Builds a one-page website for a real small business (trades, shop, café, salon, studio, clinic) from the owner's own notes. Use whenever someone asks for a website, landing page or homepage for their business, or asks to redesign one.
---

# Business site from the owner's notes

Everything on this page is a promise to real customers, made in the owner's name. A made-up review, number or guarantee is a lie the owner answers for (fake reviews are banned in the US, UK and EU).

## 1. Collect the facts first
Read every file the owner gave you. Write down the facts: name, what they do and don't do, area, hours and when they're closed, prices, how to book, phone, email, their story. Only these facts go on the page.

## 2. Never invent
Do not add anything the owner didn't tell you, even if "every good site has it":
- customer reviews, testimonials, star ratings, customer or job counts
- guarantees, warranties, "free estimates", "same-day", "24/7", "emergency"
- licences, insurance, certifications, awards, memberships, "years of experience"
- services, days, areas or prices that aren't in the notes
- photos of strangers presented as the team

If a section needs something you don't have (reviews, photos, a licence number), leave it out of the visible page, put an HTML comment where it would go (`<!-- ADD: 2-3 real customer reviews -->`), and list it for the owner.

## 3. Contact that really works
No form that only shows "Thanks, we'll be in touch". Use a tap-to-call link (`tel:`) and an email link (`mailto:`) with the exact number and address from the notes. Add a form only if the owner named a form service; otherwise list "contact form needs a service" for the owner.

## 4. Built for a phone
- First screen: what they do, where, and a big Call button with the real number. Hours right under it, including when they're closed.
- Then: services with prices exactly as written, the area, how booking works, the story, contact.
- One file, `index.html`, CSS inside it. Opens by double click. No external fonts, scripts or images.
- Colours from the owner's logo, one accent colour. Body text at least 16px, strong contrast. No emoji as icons.

## 5. Before you say done
- Re-read the finished page. For every fact on it, find the line in the notes it came from. Delete anything without one.
- Check every phone number, price and hour against the notes character by character.
- Tell the owner in a few lines: what's on the page, what they should add (the HTML comments), and what you left out because you didn't know it.
