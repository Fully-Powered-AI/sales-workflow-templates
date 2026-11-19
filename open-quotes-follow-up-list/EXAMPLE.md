# Open quotes follow-up list: an example

*Illustrative example with sample data.* Company Z is an illustrative business that makes and installs commercial signs. Its sales lead runs the list every Monday. The two quote owners, Rae and Tomas, and every customer contact are illustrative first names; the customers appear as letters. Every row, date and amount below is illustrative.

The inputs come first, in full, so the workflow template can be run on them. The list follows.

## The inputs

### 1. Follow-up rules and today's date (typed by the sales lead)

```
Business: Company Z
Today: Monday 23 November 2026
List is for: sales lead
First follow-up, sent with no view: 3 days after sending
Follow-up after a view with no answer: 2 days after the last view
Urgent: valid-until date within 7 days of today
Drafts listed after: 2 days
Who may be contacted: only the contact on the quote, signed by the quote's owner
Do not contact this week: Customer H (Tomas is calling them himself this week)
```

### 2. The quote status export from your quoting or proposal tool (exported Monday 23 November 2026)

The export has one row per quote and these columns: quote ID, customer, contact, owner, amount, currency, created date, sent date, status, last viewed date and valid-until date.

```
quote_id,customer,contact,owner,amount,currency,created_at,sent_at,status,last_viewed_at,valid_until
Q-1001,Customer A,Ines,Rae,4800.00,USD,2026-10-12,2026-10-14,expired,2026-10-20,2026-11-13
Q-1002,Customer B,Marco,Tomas,12500.00,USD,2026-10-28,2026-10-30,viewed,2026-11-18,2026-11-29
Q-1003,Customer C,Leah,Rae,2350.00,USD,2026-11-10,2026-11-12,viewed,2026-11-17,2026-12-12
Q-1004,Customer D,Sam,Tomas,7900.00,USD,2026-11-13,2026-11-16,sent,,2026-12-16
Q-1005,Customer E,Noor,Rae,3100.00,USD,2026-11-19,2026-11-20,viewed,2026-11-22,2026-12-20
Q-1006,Customer F,Owen,Tomas,1450.00,USD,2026-11-17,,draft,,
Q-1007,Customer G,Bea,Rae,9200.00,CAD,2026-11-02,2026-11-04,sent,,2026-12-04
Q-1008,Customer H,Ken,Tomas,5600.00,USD,2026-11-05,2026-11-06,viewed,2026-11-10,2026-11-27
Q-1009,Customer J,Ada,Rae,6000.00,USD,2026-10-20,2026-10-22,accepted,2026-10-25,2026-11-21
Q-1010,Customer K,Paz,Tomas,2200.00,USD,2026-10-26,2026-10-27,declined,2026-10-29,2026-11-26
Q-1011,Customer L,Rui,Rae,3900.00,USD,2026-11-09,2026-11-10,sent,2026-11-12,2026-12-10
Q-1012,Customer M,,Tomas,8400.00,USD,2026-11-11,2026-11-12,viewed,2026-11-13,2026-12-11
Q-1013,Customer N,Ivo,Rae,1800.00,USD,2026-10-17,2026-10-19,viewed,2026-10-21,2026-11-18
Q-1014,Customer P,Lin,Tomas,2750.00,USD,2026-11-22,,draft,,
```

## The list

```
OPEN QUOTES FOLLOW-UP LIST: Company Z, Monday 23 November 2026

For: the sales lead. Export: 14 rows, exported 23 November 2026. Rules: first follow-up 3 days after sending; 2 days after a view; urgent within 7 days, through 30 November 2026; drafts listed after 2 days. Do not contact: Customer H (Tomas is calling them himself this week). Defaults used: none.

Count: 14 rows = 2 expired, no decision + 2 expiring + 1 viewed, not answered + 2 sent, never viewed + 1 drafts not sent + 2 open, not yet due + 2 held for a question + 1 accepted + 1 declined.
Follow-ups: 6 drafted + 1 not drafted = 7 quotes due a follow-up.

Quoted amounts, not a forecast. USD:
On the list USD 36,400.00 (7). Open, not yet due USD 5,850.00 (2). Held for a question USD 12,300.00 (2). Accepted USD 6,000.00 (1). Declined USD 2,200.00 (1).
Export total USD 62,750.00 (13 rows) = 36,400.00 + 5,850.00 + 12,300.00 + 6,000.00 + 2,200.00.

Quoted amounts, not a forecast. CAD:
On the list CAD 9,200.00 (1). Open, not yet due CAD 0.00 (0). Held for a question CAD 0.00 (0). Accepted CAD 0.00 (0). Declined CAD 0.00 (0).
Export total CAD 9,200.00 (1 row) = 9,200.00 + 0.00 + 0.00 + 0.00 + 0.00.

Totals are never added across currencies.

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
  - Q-1008, Customer H, USD 5,600.00. Sent 6 November 2026. Valid until 27 November 2026, in 4 days. Last viewed 10 November 2026. Not drafted: on the do-not-contact list (Tomas is calling them himself this week).
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
- Q-1005, Customer E, Rae, USD 3,100.00. Viewed. Next due 24 November 2026 (follow-up date).
- Q-1014, Customer P, Tomas, USD 2,750.00. Draft. Next due 24 November 2026 (follow-up date).

4. QUESTIONS FOR THE SALES LEAD
1. Q-1011, Customer L, Rae: the status is sent, but a view is recorded on 12 November 2026. Which does the quoting tool show?
2. Q-1012, Customer M, Tomas: no contact is recorded on this viewed quote. Who at Customer M is the contact for it?

5. CLOSED IN THE EXPORT
Accepted: Q-1009. Declined: Q-1010.

Prepared for the sales lead and each quote owner. Read from the status export only; no quote document was opened.
Amounts are as quoted: not a forecast and not a chance of winning.
Nothing has been sent, and no price, discount or validity date has been changed.
```

## Checking the figures (not part of the list)

- Window end: 23 November + 7 days = 30 November 2026.
- Groups: expired Q-1001 (status expired) and Q-1013 (viewed, valid until 18 November, before today); expiring Q-1008 (27 November) and Q-1002 (29 November); viewed, not answered Q-1003 (last view 17 November, 6 days, rule 2); sent, never viewed Q-1004 (16 November, 7 days) and Q-1007 (4 November, 19 days), rule 3; draft not sent Q-1006 (17 November, 6 days, rule 2); not yet due Q-1005 (last view 22 November, 1 day) and Q-1014 (created 22 November, 1 day); held Q-1011 (sent with a view recorded) and Q-1012 (no contact); accepted Q-1009; declined Q-1010. 2 + 2 + 1 + 2 + 1 + 2 + 2 + 1 + 1 = 14.
- Next due: Q-1005, 22 November + 2 = 24 November; it enters the urgent window on 20 December − 7 = 13 December; the earlier is 24 November. Q-1014, 22 November + 2 = 24 November; it has no valid-until date.
- USD on the list: 4,800 + 1,800 + 2,350 (Rae, 8,950) + 12,500 + 5,600 + 7,900 + 1,450 (Tomas, 27,450) = 36,400. Not yet due 3,100 + 2,750 = 5,850. Held 3,900 + 8,400 = 12,300. Accepted 6,000. Declined 2,200. 36,400 + 5,850 + 12,300 + 6,000 + 2,200 = 62,750, the sum of the 13 USD rows. CAD: Q-1007, 9,200, the one CAD row.
- Follow-ups: 7 quotes in the four follow-up groups; Q-1008 not drafted; 6 drafts.
