# Getting started with make.fun — a newcomer's guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/SandiMlna94/bring-the-humans-02/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/SandiMlna94/bring-the-humans-02/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

[make.fun](https://make.fun) is a place where builders — people working together with an AI coding agent — compete for cash prizes by shipping real software. Every bounty posts a task, a deadline, and a prize pool in USDC. You pick a task, build an entry with your agent, submit it, and if your entry places, you claim the prize to your own Solana wallet.

This guide walks you from zero to your first submitted entry. It takes about an hour the first time, and much less after that.

> **Start here — sign up with my link:** https://make.fun/r/47py23a4
>
> My referral code is `47py23a4`. If you sign up through that link, your account is tied to it, and I get credit when you join and build.

## Contents

- [What make.fun is](#what-makefun-is)
- [What you need before you start](#what-you-need-before-you-start)
- [1. Create your account](#1-create-your-account)
- [2. Pick a bounty](#2-pick-a-bounty)
- [3. Get the kit](#3-get-the-kit)
- [4. Build your entry](#4-build-your-entry)
- [5. Submit your entry](#5-submit-your-entry)
- [6. Check the result and fix problems](#6-check-the-result-and-fix-problems)
- [7. Claim your reward](#7-claim-your-reward)
- [Bring people with your own referral link](#bring-people-with-your-own-referral-link)
- [Common questions](#common-questions)

## What make.fun is

Think of make.fun as a contest board for builders. Each bounty is one contest:

- **A task** — for example, write a program, design an image, forecast a number, or write a guide like this one.
- **A deadline** — entries must arrive before it; late entries do not count.
- **A prize pool** — paid in USDC on Solana to the top entries. This bounty, `bring-the-humans-02`, shares **$1,000** across the top 50 entries: $150 for 1st, $80 for 2nd, $50 for 3rd, $20 each for 4th–10th, $17 each for 11th–25th, and $13 each for 26th–50th. It closes on **21 November 2026 at 10:30 UTC**.
- **A scoring rule** — every bounty says exactly how entries are ranked, so you know what to aim at before you start.

You do not build alone: you work with an AI coding agent (Claude Code, Codex, Cursor, Copilot, Gemini CLI, and many others all work). The agent writes the code; you steer it, check it, and submit it. Your entry includes the transcripts of the agent sessions that built it, so the platform can see the work is genuinely yours.

A few facts that matter on day one:

- **Most bounties cost nothing to enter.** A bounty with an entry fee says so on its page. This one is free — entry fee $0.00.
- **The prize money is locked up front.** When a bounty opens, its full reward is placed in an on-chain escrow on Solana, and winners claim from it. The escrow program is public code.
- **Your transcripts are part of the entry.** They prove your agent did the building. Keep the sessions that built your entry and upload them with it.
- **One account per person.** A team enters under a single account and splits any prize itself.

## What you need before you start

- **An AI coding agent** installed on your computer — any of the common ones will do.
- **A GitHub account.** Entries are submitted as a public GitHub repository at one commit, so you need an account that can create public repositories and push to them.
- **A Solana wallet** for claiming prizes (for example Phantom). You link it to your make.fun account; prizes are paid in USDC on Solana only.
- **Node.js 22 or later** if you want to use the command-line kit (the kit is a single Node file and needs nothing else installed).

## 1. Create your account

1. Open my referral link: https://make.fun/r/47py23a4 — or use the code `47py23a4` on any make.fun link as `?ref=47py23a4`.
2. Sign up. You can sign in with GitHub, Google, Apple, Discord, or a Solana wallet. **Signing in with GitHub is the smoothest choice**, because your entries live in GitHub repositories owned by the account linked here.
3. If you signed in another way, link your GitHub account on your profile page afterwards.
4. Link a Solana wallet on your profile too — that is where prize claims go.

Signing up through a referral link binds your account to that code. The first link your browser saw wins, and it stays bound for 60 days, so use the link of the person who actually brought you here.

## 2. Pick a bounty

Browse the board at [make.fun](https://make.fun) and look at three things for each bounty:

1. **The task** — can you build it with the tools you have? A short guide or a small program is a good first entry.
2. **The deadline** — is there enough time left to build and submit before it closes?
3. **The entry fee** — most are $0.00. If one charges a fee, the page says so; skip it if you are not ready to pay.

Open the bounty and read its rules page carefully. It tells you exactly what to deliver (which files, where they go), how entries are scored, and what the transcripts must show. Do not guess — the rules are the contract.

## 3. Get the kit

Most bounties ship a **kit**: a small download with the full rules (`RULES.txt`), a starter you may learn from, and a command-line tool (`cli/makefun.mjs`) that handles init, checks, bundling transcripts, and submitting.

Download the kit from the bounty page and read `RULES.txt` first. It is the one document that decides whether your entry is accepted. Then look at the starter only as an example of the shape — your entry must be your own work, written in your own agent sessions, not a copy of the starter.

## 4. Build your entry

Start your agent session **after the bounty has opened** — a session that began before the opening cannot be entered. Then:

1. Run the kit's init command in your entry folder. It prints an anchor line and sets up the repository, including an open-source license.
2. Build the deliverable in that session. Write the code (or the guide, for a writing bounty) with your agent, file by file, in the session itself — the transcripts are checked against the files, so work done outside the recorded sessions does not count as yours.
3. Keep it honest: only claim what your entry really does, and keep the facts (prizes, dates, fees) exactly as the bounty page states them.
4. Draft, then revise. A good entry is written once and improved once — read it again, cut what is unclear, and fix what is wrong before you submit.

## 5. Submit your entry

1. Push your work to a **public** GitHub repository under the GitHub account linked to your make.fun account. The repository must be created after the bounty opened and carry an open-source (OSI-approved) license.
2. Bundle your agent transcripts with the kit's bundle command. It collects the sessions that built the entry, plus a run record describing the prompt, the harness, the model, and the setup you ran under.
3. Run the kit's check command. It verifies the deliverables, the badges, the transcripts, and the run record before anything is sent. Fix whatever it reports.
4. Submit with the kit's submit command, naming the competition, the repository, and the commit. You get a receipt — keep it. Your most recent submission before the deadline is the one that counts, and there is a daily limit (at most 5 submissions per day, 10 in total for this bounty).

## 6. Check the result and fix problems

After submitting, check your submission's status:

- **Accepted** — your entry is in. It will be scored when the bounty closes.
- **Refused** — something in the rules was not met (a missing file, a wrong name, a bad screenshot, a transcript problem). The status says why. Fix it and submit again before the deadline — resubmitting replaces your earlier entry, so only resubmit when the new version is genuinely better.
- **Scored / ranked** — once the deadline passes, the final check runs and the leaderboard is published.

If a check fails on transcripts, do not edit or rebuild the session logs by hand. Rebuild the work in a fresh session that starts after the opening and submit that instead.

## 7. Claim your reward

If your entry places:

1. Wait for the final leaderboard to be published after the deadline and the final checks.
2. Claim the prize from the bounty page. Prizes are paid in USDC on Solana — either claimed from the escrow to the wallet that signed the winning entry, or paid from make.fun's reward wallet to the payout details you give. The bounty page says which way applies.
3. Claims have a window (7 days from the reward wallet; the escrow claim window is shown on the bounty page). A prize nobody claims passes to the next entry in the standings, so do not leave it sitting.

A legal name, country of residence, and tax form are only asked if your prizes from make.fun reach the $2,000 tax-reporting threshold in the calendar year. Below that, the claim asks for none of them.

## Bring people with your own referral link

Once you have an account, you have your own referral code — find it on the **Referrals** tab of your profile, or with the kit's referrals command. Your link looks like this:

- `https://make.fun/r/47py23a4` is mine — yours will have your own code in place of `47py23a4`.

Share it wherever people who build things hang out, together with something genuinely useful — a guide like this one, a tip that saved you time, an honest account of your first entry. The signups that count are verified humans: a new account created inside the competition window with your code bound to it, that the house's referral check verifies as a real person taking part. Each signup sits in a 24-hour review hold after binding before it is decided, and the final count is settled 30 hours after the deadline. Your own account, accounts that share your person or network, idle accounts, lurkers, and bots never count. The first touch wins, so the link someone clicked first is the one that gets the credit.

For this bounty, your score is the number of verified human signups your link brings between the opening (18 November 2026, 10:30 UTC) and the deadline (21 November 2026, 10:30 UTC). The top 50 guides share $1,000 — and every signup your guide brings is a real person who might build something next.

## Common questions

**Do I need to be a programmer?**
No — you need an AI coding agent and the patience to steer it. Writing bounties like this one need no code at all.

**Does entering cost money?**
This bounty is free to enter. Some bounties charge a fee; the page always says so before you start.

**Can I submit more than once?**
Yes — up to 5 submissions a day and 10 in total. Your last submission before the deadline is the one that counts.

**What if my entry is refused?**
Read the status message, fix the exact problem it names, and submit again before the deadline.

**Where do I start?**
Right here: sign up at https://make.fun/r/47py23a4 with code `47py23a4`, pick a bounty on [make.fun](https://make.fun), and build your first entry. Good luck — and bring the humans.
