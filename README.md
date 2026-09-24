<img src="assets/banner.png" alt="NIGHT: a student building with AI to create useful products and solve real problems" width="100%">

Hi, I'm Night. I'm a student who builds software with AI.

I've been using AI for about four years. At first I just used it. Then I wanted to know why it
works when it works and why it fails when it fails, and I've been digging into that ever since:
how prompts shape the output, which models are good at which jobs, what benchmarks tell you and
what they leave out, how much reasoning effort a task actually needs, and why a model gets worse
as its context fills up. The projects below are where I test all of that on real problems.

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

## What I've learned so far

These are the ideas that changed how I work. I keep notes on each one in my study vault.

- A model's useful context is much smaller than its advertised window. Accuracy drops long
  before the limit, so I keep sessions short, hand exploration to subagents, and restart from
  written notes instead of dragging a long chat along.
- Instructions that load on every turn cost attention on every turn. My CLAUDE.md stays short.
  Anything situational goes in its own file with a one-line pointer, or in a skill that only
  loads when it's needed.
- Pick the model and the effort level for each task. Bulk mechanical work goes to a small, fast
  model. Architecture and hard bugs get the strongest model at high effort. There's no magic
  "think harder" phrase; effort is a setting.
- Agents are reliable when there's a clear check to hit: a failing test, a build, a benchmark.
  They're unreliable at anything that depends on context only I have, and at deciding when
  they're done. So I write down what "done" means before any code gets written.
- Code should be reviewed by a different model than the one that wrote it. A fresh session of
  the same model drops its bias toward its own work, but it keeps the same blind spots.
- Code can be regenerated from a clear spec. The reasons behind a decision can't be regenerated
  from anything. So I keep specs and decision records, and treat the code as the cheaper of
  the two.
- Guard actions by whether they can be undone, not by how big they look. Deleting
  `node_modules` is fine. A force-push isn't.

Right now I'm working through Python fundamentals and the math behind machine learning,
because I want to be able to read and judge the code my tools write.

If something in one of these repos is broken or unclear, open an issue.
