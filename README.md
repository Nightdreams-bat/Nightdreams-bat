<img src="assets/banner.png" alt="NIGHT: a student building with AI to create useful products and solve real problems" width="100%">

Hi, I'm Night. I'm a student, and I build software with AI.

I don't write most of the code by hand. I describe what I want, plan it with the model,
read what it gives back, and test it until it works. I've been doing this on real projects
for a few years now, and the part I keep getting better at is knowing what to ask for and
when not to trust the answer.

## Projects

### [Kairo](https://github.com/Nightdreams-bat/kairo)

Cold email is mostly repetitive work: send, wait, follow up, read the replies, book a call.
Kairo handles that from a spreadsheet of leads. It sends the first email and up to three
follow-ups, and Claude sorts each reply into yes, no, maybe or question and drafts an answer.
Nothing goes out until you click approve. It installs on Windows like a normal app and
doesn't need a server.

### [supermarket-deals](https://github.com/Nightdreams-bat/supermarket-deals)

I didn't want to flip through four supermarket leaflets every week. This script checks about
1,100 offers from Lidl, Hofer, Spar and Norma in Linz each morning and sends a Telegram
message with whatever on my shopping list is discounted, plus the biggest price cuts. When
the site it first used shut down, I moved it to the JSON API behind another deals site.

### [pdf-craft](https://github.com/Nightdreams-bat/pdf-craft)

PDFs made by AI tend to look the same: Arial, a centered bold title, bullet points
everywhere. This Claude Code skill makes the agent pick a layout and fonts before it writes
anything, and it keeps a log so the next document gets a different style. It also checks the
finished file and fails if a font quietly fell back to Times.

### [claude-code-kit](https://github.com/Nightdreams-bat/claude-code-kit)

The setup I use for AI coding every day: 25 skills, 25 slash commands and 7 subagents for
Claude Code, plus a small script that runs several agents at once, each in its own git
worktree. Most of the ideas come from people who shared their own workflows, and they're
credited in the repo.

### [claude-skills](https://github.com/Nightdreams-bat/claude-skills)

17 Claude Code skills you can copy one folder at a time. The ones I wrote include a quiz
tutor that runs on an Obsidian vault and a check that looks for leaked API keys before you
push.

### [Trade Journal](https://github.com/mateitodirel/TradeJournal)

An offline desktop journal for traders, built together with
[@mateitodirel](https://github.com/mateitodirel). It tracks drawdowns and prop-firm payouts.

## What I'm learning right now

- Writing prompts that say what "done" looks like, so the model knows when to stop.
- Giving the model the right context before asking it for anything.
- Having a second model review the first one's work before I merge it.
- Checking the result myself with tests and screenshots, and scanning for secrets before
  anything goes public.

If something in one of these repos is broken or unclear, open an issue.
