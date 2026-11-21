# apple-app-review-skill

> Built at [Agniverse](https://agniverse.co), by [An Nayal](https://annayal.com) · more free tools at [annayal.com/open-source](https://annayal.com/open-source)

**Avoid an App Store rejection.** [GUIDE.md](GUIDE.md) is the full playbook: how App Review works, a map of the guidelines that cause most rejections (2.1, 2.3, 3.1, 4.2, 4.3, 4.8, 5.1) with fixes, Apple's 9 questions after a 4.3 spam rejection and how to answer them, the 2.1 new-account packet, how to avoid a 3.2(f) account termination, and a pre-submit checklist.

A free Claude Code skill that fills the App Store Connect **Notes for Review** so the reviewer never has to guess, answers Apple's **9 questions** after a Guideline 4.3 / 4.2.6 rejection, and builds the **Guideline 2.1** packet new developer accounts now get asked for.

It reads your app's code first (screens, purchases, account deletion, every SDK and AI service), then asks you only for what code can't tell it.

Why it exists: [App Store rejection: the 9 questions Apple asks, and the answers that got apps approved](https://annayal.com/blog/app-store-rejection/).

## Pair it with a scanner

This skill writes the words. For technical misses (demo account, privacy manifest, account deletion, staging backend) run a scanner first, e.g. [app-store-preflight-skills](https://github.com/truongduy2611/app-store-preflight-skills) or [app-store-compliance](https://github.com/mjmirza/app-store-compliance). Neither covers the 4.3 nine questions, 3.2(f) or the 2.1 new-account packet, which is what this one is for.

## Real example

[Backed, approved in 1 minute](examples/backed-update.md): the exact Notes for Review text and why it works.

## Install

```bash
mkdir -p ~/.claude/skills/apple-app-review && curl -sL https://raw.githubusercontent.com/Git-Agni/apple-app-review-skill/main/SKILL.md -o ~/.claude/skills/apple-app-review/SKILL.md
```

## Use

In your app's repo, ask Claude Code:
- "write my App Review notes for this update"
- "Apple rejected us under 4.3, here's the message, answer the 9 questions"
- "we got the limited App Review history notice, build the packet"
- "audit this app for App Store rejection risks before I submit"

It drafts. You check every claim before pasting it into App Store Connect.

Sources: Phillip Shoemaker's [Substack](https://phillipshoemaker.substack.com), Rasty Turek's [public reply](https://x.com/synopsi/status/2122380692747411566), Apple's [App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/).

Built at [Agniverse](https://agniverse.co), by [An Nayal](https://annayal.com)
