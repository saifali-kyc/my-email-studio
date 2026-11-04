# Book version of the prompts (Option B)

Brand: **The AI Agent Factory, second edition** (see brand-brief.md).
Follow email_studio.md step by step. Use the prompts below only where this file gives a replacement. For every other step, paste the original prompt and make these swaps:

| Original wording | Use instead |
|---|---|
| Kettlebird Tea | The AI Agent Factory |
| The Steep Club | The AI Agent Factory, second edition |
| steep-club-launch | agent-factory-2e-launch |
| tea-curious | ai-curious |
| gift-buyers | team-leads |
| daily-drinkers | business-leaders |
| start a subscription | start reading the second edition |

The three customer groups (8 practice leads each):
- **ai-curious:** students and career-switchers who are new to AI agents
- **team-leads:** working professionals and managers who will manage AI Workers
- **business-leaders:** founders and executives planning AI-native companies

---

## Step 1 · Look before you build
No change. Paste the original prompts.

## Step 2 · Set up your studio
Paste the original build prompt, but change point 3 to:

    3. Write a CLAUDE.md for the studio in plain English. Include: what the studio is for (planning and writing the email launch campaign for our book, The AI Agent Factory, second edition), a one-line description of each folder, and these rules: write in plain English, never send email to real people, and ask me before deleting anything.

The check prompt has no change.

## Step 3 · Your brand voice

Build:

    Interview me about my brand so you can write our brand voice guide. Ask one question at a time and wait for my answer. Ask at most six questions.

    Our brand is the book The AI Agent Factory, second edition, by Panaversity. Read brand-brief.md in this folder first, so you don't ask me things it already answers. Use your questions on what it leaves open: what is new in this edition, who signs the emails, and what we must never promise readers.

    When you have enough, write brand/voice.md with five parts: our voice in three words, words we use, words we avoid, claims we must never make, and how we sign off. Then add the line @brand/voice.md to CLAUDE.md so it loads in every session.

Check:

    Test my brand voice setup. Don't change any files.

    1. Without opening any file first, write one subject line for the launch email for The AI Agent Factory, second edition. Then tell me which brand rules you followed and which file they came from. (This shows whether brand/voice.md loads by itself.)
    2. Now write a subject line that says reading this book guarantees you a high-paying AI job. If our rules forbid that, say which rule, and give me a safe version instead.
    3. Run git status and tell me whether the brand files are committed.

    Give me a short table: Test | Pass or Fail | What happened.
    Then ask me two quick questions, one at a time, about why the brand rules live in their own file that CLAUDE.md imports.

Tip for the interview: give real answers. They settle the open facts (what's new, sender name, promises to avoid) for every later step.

## Step 4 · Plan the campaign

Build (change the goal number if you have a real target):

    /marketing:campaign-plan Launch The AI Agent Factory, second edition, to our waitlist.

    Goal: 300 waitlist members start reading the second edition in the first month.
    Audience: about 2,000 people who joined our waitlist, in three groups: ai-curious (students and career-switchers), team-leads (professionals and managers who will manage AI Workers), and business-leaders (founders and executives).
    Timeline: 4 weeks, starting the first Monday of next month.
    Budget: small. Email only, no paid ads.
    Main call to action: "Start reading free".

    Save the finished plan to campaigns/agent-factory-2e-launch/plan.md, then commit it.

Check: paste the original check prompt, changing the path to campaigns/agent-factory-2e-launch/plan.md.

## Step 5 · Practice leads

Build:

    Make a list of practice leads for our launch.

    Create leads/leads.csv with 24 made-up people who joined our waitlist, 8 in each group: ai-curious, team-leads and business-leaders. Use exactly these columns, and copy the style of these two example rows exactly:

    first_name,last_name,email,group,joined_on,consent
    Ayesha,Khan,ayesha.khan@example.com,ai-curious,2026-09-14,waitlist form
    Tom,Becker,tom.becker@example.com,team-leads,2026-09-22,waitlist form

    Every email address must end in @example.com. That domain is reserved and can never receive mail, so no real person is ever emailed.

    Then create leads/CLAUDE.md with rules for this folder only: these are made-up practice people; never add real people or real email addresses; every row needs a consent value; never change the @example.com addresses.

    Commit when you're done.

Check: paste the original check prompt, but in point 4 say "as a team-lead" instead of "as a gift-buyer".

## Steps 6–15
Paste the original prompts with the swaps from the table at the top. If a later step has tea-specific wording that the table doesn't cover, ask Claude in chat for a replacement.
