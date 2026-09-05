# Medication

*This is an example with placeholder timings and no drug names. Replace every line with your own
actual prescription, or delete the file.*

**If you do not take medication for ADHD, delete this file.** Its absence is the answer, not a
gap: the skill will never suggest, mention, or ask about medication. Many people with ADHD choose
not to medicate, and that choice needs no explanation and gets none.

**If you do, this file makes medication first line of defence** — checked before anything else,
because the rest of the menu works poorly on top of an unmedicated day. Necessary, though, not
sufficient: a dose being due doesn't end the check, it comes before it.

**The skill never writes to this file and never suggests a dose.** It reads your own rule back to
you and stops:

> *this looks like the state you called X, and your own rule for X says Y.*

The call is always yours. If you ask it to just decide, it will decline and read you your rule
instead — say so here, so it knows you meant that.

Lives in Google Drive as `adhd-assist/medication.md`.

---

## Schedule

Approximate times are fine. Regularity is what makes it predictive.

- `[Morning]` — long-acting dose
- `[Midday]` — short-acting top-up
- `[Late afternoon]` — short-acting top-up

---

## My own rules

`[When an extra dose is on the table, in your own words, and what your prescriber has agreed to.]`

`[The latest time you're willing to take something, and the one exception that overrides it.]`

`[Anything seasonal or situational that changes the weighting.]`

`[Whether you want a hard day raised with you unprompted, or would rather it stayed quiet.]`

**Write each exception into the same sentence as the rule it modifies.** "Not after 7pm unless X"
read on its own becomes "not after 7pm" plus a loophole, and whichever half gets quoted back at
you is the half that wins. "Not after 7pm — the exception is X, and Y is not X" survives being
read in isolation, which is how it will usually be read.

---

## The clock

Your schedule is regular enough to be predictive on its own, with no sensors at all. This is the
free signal, and the one worth leaning on hardest.

| Local time | Where you are | What it makes more likely |
|---|---|---|
| before the first dose | pre-dose | `[you probably shouldn't be working yet]` |
| first two hours after it | coming up | `[best window of the day, protect it]` |
| the hour before each top-up | trough | `[scattered, flat, irritable, short fuse]` |
| between doses | covered | `[steady]` |
| after the last dose wears off | tail | `[locked, or wired-tired, and it's near bedtime]` |
| past your bedtime | off-plan | `[you said you'd be in bed]` |

The point of this table: **the same behaviour means different things at different hours.** Clipped
and irritable in a mid-afternoon trough is a dip that will pass. The identical messages late in
the evening are the day catching up with you, and the answer is not the same one.
