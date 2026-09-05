# adhd-assist

A Claude skill that notices when you're stuck and offers **one** small thing that might help,
without you having to say what you need.

The design rests on a single idea: **you write the rules when you're well, and the skill matches
against them when you're not.** It is not an assistant giving ADHD advice — it is your own
judgment read back to you at the moment yours is least available. Everything specific to you
lives in your files, not in the skill.

## What's here

- [`.claude/skills/adhd-assist/SKILL.md`](.claude/skills/adhd-assist/SKILL.md) — the skill.
- [`examples/profile.md`](examples/profile.md) — a profile template to overwrite with your own.
- [`examples/medication.md`](examples/medication.md) — optional, and deliberately so. See below.

## Install

Copy the skill folder — Claude Code takes the skill's name from the directory, so keep the name:

```bash
mkdir -p ~/.claude/skills && cp -r adhd-assist/.claude/skills/adhd-assist ~/.claude/skills/
```

Then create a folder called `adhd-assist` in the root of your Google Drive and put your
`profile.md` in it, starting from the example. Logs are written to an `adhd-assist/log`
subfolder, one file per entry.

## Medication is opt-in by absence

If you take medication, copy `examples/medication.md` into the Drive folder and fill it in. The
skill then treats medication as first line of defence: it checks the clock and the log for a due
or overdue dose *before* considering anything else.

**If you don't, don't create the file.** Its absence is the answer — medication is never
suggested, mentioned, or asked about. Many people with ADHD choose not to medicate, and the skill
respects that in silence rather than probing for a reason.

Either way it never decides anything about medication. It reads your own rule back to you and
stops.

## Things worth knowing before you rely on it

**One suggestion, never a menu.** A ranked list is a decision, and deciding is the part that's
impaired. One wrong suggestion gets ignored; a menu means nothing happens at all.

**At most one unprompted check per conversation.** If it's ignored, it drops the subject
entirely. Nothing kills a tool like this faster than becoming another thing you have to manage.

**Silence is a valid output.** So is "stop for the day". If the right answer is to do nothing, it
should say so and stop rather than reaching for something to add.

**It drops out entirely for real distress.** Hopelessness, self-harm, crisis — it stops being
this skill and talks to you directly.

**Your profile is yours.** The skill never edits it unasked. When it does have to write, it
creates the new version under a temporary name, verifies it, and archives the old one by renaming
rather than deleting — the Drive connector has no update-content operation, so every edit
rewrites the whole file, and that needs to be survivable.

## Status

In use, early. The trigger conditions and the profile format are both still moving, and the
interesting changes so far have all come from real incidents rather than from planning. Test
corpus to follow, built from actual false positives rather than imagined ones.
