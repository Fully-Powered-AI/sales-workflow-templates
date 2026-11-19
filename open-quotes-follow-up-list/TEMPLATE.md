# Open quotes follow-up list

Workflow template, version 0.1.0.

## Purpose

Read the week's quote status export from a quoting or proposal tool and return one follow-up list for the person who runs it: every open quote placed in one group (expired with no decision, expiring inside the urgent window, viewed and not answered, sent and never viewed, draft not sent, or not yet due), shown by owner, with a count and quoted totals by currency that tie to the export, and a short follow-up draft for each quote that is due one, for its owner to approve and send. The assistant works from the status export only. It changes no price, offers no discount, extends no validity date, gives no chance of winning and no forecast, and sends nothing.

## When to use it and when not to

Use it once a week, from an export taken that morning, at any business that sends priced quotes or proposals and records their status in one tool. It also serves before a sales meeting, to see what is waiting.

Do not use it:

- to decide whether to lower a price, offer a discount or extend a quote. The owner or the person who approves prices decides, in the quoting tool;
- to forecast sales or judge which quotes will be won. Every amount is a quoted amount;
- to read, check or rewrite the quote documents. It reads the status export only;
- to send follow-ups, log calls or update statuses. The owners do that;
- when the export is older than today: the days counted would be wrong.

## Roles

- **Runs it and supplies the export, the rules and today's date:** the owner of the business, the sales lead or the estimator.
- **Reads their part, approves, edits or drops each follow-up and sends it:** the quote owner named on each row.
- **Answers the questions about the export:** the person who runs it, checking in the quoting tool.
- **Decides any price, discount, validity date or reissue:** the quote owner or whoever the business names to approve prices. Never the assistant.

## Inputs

1. **The quote status export from your quoting or proposal tool,** one row per quote, with these default column headers: `quote_id`, `customer`, `contact`, `owner`, `amount`, `currency`, `created_at`, `sent_at`, `status`, `last_viewed_at`, `valid_until`. `status` is one of `draft`, `sent`, `viewed`, `accepted`, `declined`, `expired`. Dates are written YYYY-MM-DD. `amount` is the quoted amount as a plain number. If the export is missing, stop and ask.
2. **The follow-up rules.** Defaults: a quote sent with no view recorded is due a first follow-up 3 days after `sent_at`; a viewed quote with no answer is due 2 days after `last_viewed_at`; a quote is urgent when its `valid_until` is within 7 days of today; a draft is listed once it is 2 days past `created_at`; follow-ups go only to the contact on the quote, signed by its owner. The rules may also list customers or quote IDs not to contact this week, each with a reason. Say which defaults were used; a rule given that happens to equal a default counts as supplied.
3. **Today's date,** which is also used as the export's date unless the export's own date is given. If today's date is not given, stop and ask; never take it from the export's file name.
4. **Who the list is for and the business's name.** If not given, write "the person who runs it" and leave the name out.

**Column headers.** If a header is missing, renamed or extra, stop and ask which column holds what. Never guess a column. If the tool uses other status words, stop and ask how they map to the six.

The assistant works from the export and notes supplied. It needs no connection to the quoting tool and never asks for a password or a login code. If a quote document is supplied, it says it does not read quote documents and works from the export alone.

## The procedure

1. **Check the inputs.** Confirm every header. Count the rows. If two rows share a `quote_id`, stop and ask. If a date could be read two ways, stop and ask. If any row's `amount` is blank, not a number or below zero, or its `currency` is blank, stop and ask: the totals cannot tie without it.
2. **Set the window.** Window end = today + [your urgent window] calendar days. Count calendar days only. Days since a date = today minus that date.
3. **Place every row in exactly one group,** testing in this order:
   1. **Accepted** or **Declined:** the status says so. These rows are checked for nothing else.
   2. **Held for a question,** when any of these is true: `owner` is blank; on a draft, `created_at` is blank or after today, or `sent_at` is filled; on any other row, `sent_at` is blank or after today; `contact` is blank on a sent, viewed or expired quote; `status` is viewed and `last_viewed_at` is blank; `status` is sent and `last_viewed_at` is filled; `last_viewed_at` is before `sent_at` or after today; `valid_until` is before `sent_at`; `status` is expired and `valid_until` is blank, today or later.
   3. **Expired, no decision:** `status` is expired, or `status` is sent or viewed and `valid_until` is before today.
   4. **Expiring:** `status` is sent or viewed and `valid_until` is from today to the window end.
   5. **Viewed, not answered:** `status` is viewed and days since `last_viewed_at` is at least [your view rule].
   6. **Sent, never viewed:** `status` is sent and days since `sent_at` is at least [your send rule].
   7. **Draft not sent:** `status` is draft and days since `created_at` is at least [your draft rule]. A draft whose `valid_until` has already passed stays here; the owner decides in the tool whether to send, change or withdraw it.
   8. **Open, not yet due:** everything left.
   A blank `valid_until` on a sent or viewed quote skips steps 3.3 and 3.4 for that quote, and its line says "no valid-until date recorded".
4. **Next due date** for each quote open and not yet due: the earlier of its follow-up date (`sent_at` + send rule for sent, `last_viewed_at` + view rule for viewed, `created_at` + draft rule for a draft) and the day it enters the urgent window (`valid_until` minus the window), when it has a `valid_until`.
5. **Check who may be contacted.** A quote in the expired, expiring, viewed-not-answered and sent-never-viewed groups whose customer or quote ID is on the rules' do-not-contact list stays in its group, gets no draft and carries "Not drafted: on the do-not-contact list ([reason from the rules])".
6. **Write one follow-up draft** for every other quote in the expired, expiring, viewed-not-answered and sent-never-viewed groups, in the wording fixed in the output format for its group, filled only from that row: the contact's name as written, the quote ID, the sent date, the amount and currency as exported, the valid-until date where the wording uses it, and the owner's name. A draft never mentions that the customer opened the quote, never names a price other than the quoted amount, never offers a discount, a new date or an extension, never says how likely anything is, and never adds a fact the row does not hold. Drafts for the draft-not-sent group are not written: the line asks the owner to send, change or withdraw the draft in the tool.
7. **Add the totals,** per currency and never across currencies: the quoted amount on the list (those four groups and the draft-not-sent group), open and not yet due, held for a question, accepted and declined, each with its count, and the export total for that currency, which must equal the five parts and the sum of that currency's rows. Per owner, total the quotes on the list by currency.
8. **Prove the count.** Rows read = rows in the export = the nine group counts added. Drafts written + not drafted = quotes in the expired, expiring, viewed-not-answered and sent-never-viewed groups. Then re-check every date printed or counted (days ago, days to expiry, next due) against its row and the rules, one by one; a date is not proved by the counts. If any count, total or date does not tie, stop and report the figures; print nothing else.
9. **Return the list** in the output format to the person who ran it. Do not send it or any draft onward.

## Exceptions and stop conditions

- **A header is missing, renamed or extra; a status word is not one of the six; a date is ambiguous; two rows share an ID; today's date is missing; the export's date is earlier than today's date; an amount or currency is blank or unreadable:** stop and ask.
- **A count or total in step 8 does not tie:** stop and show the figures and the difference; never leave a row out to make it tie.
- **Asked to change a price, offer or suggest a discount, extend or renew a validity date, or reissue a quote:** decline; the quote owner or the person who approves prices decides and does it in the quoting tool. A draft may say the quote was valid until a date; it never offers a new one.
- **Asked for the chance of winning a quote, a forecast or an expected value:** decline; the list shows quoted amounts only.
- **Asked to send a follow-up, mark a quote as followed up, change a status or contact anyone:** decline; the owner sends and updates the tool.
- **Asked to contact someone other than the contact on the quote, or a customer on the do-not-contact list:** decline and show the rule.
- **Given a quote document, or asked to read or rewrite one:** decline; this workflow template reads the status export only.
- **The export holds a password, a login code, a link carrying an access token, or payment card or bank details:** do not repeat them; ask for the export again without them.

## Output format

```
OPEN QUOTES FOLLOW-UP LIST: [business], [weekday date]

For: [who runs it]. Export: [n] rows, exported [date]. Rules: first follow-up [n] days after sending; [n] days after a view; urgent within [n] days, through [window end]; drafts listed after [n] days. Do not contact: [customers or quote IDs, with reasons / none]. Defaults used: [list / none].

Count: [n] rows = [n] expired, no decision + [n] expiring + [n] viewed, not answered + [n] sent, never viewed + [n] drafts not sent + [n] open, not yet due + [n] held for a question + [n] accepted + [n] declined.
Follow-ups: [n] drafted + [n] not drafted = [n] quotes due a follow-up.

Quoted amounts, not a forecast. [Currency]:
On the list [amount] ([n]). Open, not yet due [amount] ([n]). Held for a question [amount] ([n]). Accepted [amount] ([n]). Declined [amount] ([n]).
Export total [amount] ([n] rows) = [the five amounts added].
[One block per currency, a blank line between blocks. After the last block, a blank line and the line: Totals are never added across currencies.]

1. BY OWNER
[Owner]: [n] quotes on the list. Quoted: [currency amount] ([n])[; currency amount ([n])].
  Expired, no decision:
  - [quote_id], [customer], [currency amount]. Sent [date]. Valid until [date], [n] days ago. Tool shows [status]. [Draft D[n] / Not drafted: on the do-not-contact list ([reason from the rules])].
  Expiring by [window end]:
  - [quote_id], [customer], [currency amount]. Sent [date]. Valid until [date], in [n] days. [Last viewed [date] / No view recorded]. [Draft D[n] / Not drafted: on the do-not-contact list ([reason from the rules])].
  Viewed, not answered:
  - [quote_id], [customer], [currency amount]. Sent [date]. Last viewed [date], [n] days ago. Valid until [date / no valid-until date recorded]. [Draft D[n] / Not drafted: on the do-not-contact list ([reason from the rules])].
  Sent, never viewed:
  - [quote_id], [customer], [currency amount]. Sent [date], [n] days ago, no view recorded. Valid until [date / no valid-until date recorded]. [Draft D[n] / Not drafted: on the do-not-contact list ([reason from the rules])].
  Drafts not sent:
  - [quote_id], [customer], [currency amount]. Created [date], [n] days ago. For [owner]: send it, change it or withdraw it in the quoting tool.
Owners with nothing on the list: [names / none].

2. FOLLOW-UP DRAFTS, FOR THE OWNER TO APPROVE AND SEND
D[n]. To: [contact], [customer]. From: [owner]. About: [quote_id] ([group]).
Subject: [by group, below]
Hello [contact],
[Body, by group, below]
Thank you,
[owner]

  Expired, no decision. Subject: Our quote [quote_id]
  We sent you quote [quote_id] on [sent date], for [currency amount].
  It was valid until [valid-until date].
  If you are still interested, reply to this email
  and I will come back to you about next steps.

  Expiring. Subject: Quote [quote_id], valid until [valid-until date]
  I am following up on quote [quote_id], which we sent on [sent date],
  for [currency amount]. It is valid until [valid-until date].
  If you would like to go ahead, or have any questions,
  reply to this email before then.

  Viewed, not answered. Subject: Following up on quote [quote_id]
  I am following up on quote [quote_id], which we sent on [sent date],
  for [currency amount].
  If you have any questions, or would like to go through it together,
  just reply to this email.

  Sent, never viewed. Subject: Quote [quote_id]
  We sent you quote [quote_id] on [sent date], for [currency amount].
  I wanted to check that it reached you.
  If it has not, or is hard to find, reply to this email and let me know.

/ No follow-up is due this week.

3. OPEN, NOT YET DUE: [n]
- [quote_id], [customer], [owner], [currency amount]. [Status]. Next due [date] ([follow-up date / enters the urgent window]).
/ None.

4. QUESTIONS FOR [WHO RUNS IT]
[n]. [quote_id], [customer], [owner / owner not recorded]: [the facts as exported]. [Question.]
/ None.

5. CLOSED IN THE EXPORT
Accepted: [quote_ids] / none. Declined: [quote_ids] / none.

Prepared for [who runs it] and each quote owner. Read from the status export only; no quote document was opened.
Amounts are as quoted: not a forecast and not a chance of winning.
Nothing has been sent, and no price, discount or validity date has been changed.
```

Order: owners alphabetically; inside an owner, the groups in the order shown, and within a group oldest first by the date that put the quote there (valid-until for expired and expiring, last viewed, sent, created). An owner's block lists only the groups that hold one of their quotes. Drafts are numbered D1 onward in the order their quotes appear in section 1. Section 3 is ordered by next due date, then quote ID; section 4 by quote ID. Write dates in words, such as "23 November 2026", and amounts with the currency code first and two decimals, such as "USD 4,800.00". One day reads "1 day". When a numbered section is empty, print the line after the "/" or "None."; never leave a section out.

## Reviewer checklist

1. The headers matched the defaults, or the mapping was confirmed. (Person who runs it)
2. The nine group counts add up to the rows in the export. (Person who runs it)
3. For each currency, the five amounts add up to the export total, and no total mixes currencies. (Person who runs it)
4. Every quote is in the right group, tested in the order given, and every day count is right. (Person who runs it)
5. Every draft holds only facts from its row, and none mentions a view, a discount, a new price, a new date or how likely anything is. (Quote owner)
6. No draft goes to a customer on the do-not-contact list or to anyone but the contact on the quote. (Quote owner)
7. Every question names the row and the facts, and none suggests a fix. (Person who runs it)

## Acceptance tests

Proposed tests. None has been run.

1. **Sent, never viewed.** Sent 2026-11-16, no view, today 2026-11-23, send rule 3. Expected: sent, never viewed, "7 days ago", with a draft.
2. **Viewed, not yet due.** Last viewed 2026-11-22, view rule 2. Expected: open, not yet due, next due 24 November 2026.
3. **Viewed and expiring.** Viewed, valid until 2026-11-29, window 7 days. Expected: expiring, not viewed with no answer, with the expiring wording.
4. **Past validity, still viewed.** Status viewed, valid until 2026-11-18. Expected: expired, no decision, "Tool shows viewed".
5. **Status sent with a view recorded.** Expected: held for a question; no draft.
6. **Blank contact.** On a viewed quote. Expected: held for a question; no draft.
7. **Do not contact.** Customer on the rules' list, quote expiring. Expected: listed as expiring, "Not drafted: on the do-not-contact list" with the reason in brackets.
8. **Two currencies.** One CAD row among USD rows. Expected: a block per currency; nothing added across them.
9. **Blank amount.** Expected: stops and asks.
10. **Header mismatch.** `expires_on` in place of `valid_until`. Expected: stops and asks.
11. **Asked to offer 5% off in the draft.** Expected: declines; the owner decides prices in the quoting tool.
12. **Asked which quotes will close this month.** Expected: declines; amounts are quoted, not a forecast.

## Instructions for the AI assistant

```
You prepare the week's follow-up list of open quotes from a quoting or
proposal tool's status export, for the person who runs it and each quote
owner. You read the status export only, never a quote document. You never
send anything, contact anyone, change a status, change a price, offer or
suggest a discount, or extend or renew a validity date: the quote owner
decides and does those in the tool. You give no chance of winning and no
forecast. You never ask for a password or a login code.

The user will supply: the quote status export; the follow-up rules; today's
date, also the export's date unless given; who the list is for and the
business's name (if no name is given, leave it out). Default headers:
quote_id, customer, contact, owner, amount, currency, created_at, sent_at,
status, last_viewed_at, valid_until. Status is draft, sent, viewed,
accepted, declined or expired. Default rules: send rule 3 days; view rule 2 days; urgent window 7 days;
draft rule 2 days; follow-ups only to the contact on the quote, signed by
its owner; a do-not-contact list may name customers or quote IDs. Stop and
ask if a header is missing, renamed or extra, a status word is unknown, a
date is ambiguous, two rows share an ID, today's date is missing, the
export's date is earlier than today's date, or any amount or currency is
blank, unreadable or below zero. Never repeat a password, a login code, a
link carrying an access token, or card or bank details found in the export;
ask for the export again without them.

1. Window end = today + urgent window, in calendar days.
2. Put every row in one group, testing in order: accepted; declined; held
   for a question (owner blank; draft with created_at blank or after today
   or sent_at filled; other rows with sent_at blank or after today; contact
   blank on sent, viewed or expired; viewed with no last_viewed_at; sent
   with last_viewed_at filled; last_viewed_at before sent_at or after
   today; valid_until before sent_at; expired with valid_until blank or not
   yet passed); expired, no decision (expired, or sent or viewed with
   valid_until before today); expiring (sent or viewed, valid_until from
   today to window end); viewed, not answered (days since last view at
   least the view rule); sent, never viewed (days since sent at least the
   send rule); draft not sent (days since created at least the draft
   rule; a draft past its valid_until stays a draft not sent); open, not yet
   due.
3. Next due for open, not yet due: the earlier of the follow-up date and
   valid_until minus the window.
4. One draft per quote expired, expiring, viewed or sent-never-viewed,
   unless its customer or ID is on the do-not-contact list ("Not drafted: on
   the do-not-contact list ([reason])"). Use the fixed wording for its
   group, filled only from its row. Never mention that the quote was opened, never offer a
   discount, another price, a new date or an extension, never add a fact.
5. Totals per currency, never across currencies: on the list, open not yet
   due, held, accepted, declined, and the export total, which must equal
   the five parts. Label them as quoted amounts, not a forecast.
6. Prove the count: rows = the nine groups added; drafted + not drafted =
   quotes due a follow-up. Then re-check every printed or counted date
   (days ago, days to expiry, next due) against its row and the rules. If
   anything fails, stop and show the figures.
7. Use the output format exactly and follow the notes under it on order,
   dates, amounts and empty sections. End with the three closing lines.

If asked to send, change a price, discount, extend, forecast, read a quote
document or contact anyone else, decline and say who decides.
```

## What to customize

- Your export's headers, or the mapping from them to the defaults, and your tool's status words mapped to the six.
- [your send rule], [your view rule], [your urgent window] and [your draft rule], in calendar days.
- The do-not-contact list, refreshed each week, and who signs each follow-up.
- The wording of the four follow-up drafts, kept to facts the export holds.
- Who reads the list and when the owners send their follow-ups.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 19 November 2026. Written by FullyPowered AI as original work. Tried on its example on 19 November 2026 in one run, published with it; edits after that run, to the date check, the export date, the totals line and the "Not drafted:" wording, and then to the stop on an export older than today, the draft-past-validity note and the instruction block's business-name and credentials lines, have not been run again. Not yet tested in a client environment.
