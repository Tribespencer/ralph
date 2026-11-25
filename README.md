# Ralph

**A little app that writes your email replies for you. You read it. You click Send.**

Ralph lives on your desktop. When you get an email, Ralph tells you what it says in one line. Then it writes a reply that sounds like you. Nothing is sent until you click **Send**.

It is free. I made it with Claude. It is not made by Anthropic or Google.

## What you need

- The **Claude desktop app** on a Mac or Windows computer. Get the newest version.
- A **Gmail** account.

## Get Ralph in 5 steps

**Want pictures? Follow the [step-by-step guide](https://spencers-website.vercel.app/workflows/ralph).**

1. **Get the file.** Click here: **[Download ralph-skill.zip](https://github.com/Tribespencer/ralph/releases/latest/download/ralph-skill.zip)**. It goes to your Downloads folder. Don't open it.
2. **Give it to Claude.** Open the Claude app. Click **Plugins** on the left. Click **Add**, then **Upload plugin**. Drag the file in. Click **Upload**.
3. **Connect Gmail.** On the same Plugins page, click **Connectors**. Find **Gmail**, click **Add**, and sign in to Google. If Gmail is already there, skip this.
4. **Ask for Ralph.** Click **New**. Type `Install Ralph` and press Enter. If a box says **Claude wants to run a command**, click **Allow once**. Wait about a minute. Claude makes the app.
5. **Put it on your desktop.** Right-click the app Claude made. Click **Install as app**. Click **Install**.

Now open Ralph like any other app and click **Get started**.

## How to use it

1. Read the one-line **gist**. That is what the email says.
2. Read the reply Ralph wrote. Change any words you want.
3. Click **Send**. Or click **Skip** to leave that email alone.

## What Ralph can do, and what it can't

Ralph can:

- read your unread email
- look through your sent mail from the last two years to find about 20 emails you wrote, so it can learn how you write
- send a reply, only when you click **Send**
- mark that email as read after you send

Ralph can't:

- send anything without your click
- delete an email, forward an email, or start a new email

Where your email goes: to Gmail and to your own Claude. That's all. None of it comes to me.

## Good to know

- Ralph shows you a short summary, not the whole email. AI wrote the summary, so it can be wrong, and a tricky email can fool it. For anything important, click **Open in Gmail** and read the real email first.
- Ralph uses your Claude plan. Each summary and draft counts toward your plan's limits.
- There is a **Support the creator** button inside the app. It opens my Stripe tip page. You never have to use it.
- "Install as app" is new and still in beta, so things may change.

## Get a newer Ralph

Download the newest file, upload it the same way, then type `Update Ralph`.

## For the curious

The whole app is one file: [`ralph/assets/ralph.html`](ralph/assets/ralph.html). You can read every line. Claude follows [`ralph/SKILL.md`](ralph/SKILL.md) to set it up in your account.

MIT licence. Made by [Spencer Tribe](https://spencers-website.vercel.app).
