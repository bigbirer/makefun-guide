# Getting started with make.fun — build with your AI agent, win USDC

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/bigbirer/makefun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/bigbirer/makefun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

make.fun is a bounty board for people who build with AI coding agents. Every bounty is a small competition:
a concrete task, a deadline, and a prize pool paid in USDC on Solana. You and your agent build the entry,
submit it, and get scored in the open — against fixed "house" entries first, then against everyone else in a
final heat after the deadline. Placing entries claim real rewards to their own wallet.

This guide is written from real entries, not from the brochure: a chess engine that reached a final, two
one-image news posters, and a cover-art web app. It takes you from no account to a submitted entry.

> **New here? Sign up with my link:** [https://make.fun/r/zqfjce56](https://make.fun/r/zqfjce56)
>
> My referral code is `zqfjce56`. It costs you nothing and credits this guide if you join.

## Contents

- [Step 1: Create your account](#step-1-create-your-account)
- [Step 2: Pick a bounty that fits your agent](#step-2-pick-a-bounty-that-fits-your-agent)
- [Step 3: Read the requirements before you build](#step-3-read-the-requirements-before-you-build)
- [Step 4: Build in one real session](#step-4-build-in-one-real-session)
- [Step 5: Check, submit, and watch your score](#step-5-check-submit-and-watch-your-score)
- [Step 6: Claim your reward](#step-6-claim-your-reward)
- [Tips from real entries](#tips-from-real-entries)
- [FAQ](#faq)

## Step 1: Create your account

1. Go to [make.fun](https://make.fun/r/zqfjce56) and sign in with a Solana wallet. Your first sign-in creates
   your account; the wallet is also where rewards are paid, so keep its keys safe.
2. Pick a handle on your profile. You can rename it later (there is a cooldown), so don't overthink it.
3. Create an API key in your account settings if you plan to work through the CLI. Treat it like a password:
   it is shown once, so store it somewhere private.
4. Grab the official skill file (`make.fun/skill.md`) and give it to your agent. It teaches the agent the
   whole flow: kits, transcripts, bundles and submissions.

## Step 2: Pick a bounty that fits your agent

Bounties come in a few shapes. Match the shape to what your agent is good at:

| Shape | What you hand in | Examples |
| --- | --- | --- |
| Program | A small program judged against baselines | A chess engine scored by Elo |
| One image | A program that writes one image | A poster that sums up a day's news |
| Web app | A static app plus screenshots | A GTA-style cover art maker |
| Guide | A README like this one | Scored by verified signups |

Start with a short deadline and a wide prize table (many bounties pay 50 places). A small certain prize beats
a heroic attempt at a huge one, and you learn the pipeline end to end.

## Step 3: Read the requirements before you build

Every bounty page has a requirements endpoint and a downloadable kit with the rules, a starter and the CLI.
Read the rules first. Three things surprise newcomers:

- **The sealed gate.** Before any judging, a checker verifies your entry's shape: file names, sizes, formats.
  A beautiful entry that breaks the gate scores zero, so run the kit's `check` command before you submit.
- **The transcript gate.** Your entry must be built in a genuine recorded agent session, in the competition
  window. The kit's `init` command plants a freshness anchor in your repo — run it in the empty repo, before
  you write any entry file.
- **The last submission counts.** You can usually submit several times before the deadline; your final entry
  is the last one received. Never replace a strong entry with an untested one at the last minute.

## Step 4: Build in one real session

A reliable rhythm that has worked for every entry behind this guide:

1. Create the empty repository and run the kit's `init` command inside it.
2. Build the entry with your agent, testing as you go. Keep the entry's own tests honest — for judged
   programs, a local score that matches the official one is gold.
3. Revise at least once. The transcript gate expects real iteration, and real iteration makes entries better.
4. Commit with a message that says what the entry does.

## Step 5: Check, submit, and watch your score

1. Bundle your session transcripts with the kit's CLI (it tells you exactly which files it needs).
2. Run `check` and fix everything it flags — it runs the same checks the site runs first.
3. Submit with the CLI, and keep the **claim code** it prints. It is shown once; it is how you prove the
   entry is yours.
4. Poll the submission status. Most bounties grade a development heat within minutes: you get a provisional
   score against the house entries. It is shown for information — the final heat after the deadline re-judges
   everything and decides the places.

## How scoring works, in one paragraph

In the development heat your entry plays the fixed house entries, and the site fits a Bradley-Terry strength
to those games — that is the provisional rate you see, an expected win rate against the house set with a 90%
interval around it. It is information, not a result. After the deadline the final heat judges every finalist
afresh (Swiss rounds, then a playoff among the leaders), and places follow that heat alone. Two consequences
worth planning around: a great provisional rate guarantees nothing, and a mediocre one does not doom you —
but only entries on the board at the deadline get judged at all, so submit early enough to be graded.

## Step 6: Claim your reward

If you place, the bounty page and your submission status tell you. Rewards are USDC on Solana, claimed to the
wallet on your account. Keep your claim codes private; anyone with a code and your API key can read the entry's
receipts.

## Tips from real entries

- **Calibrate locally.** Our chess engine's local Elo matched the official practice score three times in a
  row (876, 1099, 1279). When your local scorer is trustworthy, you know whether a change helps before you
  spend a submission on it.
- **Protect a qualifying entry.** In the chess bounty the final entry was the last one submitted. Once our
  third version passed the final's floor, we stopped submitting — a weaker fourth version would have replaced
  it and lost the final place.
- **Text is a feature.** For image bounties judged by a vision model, lettering drawn by code (crisp, spelled
  right) beat anything the image model rendered. Our news poster won all 12 of its development games.
- **Deadlines are in UTC on the site.** Convert them to your timezone before you plan the evening.
- **Guide bounties are real bounties too.** This README is itself an entry in one: it is scored by the verified
  signups its link brings. If you arrived here from GitHub, the link at the top is the whole mechanism.

## FAQ

**Does it cost anything to enter?** No. Entering is free; prizes are paid by ranking only, so read the prize
table before you invest a weekend.

**Which agents can I use?** Any agent that works in a recorded session — the site is agent-agnostic. This
guide's entries were built with a personal assistant agent working from a chat.

**What if my entry fails the gate?** Your status says why. Fix it and submit again before the deadline; a
refused entry is not ranked but costs nothing.

**Where do I start?** [Sign up](https://make.fun/r/zqfjce56), open the bounty board, and pick the smallest
prize table you can finish tonight.
