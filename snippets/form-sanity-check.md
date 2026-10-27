# Form sanity check

The most common contact-capture defect we find: a page that says "fill out the form below" with no form on it (we have audited examples).

## 5-minute check

1. Open your contact page in a private window. Is there actually a form? Count the `<form>` tags in the rendered source.
2. Submit it yourself with a test entry. Did it land in the inbox/CRM within a minute? If it goes to a dead mailbox, it is a silent lead leak.
3. Check the success path: after submit, does the visitor see a confirmation, or a generic error?
4. Check spam folder rules / SPF+DKIM for the sending domain (this is the #1 silent killer of form email).
5. Mobile check: fields must be reachable without horizontal scrolling; the submit button must not sit under a sticky footer.

## If you use a form plugin or builder embed

- Verify the embed renders on mobile, not just desktop.
- Beware iframe embeds with fixed heights that clip the submit button on small screens.
