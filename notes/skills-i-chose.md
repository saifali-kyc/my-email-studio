# Skills I chose

Checked on 3 Nov 2026. Install and star counts come from skills.sh and GitHub listings on that day and will change.

**How the search was done:** the `npx skills find` commands couldn't reach skills.sh from Claude's cloud workspace, so every search returned "No skills found". That result was a network block, not a real empty result. The same searches were run on the skills.sh website instead. Run the four commands again on your own computer to see the live lists.

## Use these

1. **Anthropic's marketing plugin: `anthropics/knowledge-work-plugins`**
   - Covers writing the campaign: its `email-sequence` skill plans and drafts multi-email sequences, and the plugin also has campaign planning and brand review.
   - The publisher is official (Anthropic), the GitHub repo has about 34.2K stars, and the email-sequence skill has about 3K installs.
   - Step 2 of the assignment installs this plugin for the project.

2. **Resend's own skills: `resend/resend-skills`**
   - Covers sending the email: it sends single and batch emails (up to 100 per request), with retries and protection against duplicate sends.
   - The publisher is official (Resend runs the email service itself), and the GitHub repo has about 174 stars. That's a small number, but it comes from the company that runs the service, so it can be trusted.
   - Its documentation also links to Resend's remote MCP server, which Step 9 uses.

Runner-up for writing: `coreyhaines31/marketingskills`, skill `emails`, with about 83K installs and 58.1K stars from a well-known marketer. Note that it is now called **emails**. Older guides call it **email-sequence**.

## Avoid these

1. **`jwtappert/marketingskills`, skill `email-sequence`**
   - It has about 2 installs, and skills.sh shows no star count for it.
   - Its repo name copies the popular `marketingskills` repo, and the page doesn't say whether it's a fork or who maintains it. A copy can drift from the original, or have things added to it.

2. **`atxinsky/skills`, skill `email-sequence`**
   - It has about 3 installs and 5 GitHub stars, and it was first seen in May 2026.
   - It's a one-person collection with no track record. The official and well-known options do the same job.

Note: some small repos also have a "resend" skill. For example, `renatoasse/opensquad` has 2.2K stars but only 16 installs. Use Resend's own skill for sending.

## How I decided

Check these three things before installing any skill:

1. **Who publishes it.** Prefer the official maker of the tool, such as anthropics for Claude or resend for Resend, or a well-known author. Check that the owner name is the real one and not a look-alike.
2. **Whether installs and stars agree.** Install counts can be inflated. Many installs with very few GitHub stars is a warning sign. A real, active GitHub repo with stars and recent updates is harder to fake.
3. **What it can do on your machine.** Read the SKILL.md and any scripts before installing, and look for the security audits on its skills.sh page (Gen Agent Trust Hub, Socket, Snyk). Be careful with any skill that runs commands, sends email or asks for API keys.
