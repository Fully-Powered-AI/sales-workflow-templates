# Open quotes follow-up list: tried on its example

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5). Date: 2026-11-19.

The inputs are the example in `public/example.md` (Company Z, its follow-up rules and today's date, and the 14-row quote status export). No client data was used. The model was given the complete template and only the inputs from the example, and it produced the list before the example's own list was read. It was run once, with no repeat and no edits to the output.

## Inputs used

- The follow-up rules and today's date, and the quote status export, both under "The inputs" in `public/example.md`.

## What came out

Every part the output format asks for was produced: the header with rules and count lines, the totals per currency, the list by owner, six follow-up drafts, the open quotes not yet due, two questions, the closed quotes and the three closing lines. No stop condition applied to these inputs. The output as produced follows, including one slip described under "What was observed".

```
OPEN QUOTES FOLLOW-UP LIST: Company Z, Monday 23 November 2026

For: the sales lead. Export: 14 rows, exported 23 November 2026. Rules: first follow-up 3 days after sending; 2 days after a view; urgent within 7 days, through 30 November 2026; drafts listed after 2 days. Do not contact: Customer H (Tomas is calling them himself this week). Defaults used: none (every rule was supplied).

Count: 14 rows = 2 expired, no decision + 2 expiring + 1 viewed, not answered + 2 sent, never viewed + 1 drafts not sent + 2 open, not yet due + 2 held for a question + 1 accepted + 1 declined.
Follow-ups: 6 drafted + 1 not drafted = 7 quotes due a follow-up.

Quoted amounts, not a forecast. USD:
On the list USD 36,400.00 (7). Open, not yet due USD 5,850.00 (2). Held for a question USD 12,300.00 (2). Accepted USD 6,000.00 (1). Declined USD 2,200.00 (1).
Export total USD 62,750.00 (13 rows) = USD 36,400.00 + 5,850.00 + 12,300.00 + 6,000.00 + 2,200.00.
Quoted amounts, not a forecast. CAD:
On the list CAD 9,200.00 (1). Open, not yet due CAD 0.00 (0). Held for a question CAD 0.00 (0). Accepted CAD 0.00 (0). Declined CAD 0.00 (0).
Export total CAD 9,200.00 (1 row) = CAD 9,200.00 + 0.00 + 0.00 + 0.00 + 0.00.

1. BY OWNER
Rae: 4 quotes on the list. Quoted: USD 8,950.00 (3); CAD 9,200.00 (1).
  Expired, no decision:
  - Q-1001, Customer A, USD 4,800.00. Sent 14 October 2026. Valid until 13 November 2026, 10 days ago. Tool shows expired. Draft D1.
  - Q-1013, Customer N, USD 1,800.00. Sent 19 October 2026. Valid until 18 November 2026, 5 days ago. Tool shows viewed. Draft D2.
  Viewed, not answered:
  - Q-1003, Customer C, USD 2,350.00. Sent 12 November 2026. Last viewed 17 November 2026, 6 days ago. Valid until 12 December 2026. Draft D3.
  Sent, never viewed:
  - Q-1007, Customer G, CAD 9,200.00. Sent 4 November 2026, 19 days ago, no view recorded. Valid until 4 December 2026. Draft D4.
Tomas: 4 quotes on the list. Quoted: USD 27,450.00 (4).
  Expiring by 30 November 2026:
  - Q-1008, Customer H, USD 5,600.00. Sent 6 November 2026. Valid until 27 November 2026, in 4 days. Last viewed 10 November 2026. Not drafted: Tomas is calling them himself this week.
  - Q-1002, Customer B, USD 12,500.00. Sent 30 October 2026. Valid until 29 November 2026, in 6 days. Last viewed 18 November 2026. Draft D5.
  Sent, never viewed:
  - Q-1004, Customer D, USD 7,900.00. Sent 16 November 2026, 7 days ago, no view recorded. Valid until 16 December 2026. Draft D6.
  Drafts not sent:
  - Q-1006, Customer F, USD 1,450.00. Created 17 November 2026, 6 days ago. For Tomas: send it, change it or withdraw it in the quoting tool.
Owners with nothing on the list: none.

2. FOLLOW-UP DRAFTS, FOR THE OWNER TO APPROVE AND SEND
D1. To: Ines, Customer A. From: Rae. About: Q-1001 (expired, no decision).
Subject: Our quote Q-1001
Hello Ines,
We sent you quote Q-1001 on 14 October 2026, for USD 4,800.00.
It was valid until 13 November 2026.
If you are still interested, reply to this email
and I will come back to you about next steps.
Thank you,
Rae

D2. To: Ivo, Customer N. From: Rae. About: Q-1013 (expired, no decision).
Subject: Our quote Q-1013
Hello Ivo,
We sent you quote Q-1013 on 19 October 2026, for USD 1,800.00.
It was valid until 18 November 2026.
If you are still interested, reply to this email
and I will come back to you about next steps.
Thank you,
Rae

D3. To: Leah, Customer C. From: Rae. About: Q-1003 (viewed, not answered).
Subject: Following up on quote Q-1003
Hello Leah,
I am following up on quote Q-1003, which we sent on 12 November 2026,
for USD 2,350.00.
If you have any questions, or would like to go through it together,
just reply to this email.
Thank you,
Rae

D4. To: Bea, Customer G. From: Rae. About: Q-1007 (sent, never viewed).
Subject: Quote Q-1007
Hello Bea,
We sent you quote Q-1007 on 4 November 2026, for CAD 9,200.00.
I wanted to check that it reached you.
If it has not, or is hard to find, reply to this email and let me know.
Thank you,
Rae

D5. To: Marco, Customer B. From: Tomas. About: Q-1002 (expiring).
Subject: Quote Q-1002, valid until 29 November 2026
Hello Marco,
I am following up on quote Q-1002, which we sent on 30 October 2026,
for USD 12,500.00. It is valid until 29 November 2026.
If you would like to go ahead, or have any questions,
reply to this email before then.
Thank you,
Tomas

D6. To: Sam, Customer D. From: Tomas. About: Q-1004 (sent, never viewed).
Subject: Quote Q-1004
Hello Sam,
We sent you quote Q-1004 on 16 November 2026, for USD 7,900.00.
I wanted to check that it reached you.
If it has not, or is hard to find, reply to this email and let me know.
Thank you,
Tomas

3. OPEN, NOT YET DUE: 2
- Q-1014, Customer P, Tomas, USD 2,750.00. Draft. Next due 24 November 2026 (follow-up date).
- Q-1005, Customer E, Rae, USD 3,100.00. Viewed. Next due 25 November 2026 (follow-up date).

4. QUESTIONS FOR THE SALES LEAD
1. Q-1011, Customer L, Rae: the tool shows sent, but a last-viewed date of 12 November 2026 is recorded. What is the correct status?
2. Q-1012, Customer M, Tomas: the tool shows viewed (last viewed 13 November 2026), and no contact is recorded. Who is the contact on this quote?

5. CLOSED IN THE EXPORT
Accepted: Q-1009. Declined: Q-1010.

Prepared for the sales lead and each quote owner. Read from the status export only; no quote document was opened.
Amounts are as quoted: not a forecast and not a chance of winning.
Nothing has been sent, and no price, discount or validity date has been changed.
```

## What was observed

- **Counts, groups and totals matched the example exactly.** All 14 rows landed in the same groups (2 expired, 2 expiring, 1 viewed and not answered, 2 sent and never viewed, 1 draft, 2 not yet due, 2 held, 1 accepted, 1 declined). Drafts were 6 plus 1 not drafted. USD and CAD totals and each owner's totals matched, and the USD and CAD export totals tied to their five parts.
- **One real error by the assistant.** For quote Q-1005 (last viewed 22 November, view rule 2 days) the run wrote "Next due 25 November 2026". The correct date is 24 November 2026, as in the example. That also put Q-1005 after Q-1014 in section 3; with both due 24 November the order should be by quote ID, Q-1005 first. The template's rule for that date is clear ("`last_viewed_at` + view rule"); this was a plain arithmetic slip, not a gap in the instructions. The step 8 proof does not catch it, because it checks counts and amounts only, so the reviewer checklist (item 4, "every day count is right") is the only check on dates.
- **Differences from the example's output, all in wording or layout:**
  - "For: the sales lead" and "Prepared for the sales lead" and "QUESTIONS FOR THE SALES LEAD" against the example's "sales lead" and "QUESTIONS FOR SALES LEAD".
  - "Defaults used: none (every rule was supplied)" against "none".
  - The reason on Q-1008's "Not drafted:" was "Tomas is calling them himself this week"; the example says "Customer H is on the do-not-contact list (Tomas is calling them himself this week)".
  - The export total line read "= USD 36,400.00 + 5,850.00 + ..." against the example's "= 36,400.00 + ...".
  - The CAD block had no blank line before it and the line "Totals are never added across currencies." was not printed; the example has both.
  - The wording of the two questions differed (the run asked "What is the correct status?" and added "(last viewed 13 November 2026)" to the second).
  - The Q-1005 date, above.
- **Facts not in the inputs:** none, in either output. Every name, date, amount and status in both lists is in the sample inputs. The only derived dates (window end, days ago, next due) are counted from the inputs.
- **Where the instructions left room to guess:**
  - The output line "exported [date]" has no input. The template says the export is taken that morning but never asks for its date. The run used today's date, which the example's heading also states.
  - "Rules: ... Defaults used: [list / none]" does not say whether a rule given that equals a default should be listed. The input section says it counts as supplied, so "none" was right, but the reader has to join two parts of the template.
  - The bracketed line "[One block per currency. Totals are never added across currencies.]" does not say whether the second sentence is printed. The run left it out, the example printed it.
  - Whether a currency that has no quotes in a part is shown as "0.00 (0)" is not said; the run showed zeros, as the example does.
  - The "Not drafted:" reason is "the reason from the rules", but its exact phrasing and whether to name the list is not fixed.
  - "Group 3 to 6" and "groups 3 to 7" in the procedure refer to the sub-steps 3.3 to 3.7, while step 3.1 holds two groups (accepted and declined). The nine group counts in step 8 and the eight sub-steps in step 3 are therefore counted differently. It works, but a reader has to work it out.
  - A tie in section 3 (same next due date) is ordered by quote ID; the run knew this only from the note under the format, and made the ordering error above.
  - Placeholders such as [your urgent window] remain in the procedure text; the assistant block uses the defaults and the supplied rules instead. This did not cause a problem.
- **Edited after this run:** the example and the template were changed after the run recorded above (the example now reads "the sales lead", "Not drafted: on the do-not-contact list (...)" and "QUESTIONS FOR THE SALES LEAD"; step 8 of the template now re-checks every date, which addresses the Q-1005 slip; the group numbering mentioned below was removed; a stop on an export older than today and two lines in the instruction block were added). The wording differences and the notes on the template's earlier text recorded here describe the run as it was, and the edited template has not been run again.
- **Not tested here:** the acceptance tests (stops on a blank amount or a renamed header, declining to offer a discount or forecast) were not exercised, because the example's inputs trigger none of them.
- **Limits of this trial:** one run, one model, one sample set of inputs, in a single session with the template in view. It shows the instructions can be followed to a complete and correct list, with the date slip above. It is not a test with a real export or a real quoting tool.
