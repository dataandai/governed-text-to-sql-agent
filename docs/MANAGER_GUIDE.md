# Manager's Guide to the Retail Insights Assistant

*For store and regional managers. No technical background needed.*

The assistant answers business questions about our online store — customers, products,
orders, revenue — in plain English. You type a question, it looks at the data and comes
back with a short report. That's it.

## Starting a conversation

Your IT contact gives you a one-line command and a personal access code. After you run it,
you'll see:

```
manager>
```

Type your question after the `manager>` prompt and press Enter. When you're done, type
`/exit`.

## What kinds of questions work well

Ask the way you'd ask an analyst. Real examples:

- **Customers** — "Who are our top 10 customers by total spend?" · "How many repeat
  customers did we have this year?"
- **Products** — "Which product categories bring in the most revenue?" · "Which brands have
  the highest return rate?"
- **Trends over time** — "Show me monthly revenue for this year." · "How did order volume
  change over the last quarter?"
- **The data itself** — "What information do we actually have about customers?" (type
  `/schema` for the full list)

**Tips for better answers:**

- One question at a time beats a compound question. Instead of "show revenue and returns
  and top customers", ask three questions.
- Be specific about time: "monthly revenue in 2024" works better than "revenue lately".
- If the answer isn't what you meant, just rephrase — each question is answered fresh.

## A note about "branches"

We're an online retailer — there are no physical branch stores in the data. If you ask
about a "branch" or "region", the assistant reads it as **where our customers are located**
(their state or country) and will say so in its answer. If you actually meant our
**warehouses / distribution centers**, say that word and it will use those instead.

## Saved reports

Every successful answer is saved automatically as a report under your name. You can ask
things like "delete all reports mentioning Acme Corp".

Deleting is deliberately careful: the assistant first shows you **exactly how many** of
your reports match and a preview, then asks you to type a confirmation phrase **exactly as
shown**. Anything else cancels. You can only ever see or delete **your own** reports —
never a colleague's.

## Making it answer *your* way

- `/prefs format=table` — get answers as tables instead of bullet points
- `/prefs format=bullets tone=plain` — back to bullets, plainer wording
- `/feedback good` or `/feedback bad wrong numbers` — rate the last answer. Good examples
  you flag can be reviewed by an analyst and used to make future answers better for
  everyone.

The overall reporting style (the "company voice") is managed centrally — if leadership
changes it, you'll see the new tone automatically. Your personal `/prefs` settings always
win over the company default, for you only.

## What the assistant will NOT do — on purpose

- **It never shows personal customer data.** Emails, phone numbers, home addresses come
  back as `[REDACTED]`, always. This is not a malfunction and cannot be talked around —
  asking "just this once" or "ignore your rules" gets a polite refusal.
- **It doesn't send emails or make charts.** It tells you so if you ask. Copy the text into
  your own email if you need to share it.
- **It doesn't change any data.** It only reads. The only thing it can delete is your own
  saved reports, with your explicit confirmation.
- **It doesn't predict the future.** It reports what's in the data. If you ask about dates
  we have no data for, it will tell you which period *is* available instead of guessing.
- **It's not a general chatbot.** Weather, news, contract advice — outside its job.

## When something looks off

- **"No rows found… data covers 2019-01-01 to …"** — your question pointed at a period or
  filter with no data. The message tells you what range exists; adjust and re-ask.
- **"I could not run a safe query: …"** — the assistant tried a couple of times and
  couldn't get a valid answer. Rephrase the question more simply; if it keeps happening,
  send `/feedback bad` with a short note so the team sees it.
- **A weird or slow answer once** — just ask again. Every question is independent.
- **The session crashed or you closed the window** — start it again. Your saved reports,
  preferences, and even a pending delete confirmation survive restarts.

## Quick reference

| Type this | To get |
|---|---|
| your question in plain English | a short business report |
| `/schema` | what data exists (tables, fields, what's masked) |
| `/prefs format=table` or `format=bullets tone=...` | your personal answer style |
| `/feedback good` / `/feedback bad <why>` | rate the last answer |
| `/help` | the command list |
| `/exit` | quit |

*Questions about access or setup: contact your IT/data team. This guide covers use only.*
