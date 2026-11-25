---
name: ralph
description: Installs Ralph, a desktop app that drafts replies to your unread Gmail in your own voice and sends one only when you click Send. Use when someone asks to install, set up, get or update Ralph.
---

# Install Ralph

Publish the app in `assets/ralph.html` as an Artifact in the person's own account, so it runs on their own connectors and their own Claude.

## Steps
1. Check the Gmail connector is connected. If it is missing, say how to add it (Plugins in the left sidebar, then Connectors, then Gmail, then Add) and publish anyway; the app shows its own setup screen.
2. Copy `assets/ralph.html` into the working directory unchanged, with one `cp` command. If the person is asked to allow the command, tell them it only copies the app file. Read the whole file first. Don't edit, restyle or "improve" it.
3. Publish it with the Artifact tool: `file_path` the copied file, `icon` "mail", `description` "Drafts replies to your unread email in your voice and sends one only when you click Send.", and `capabilities` exactly:
   ```json
   {"desktop": {}, "mcp": {"servers": [{"server": "Gmail", "tools": ["search_threads", "get_thread", "reply", "unlabel_thread"]}]}, "sample": {}, "db": {}, "user": {}}
   ```
4. Tell the person:
   - **How to install it:** open the artifact in the Claude desktop app (Mac or Windows, latest version), right-click it or open its title menu, and choose "Install as app". It then opens from the Dock or Start menu like any other app.
   - **What it will ask permission for:** their Gmail connector (it reads unread mail, and it looks through sent mail from the last two years to find about 20 emails they wrote, to learn how they write); Claude, on their own plan, to write the summaries and drafts; and a hotkey, a floating window and a menu bar item.
   - **What it never does without a click:** it never sends an email until they click Send. After a reply is sent it marks that email as read. It cannot delete, forward or start a new email. They can say no to any permission.
   - **Good to know:** the card shows a one-line summary written by AI, not the whole email, so for anything important they should click "Open in Gmail" and read the real email before they send. The app has an optional "Support the creator" button that opens Spencer Tribe's Stripe donation page.

## Updating
If the person already has a copy, find it with the Artifact tool's list action (an artifact they own, titled "Ralph"), tell them which one you found and get a yes, then publish to that same `url` so their saved settings carry over. Never publish over an artifact that is not Ralph. Do not create a second copy.
