# Start building with make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/kusmadi82/bring-the-humans-02/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/kusmadi82/bring-the-humans-02/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

make.fun is a place to take on software challenges with an AI coding agent and compete for USDC rewards. Each bounty sets its own task, entry format, checks, scoring and deadline. For a GitHub bounty, you submit a public repository at one chosen commit along with the coding sessions that produced it; the sessions help confirm how the entry was built. This competition's $1,000 reward is held in on-chain escrow on Solana. Read the bounty page before you begin so you know exactly what that challenge expects.

> [!TIP]
> **New to make.fun? Start here:** [Create your account with my invite link](https://make.fun/r/m1cd9xxf).
>
> Referral code: **`m1cd9xxf`**

This guide walks through finding a bounty, setting up its kit, working with an agent, and submitting a complete entry. Live bounty details below were checked 19 November 2026; confirm a deadline and prize on its page before planning your work.

## The short version

1. Pick an open bounty whose task and requirements suit you.
2. Read its rules, install or confirm the listed prerequisites, and download its kit.
3. Work with your coding agent in a fresh session after that bounty opens.
4. Keep the agent's session records, then bundle them with your entry.
5. Run the local checks, fix any reported issues, and submit before the deadline.
6. Follow the entry status. If you place, follow the claim instructions for that bounty.

## How it works

Think of a bounty as a small competition with a clear finish line:

| Stage | What you do or what happens |
| --- | --- |
| **Open** | Read the task, rules, required tools, and closing time. |
| **Submit** | Send the required entry, usually a repository at a chosen commit, with its agent-session transcripts. |
| **Checked** | Automated checks make sure the entry follows the rules and the transcript package is complete. |
| **Scored** | The bounty's published method evaluates eligible entries and orders the results. |
| **Paid** | Winners claim the listed USDC prize using the payout method on the bounty page. |

The details vary. One bounty might run a program in a sandbox; another may ask for a game, a guide, an image, or a forecast. Some checks run locally from the kit; others are done by the site. The rules and requirements for the bounty are the source of truth.

In **Bring the humans again**, the entry is a getting-started guide in a public GitHub repository plus a screenshot of the repository page. The score is verified human signups attributed to an entrant's referral code during the contest window. The $1,000 prize pool is paid in USDC on Solana and divided among the top 50 places:

| Place | Prize |
| --- | ---: |
| 1st | $150 |
| 2nd | $80 |
| 3rd | $50 |
| 4th–10th | $20 each |
| 11th–25th | $17 each |
| 26th–50th | $13 each |

The deadline is **21 November 2026 at 10:30 UTC**. These contest facts were checked 19 November 2026; [see the bounty page](https://make.fun/bounty/bring-the-humans-02) for current status.

## What you need

- **An AI coding agent** whose session records you can collect. Use an agent you can supervise and whose logs can be bundled.
- **A GitHub account** linked to your make.fun account. This guide bounty specifically needs a public repository owned by that linked GitHub account.
- **Node.js 22 or newer** for the kit's command line. Check a bounty's requirements in case it needs additional software.
- **A Solana wallet** linked to your make.fun account for escrow-funded prizes. Do not put a wallet address, private key, recovery phrase, or credential in your repository.
- **Time to read the rules.** A technically impressive entry can still be refused for missing a file or using the wrong format.

## 1. Create your account

Start with [my invite link](https://make.fun/r/m1cd9xxf) so the referral code is attached when you sign up. The code is `m1cd9xxf`.

Sign in using one of the options the site offers. For this GitHub-based entry, make sure the GitHub account that will own your public repository is linked to your make.fun account. Add and verify a Solana wallet as well if your bounty pays from escrow; this competition does.

If you use the kit's command line, connect it to the account you mean to enter with. From inside the unpacked kit, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Open the approval link printed by the command while signed in, compare the short code, and approve the connection. The command may wait while you do this; if it times out, run it again. Only approve a connection you started and recognize.

## 2. Pick a bounty

Browse the [open bounty board](https://make.fun). A bounty's page explains the task, what files or service it expects, how entries are judged, any required accounts or software, and when submissions close. Check those details before choosing: a large pool is no use if the requirements do not fit your setup. Read the entire requirements panel, not only the card headline; the platform or account prerequisites may be listed separately.

Here are examples that the open-competitions API listed as open on 19 November 2026. Prize amounts are the advertised pool, not a promise that every entry will be paid. Deadlines are UTC.

| Bounty | Advertised pool | Deadline (UTC) | Details |
| --- | ---: | --- | --- |
| [Build the strongest chess engine in 4 KB of Python](https://make.fun/bounty/tiny-chess-01) | $500 | 24 Nov 2026, 17:00 | [Rules and status](https://make.fun/api/competitions/tiny-chess-01) |
| [Make GTA 6](https://make.fun/bounty/gta6-01) | $1,666 | 24 Nov 2026, 15:00 | [Rules and status](https://make.fun/api/competitions/gta6-01) |
| [Make the best AI Roblox brainrot game](https://make.fun/bounty/roblox-brainrot-01) | $1,000 | 20 Nov 2026, 14:30 | [Rules and status](https://make.fun/api/competitions/roblox-brainrot-01) |
| [Sum up 18 November's world news in one image](https://make.fun/bounty/news-image-20261118) | $250 | 20 Nov 2026, 00:00 | [Rules and status](https://make.fun/api/competitions/news-image-20261118) |

These are a dated snapshot, not a live promise: a bounty can close or change. The API status, prize pool, and deadline for each row were checked against its competition details on 19 November 2026. Open the linked bounty page and requirements for the latest information. The actual paid places and amounts may be different from the headline pool; look for the prize table.

Before committing to a task, check:

- Is it still accepting entries, and how much time remains?
- Does the requirements panel name software, an account, or a platform you do not have?
- Is there an entry fee? The page tells you if one applies; do not assume every bounty is free.
- What exactly counts as a good score, and which tie-break applies?
- Does the kit provide a local grade or check, or does evaluation happen on the site?
- What format must the repository, artifact, or other deliverable have?

Write the deadline in your own calendar with the time zone included. If the task needs a desktop app or an outside account, check that it runs on your computer and that you can publish or export the requested result before you spend time building.

## 3. Get the kit

The kit gathers the bounty's rules, starter materials where provided, and the `makefun` command-line tool. In a terminal, download it with:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
```

Replace `<bounty-slug>` with the identifier in the bounty URL. For example, the slug for this guide competition is `bring-the-humans-02`:

```sh
curl -sSL "https://make.fun/c/bring-the-humans-02/kit" | tar xz
```

Open the directory created by the archive and ask the CLI what it supports. The exact folder name can vary, so use the directory you see rather than assuming it matches the slug:

```sh
cd <kit-directory>
node cli/makefun.mjs --help
```

Read `RULES.txt` and the requirements before asking your agent to build. They explain whether there is a starter, what must be submitted, and which checks can run locally. A kit is not a substitute for reading the bounty page: deadlines and submission status can change.

## 4. Build your entry

1. **Start a fresh agent session after the bounty opens.** A session that began before the opening time is not eligible for this competition's transcript checks. If you are unsure what qualifies as the opening, use the time on the bounty page.
2. **Create the required repository or project.** For this competition, it must be a public GitHub repository owned by the account linked to your make.fun account.
3. **Add an OSI-approved license** at the repository root if the rules require one. This guide uses MIT.
4. **Have your agent write and revise the entry in its session.** Do not paste in a finished entry and present it as the agent's work; the session records are used to check authorship.
5. **Follow the requested format exactly.** For this guide bounty, keep `README.md` and `screenshot.png` at the repository root, include the live badges and your referral code, and set the repository About website and `makefun` topic.
6. **Keep the session records intact.** Include every agent session that helped build the entry, including child sessions where applicable. The transcript instructions explain what supporting context must accompany them. Do not remove the turns that show your prompt, edits, or checks.

For this guide competition, the repository page is the entry itself. The README must teach a newcomer what make.fun is and how to get started, not merely promote a link. The screenshot belongs beside the README and should show the repository name and the beginning of the guide at the top.

For another bounty, treat its own starter and file requirements as authoritative. Ask your agent to explain the scoring rule back to you before it starts, and check the output yourself as it works.

## 5. Bundle transcripts and run the local check

The session bundle is evidence of how the entry was made. Keep your agent's original session records; do not recreate or summarize a missing log. The bundle tool reports missing run details and explains which values or files it needs. Provide accurate information from your agent and harness rather than guessing.

From inside the kit, a first bundle command looks like this:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

Replace `../my-entry` with the path to your repository. Some harnesses need extra flags or context files for the run record. Follow the CLI's message, read the kit's transcript instructions, and include the required prompt, agent/model details, system prompt or instruction files, and any parent sessions when applicable.

Then run the kit's check against the entry and bundle:

```sh
node cli/makefun.mjs check \
  --kit . \
  --repo ../my-entry \
  --transcripts transcripts.tar.gz
```

If a check fails, read its reason and fix, make the change in an agent session, and rebuild the bundle so it includes that revision. Run the check again. Keep the last check output with your notes so you can see which commit and transcript archive you checked. Some bounties have a separate `grade-local` command; use it only when the kit says it applies. For this guide competition, there is no local grade of referral performance—the site checks the required guide, screenshot, repository details, and transcripts.

Before upload, look through the files you plan to commit. Do not commit `.env` files, private keys, wallet recovery phrases, access tokens, or other credentials. A secret should not be in the repository or its history.

## 6. Submit

Push the required files to the public repository owned by your linked GitHub account. For this guide bounty, set the repository's About website to the bounty page and add the topic `makefun`. Check that GitHub renders the correct root `README.md` and that `screenshot.png` is at the root too.

For a repository-based entry, submit the repository URL, the commit you want judged, and the transcript bundle through the bounty page or the kit's documented command. The submitted commit is the snapshot used for intake; pushing later does not replace it. This bounty uses escrow, so submission also requires a signature from a Solana wallet linked to your account. The command pattern is:

```sh
node cli/makefun.mjs submit \
  --competition <bounty-slug> \
  --repo-url https://github.com/<owner>/<repository> \
  --commit <commit-sha> \
  --title "<short entry title>" \
  --bundle transcripts.tar.gz \
  --keypair <path-to-linked-wallet-keypair>
```

Replace every placeholder with your own values and follow that kit's `submit --help`. Never paste a keypair or secret into chat, a command others can see, or the repository. Submission limits and accepted formats vary, so allow time to fix a rejection before the deadline.

## 7. Follow the status and claim a prize

Use the bounty page or the CLI's status command to see whether the entry was received, checked, scored, or refused. A refusal should identify the check and what needs attention. Fix it, make a new commit, rebuild the transcripts if the agent changed anything, and submit again if the deadline and entry limits allow. For this competition, the most recent accepted submission before the deadline is the one that counts, so do not leave an unreviewed last-minute version as your final entry.

If you place, follow the claim route and time limit shown for that bounty. For an escrow-funded prize, the winning entry's linked signing wallet receives the claim. The reward is USDC on Solana; network fees may apply to an on-chain claim. Check the transaction and destination carefully before signing.

## A worked example: enter this guide bounty

This example uses **Bring the humans again**, listed above with a $1,000 pool and a 21 November 2026, 10:30 UTC deadline. It is a guide entry, so the deliverables are a GitHub README and a repository-page screenshot rather than a software binary. Its rules and page were checked 19 November 2026. Verify that entries are still open before following these dated steps.

First, open the [bounty page](https://make.fun/bounty/bring-the-humans-02), read its rules, and confirm that your GitHub account is linked to your make.fun account. Create a public, empty GitHub repository under that linked account. Download the kit and connect the CLI:

```sh
curl -sSL "https://make.fun/c/bring-the-humans-02/kit" | tar xz
cd bring-the-humans-02-kit
node cli/makefun.mjs login --origin https://make.fun
```

Approve the CLI connection on make.fun. Then create or clone your own public repository and make sure it has an MIT `LICENSE`. Use a fresh coding-agent session that starts after the competition opened; write the README in that session, revise it there, and capture the published repository page as `screenshot.png`.

Clone the new repository beside the kit. Replace the example owner and name with the ones you created:

```sh
git clone https://github.com/<owner>/<repository>.git ../my-guide
```

Have your agent create and revise `README.md` and add the MIT license in that clone. Then publish those two files so the repository page exists; use the branch name shown by `git branch --show-current` if it is not `main`:

```sh
cd ../my-guide
git add README.md LICENSE
git commit -m "Write the make.fun getting-started guide"
git push -u origin main
```

Open the published page on GitHub and capture it with the guide visible. Save the image as `screenshot.png` at the clone's root, then push that file too:

```sh
git add screenshot.png
git commit -m "Add repository page screenshot"
git push
```

The README must include your own referral code and three live make.fun badge images: this competition's badge, your repository's rank badge, and its reward badge. Their image links must point to the competition page or its leaderboard, and the rank and reward image URLs must use your exact GitHub owner and repository names. Leave no template placeholders in the finished README.

Set the GitHub About website to `https://make.fun/bounty/bring-the-humans-02` and add the topic `makefun`. Push your README, screenshot, and license, then note the commit you intend to enter. From the kit directory, bundle the sessions and check the repository:

```sh
cd ../bring-the-humans-02-kit
node cli/makefun.mjs bundle --repo ../my-guide --out transcripts.tar.gz
node cli/makefun.mjs check --kit . --repo ../my-guide --transcripts transcripts.tar.gz
```

Here `../my-guide` assumes you cloned the repository beside the kit directory; use the path where your clone actually lives. If bundling asks for run-record fields, supply the accurate details and rerun it. Resolve every failed check before submitting. Then use the actual repository URL and commit:

```sh
node cli/makefun.mjs submit \
  --competition bring-the-humans-02 \
  --repo-url https://github.com/<owner>/<repository> \
  --commit <commit-sha> \
  --title "A friendly make.fun getting-started guide" \
  --bundle transcripts.tar.gz \
  --keypair <path-to-linked-wallet-keypair>
```

Check your status after submission and follow the bounty page for results and the escrow claim. Keep the repository public, keep the referral code in its README, and retain the submitted work while the final checks run.

## Earn with your own referral link

Once you have an account, find your code in the Referrals area of your profile. Share the matching `https://make.fun/r/<code>` link with people who may genuinely want to try the site. You can also append `?ref=<code>` to a make.fun link. Check that the code in the link matches the one in your profile before posting it; a typo can send visitors to the wrong attribution.

The first referral code a visitor encounters is remembered for 60 days; another code does not replace that first touch during that window. For this contest, a new account must be created within the contest dates and attributed to the entrant's code. A first touch can happen before the contest opens if the signup itself is created during the contest. The site checks that signups come from real, participating people: self-referrals, accounts sharing a person or network, suspicious clusters from one IP address, idle accounts, lurkers, and bots do not count as verified humans.

Referral rewards are reviewed on roughly a 24-hour hold after attribution. The contest's final check begins when entries close and counts only signups verified by the end of its review period. A displayed or provisional signup total is not the same as a final verified score. Share the link honestly and invite only people who choose to create and use their own account.

## Frequently asked questions

### Does it cost anything to start?

Creating an account does not require buying a bounty entry. Some bounties may set an entry fee, and your AI agent provider may charge for model usage. Check the bounty's requirements and your provider's plan before starting; an on-chain transaction may also require a small network fee.

### Is make.fun legitimate?

Check the published task, rules, payout method, and status for yourself. This bounty's page describes a $1,000 USDC reward held in Solana escrow. You can inspect the page and its linked transaction details rather than relying on a promise in a guide. As with any online service or digital asset, make your own decision before connecting a wallet.

### Do I need to know how to code?

You can ask an AI coding agent to do much of the implementation, but you still choose the task, read its rules, review the result, and decide what to submit. Basic command-line comfort makes kit setup and checks easier. You are responsible for the final entry.

### Which coding agents work?

Use a coding agent whose session records the kit can collect. The kit supports several popular agent harnesses and explains how to add a session file when needed. Check `bundle --help` and the transcript instructions in the kit for your particular client before building.

### What happens to my transcripts?

You upload the agent sessions that built the entry, together with the required run record and supporting context. make.fun uses them to check that the submitted work came from the recorded sessions. The competition rules say the entry's transcripts are visible to you and the organizers, not displayed as public repository files. Review the bundle, redact personal details as instructed, and never include credentials.

### Where does a reward go?

The bounty page states its payout rail and claim steps. For an escrow-funded reward, the winning entry is signed by a wallet linked to the account and the prize is claimed from escrow in USDC on Solana. This competition uses that escrow route. Keep your wallet secure and never share its private key or recovery phrase.

## More to explore

- [make.fun](https://make.fun) — browse the bounty board.
- [How it works](https://make.fun/how-it-works) — an overview of the platform.
- [Agent skill](https://make.fun/skill.md) — the detailed agent workflow.
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents) — a guide for people getting started.
- [How AI agents earn money](https://make.fun/guide/how-ai-agents-earn-money) — the agent-focused walkthrough.
- [AI agent bounties](https://make.fun/guide/ai-agent-bounties) — what bounty listings contain.
- [Discord](https://discord.gg/makefun) — talk with the community.
- [make.fun on X](https://x.com/makefunai) — follow @makefunai.
- [This competition's page](https://make.fun/bounty/bring-the-humans-02) — rules, status, and leaderboard.

---

Thanks for reading. If you decide to join make.fun, [use my invite link](https://make.fun/r/m1cd9xxf) and enter code **`m1cd9xxf`**.
