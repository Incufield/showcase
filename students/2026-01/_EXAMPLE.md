---
display_name: "Example Student"
github_handle: "example-student"
cohort: "2026-01"

project_title: "Inbox triage bot for a small support team"
summary: "Sorts incoming support email into three queues and drafts a first reply, so a two-person team stops reading every message by hand."

repo_url: "https://github.com/example-student/inbox-triage"
demo_url: "https://www.loom.com/share/example"
thumbnail: "assets/2026-01/example-student.png"

tags:
  - n8n
  - llm
  - email

published: false
---

## The problem

A two-person support team read every message that arrived, then decided who
should answer it. Most messages were one of three kinds, and the sorting alone
took about an hour a day.

## What it does

New mail is classified into billing, technical, or other. Billing and technical
go to the right person with a suggested reply already drafted. Anything the
classifier is unsure about goes to a human queue untouched.

The draft is never sent automatically. A person always approves it.

## How it works

- Trigger: new message in a shared Gmail inbox
- Steps: fetch, classify, route, draft, notify
- Tools used: n8n, Gmail API, an LLM for classification and drafting

## What I learned

My first version tried to answer everything and got confident answers wrong.
Adding an "unsure" path made it useful. Next time I would measure accuracy
before building the drafting step, not after.

