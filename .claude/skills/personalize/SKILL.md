---
name: personalize
description: Write a version of each campaign email for every lead group in leads/leads.csv. Use when a campaign's emails are final and you want one copy per group.
argument-hint: "[campaign folder]"
context: fork
allowed-tools: Read, Glob, Grep, Write
---

# Personalize

Write one version of each campaign email for each lead group.

## 1. Check the input

- The argument is a campaign folder, such as `campaigns/agent-factory-2e-launch`.
- **If no folder is given,** or the folder has no `emails/` folder inside it, stop. Use Glob with `campaigns/*/emails/*.md` to find the campaign folders that have emails, list them, and ask which one to use. Don't write anything.

## 2. Read what you need

1. **The emails:** every file in `<campaign folder>/emails/*.md`. Don't read files under `groups/`.
2. **The groups:** read `leads/leads.csv` and collect the distinct values in the `group` column. Use exactly the groups you find. Today they are `student`, `manager`, `founder` and `trainer`, but always read the file instead of trusting this list.
3. **The rules:** `brand/voice.md` and `.claude/rules/emails.md`. Every version must follow both.
4. **The audience:** the "Target audience" table in the campaign's plan, if there is one (for example `campaigns/plan_agentfactory2.md`). Use it to learn what each group wants and worries about.

## 3. Write one version per email, per group

For each email and each group, copy the email and change **only two things**:

1. **The opening line,** meaning the first sentence after `Hi {{first_name}},`. Rewrite it so it speaks to that group's situation.
2. **One example** in the body. Swap one example, or one sentence of illustration, for one that fits the group. For example, a study task for `student`, a weekly team report for `manager`, a process to scale for `founder`, or a class exercise for `trainer`. If the email already has a list with a line per group, keep only the line for this group, or reword it for this group.

**Keep everything else exactly the same:**

- The `Subject:` and `Preview:` lines
- `Hi {{first_name}},`
- The structure: the same paragraphs and lists in the same order
- The main link, its text and how many times it appears
- The sign-off and the two-line footer, as plain text

**Never add:**

- Real names or real addresses
- New links
- Claims that `brand/voice.md` forbids
- Facts about the book that aren't already in the original email

Keep each version under 250 words.

## 4. Save the files

Save each version to `<campaign folder>/groups/<group>/emails/<same file name>`. For example, `campaigns/agent-factory-2e-launch/groups/student/emails/01-five-horizons.md`.

Overwrite an existing version only if it's in that exact path.

## 5. Reply with a short summary only

Reply with nothing but:

- **How many files** you wrote: emails × groups, such as "Wrote 16 files (4 emails × 4 groups)".
- **One example opening line per group,** taken from the first email.

Don't paste the full emails or explain the process.
