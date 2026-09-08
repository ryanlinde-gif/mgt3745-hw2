# FEATURES.md — Recruiting Reality Check

**Ryan Linde — MGT 3745 — HW2**

## 4. Kano-Classified Feature List

Classified **2026-09-08**. Classifications expire; the Attractive item becomes Must-be once competitors ship it.

| # | Feature | Kano | Reason from research |
|---|---|---|---|
| 1 | Verified coach addresses for her level | Must-be | Finding addresses is what capped my sister at six emails |
| 2 | Honest level assessment | Must-be | Mom asked for exactly this; sister cannot tell if she is aiming too high or low |
| 3 | Contact log with follow-up status | Performance | The thing sister named to hand off first; she forgets who to re-email |
| 4 | Coach emails drafted for the athlete | Performance | Personalizing is why she planned more and sent six |
| 5 | Reply activity visible to the parent | Performance | Mom's definition of going well is coaches responding |
| 6 | Signal of program interest before paying for its camp | Attractive | Mom declined a camp for exactly this reason |
| 7 | Follower, view, and like counts | Indifferent | "Just getting views or likes doesn't really mean that much to me" |
| 8 | Emails sent without the athlete seeing who was contacted | **Reverse** | Sister hands off writing but insists on knowing who is contacted |

## 5. The Specification

### Context

A club soccer family cannot get evidence of interest before spending. The mother already pays for
camps, showcases, travel, and film, and declined the last camp because she could not tell whether
the program was interested. The athlete sends small personalized batches, loses track of
follow-ups, and cannot judge her own level. The Reality Check supplies that evidence free, before
money is discussed.

### Users

Profile A (The Parent) and Profile B (The Athlete) in `USERS.md`. The athlete does the outreach;
the parent decides what gets paid for. Both must be present by the end.

### Scope

**Does:** one intake form; a written Reality Check with a level assessment and stated confidence, a
fit-ranked list of at least 15 verified coach addresses, and a named next step; delivered in 48
hours; followed by a 15-minute call with a parent present.

**Does not:** guarantee placement, offers, or replies. Does not email any coach during the Reality
Check. Does not send a coach email the athlete cannot see. Does not report views, likes, or
follower counts. Does not edit film. Does not present a price before the call.

### Behavior

1. Intake submitted: grad year, position, club, GPA, film link, parent email, target regions.
2. Receipt confirmed, delivery deadline named.
3. Level assessed against the club's competitive tier and the film; confidence recorded.
4. Coach list built, each address verified against the current staff directory.
5. Reality Check emailed to athlete and parent with a booking link, then up to two follow-ups.
6. The call reviews the document and ends with an explicit next step.

### Constraints

Email only; no app or login. Under-18 athletes require a parent email before delivery. The athlete
must be able to see every coach contacted on her behalf. No athlete data is published or shared
between families. Addresses re-verified within 90 days of use. The 48 hours runs from a
**complete** intake.

### Acceptance (EARS)

- WHEN a complete intake is submitted, THE SYSTEM SHALL confirm by email within 15 minutes, stating the 48-hour deadline.
- WHEN 48 hours have elapsed since a complete intake, THE SYSTEM SHALL have delivered the Reality Check or sent a delay notice naming a new date.
- THE SYSTEM SHALL include at least 15 coach addresses, each verified against the program's staff page within 90 days.
- THE SYSTEM SHALL state one level assessment and one confidence value from {high, medium, low}.
- WHERE a coach has been contacted for an athlete, THE SYSTEM SHALL show her the coach, the date, and the follow-up status.
- IF the athlete is under 18 and no parent email is on file, THEN THE SYSTEM SHALL withhold delivery and request one.
- IF a listed address bounces, THEN THE SYSTEM SHALL replace it within 5 business days.
- WHILE a delivered Reality Check has no booked call, THE SYSTEM SHALL send at most two follow-ups, on day 3 and day 7.
- IF no parent is present at the scheduled call, THEN THE SYSTEM SHALL reschedule rather than present pricing.

## 6. Handoff Test

Four questions block a stranger. **What makes an assessment "high confidence"?** I never defined
the evidence threshold, so two people would grade the same athlete differently. Largest gap here.
**What does this cost, and would a parent pay?** My mother said she does not mind spending when
there is a reason, but I never asked what she would pay, so Kano row 6 is a hypothesis about
willingness, not a measurement. **Who re-verifies the coach data?** The databases exist; the
refresh process is only in my head. And **both interviews were one household** — a mother and
daughter agree with each other more than two unrelated families would.

## AI Use Note

I used Claude to build the interview scripts, structure both files, convert my acceptance criteria
into EARS notation, and tighten wording. I conducted both interviews myself with my mother and
sister, recorded with their permission; all quotes are theirs. An earlier Claude draft contained
invented interview content, which I replaced entirely with the real transcripts.
