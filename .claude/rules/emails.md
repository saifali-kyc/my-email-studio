---
paths:
  - "campaigns/**/emails/*.md"
---

# Rules for every email file

These rules apply to every email file in any campaign's `emails/` folder, and only to those files. Each email file must follow all of them.

## 1. Subject and preview lines

- The first line is `Subject: ...`, with the subject in 50 characters or fewer.
- The second line is `Preview: ...`, with the preview text in 90 characters or fewer.
- Count only the text after `Subject: ` and `Preview: `.

## 2. Greeting

- Greet the reader by name with `{{first_name}}`, for example `Hi {{first_name}},`.
- Never write a real name in its place.

## 3. One main link

- Each email has exactly one main link, written exactly like this:

  [Start reading free](http://agentfactory2.panaversity.org/five-horizons/)

- That same link may appear at most twice: once near the top and once just before the sign-off, as `brand/voice.md` asks.
- Don't add any other link. The only other link allowed is `{{unsubscribe_url}}` in the footer.

## 4. Sign-off and footer

- End with our sign-off from `brand/voice.md`, on two lines:

  See you in the next chapter,
  The Panaversity Team

- Right after the sign-off, add this two-line footer as plain text, not inside a code block:

  You're getting this because you joined The AI Agent Factory readers list.
  Panaversity, {{company_address}} · Unsubscribe: {{unsubscribe_url}}

- Nothing comes after the footer.
