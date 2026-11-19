# Open quotes follow-up list

A weekly list from your quote status export: quotes never viewed, unanswered, near expiry or expired, by owner, each with a follow-up draft to approve.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** This is a template, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See Open quotes follow-up list on our website](https://fullypowered.ai/workflows/open-quotes-follow-up-list/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list). Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Quick start**

1. Read EXAMPLE.md to see what a good result looks like.
2. Copy all of TEMPLATE.md into your assistant, then give it your own inputs, or the sample ones from EXAMPLE.md.
3. Read what comes back. It marks what it checked and what is left for you.

*Workflow template · Sales · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/open-quotes-follow-up-list/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list)*

## The outcome

No quote goes quiet without someone noticing. Once a week, every open quote is sorted into the place it belongs: sent and never opened, opened with no answer, running out of validity inside your urgent window, past its validity date with no decision, or still sitting as a draft nobody sent. Each quote owner sees their own part of the list, with the quoted amount, the dates that matter and how many days have passed.

For every quote that is due a nudge, a short follow-up is already written for its owner, using only what the export shows: the quote number, the date it was sent, the quoted amount and, where it applies, the date it is valid until. The owner reads it, changes what they like and sends it, or decides not to.

The totals tie back to the export, currency by currency, so the reader knows nothing was skipped. They are labelled as quoted amounts, because that is all they are: the list gives no chance of winning and no forecast.

Prices, discounts and validity dates stay where they are. The workflow template changes none of them and offers none of them in a draft; if a quote needs a new price or a new date, a person decides and does it in the quoting tool. It sends nothing.

## Who starts the work, and when

The owner of the business, the sales lead or the estimator starts it once a week, usually on Monday morning, from a fresh export taken that day. Each quote owner reads their part, approves, edits or drops each follow-up and sends the ones they keep. Questions about the export itself go to whoever ran the list, who checks them in the quoting tool.

## What they supply

- **The quote status export from your quoting or proposal tool**, one row per quote, with these columns: quote ID, customer, contact, owner, amount, currency, created date, sent date, status (draft, sent, viewed, accepted, declined or expired), last viewed date and valid-until date. If your headers differ from the defaults, the workflow template stops and asks which column is which.
- **Your follow-up rules:** how many days after sending a quote with no view gets a first follow-up (three unless you change it), how many days after the last view with no answer (two), how close to the valid-until date counts as urgent (seven days), how long a draft may sit unsent before it is listed (two days), and who may be contacted, including any customer or quote to leave alone this week and why.
- **Today's date.**

It reads the status export only. It does not open the quotes themselves, and it needs no connection to your quoting tool.

## What comes out

One list in a fixed order. At the top, a count that places every row of the export in exactly one group, and the quoted amounts for each group by currency, adding up to the export's total. Then each owner's quotes, grouped as expired with no decision, expiring soon, viewed with no answer, sent and never viewed, and drafts not sent. Then the follow-up drafts, numbered, each addressed to the contact on the quote and signed by its owner, for the owner to approve and send. Then the open quotes not yet due, with the date each one will be; the questions about rows that do not make sense; and the quotes already accepted or declined. A section with nothing in it says so.

See the worked example in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Sales](https://fullypowered.ai/functions/sales/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list), which owns the quotes and the habit of following them up before they go cold.
- [Construction](https://fullypowered.ai/industries/construction/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list), where estimators send many priced bids and the ones nobody chases are quietly lost.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list), where quotes for custom parts and orders carry validity dates set by material prices.
- [Professional services](https://fullypowered.ai/industries/professional-services/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list), where proposals sit with a client for weeks and a polite nudge at the right time keeps the conversation alive.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list), where distributors and freight firms send rate and price quotes daily and need the week's open ones in one place.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list), when quotes go out faster than anyone can remember which ones were answered.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list), where the follow-up lives in one long-serving estimator's head and should be the same every week.

It sits beside [Sales pipeline review](https://fullypowered.ai/workflows/sales-pipeline-review/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list), which looks at the whole pipeline by stage and value, and [Deal close plan](https://fullypowered.ai/workflows/deal-close-plan/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list), which works one late deal through to signature. [Sales proposal preparation](https://fullypowered.ai/workflows/sales-proposal-preparation/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list) writes the proposal; this list makes sure someone follows it up once it is sent.

## What has to change for your company

Match the column headers to your export, or rename the columns once. Map your tool's own status words to the six this list knows. Set your follow-up rules: the days after sending, the days after a view, the urgent window and how long a draft may wait. Decide who may be contacted and who signs each follow-up, normally the quote's owner. Agree who reads the list and when the owners send their follow-ups. It runs in ChatGPT, Claude, Copilot or Gemini, from the export and notes you supply.

## What has been checked

FullyPowered AI wrote this workflow template. It was editorially reviewed on 19 November 2026. It was tried on its example on 19 November 2026 in one run, published with it. Edits after that run, to the date check, the export date, the totals line and the wording of "Not drafted:", have not been run again. It has not yet been tested in a client environment or as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past exports your sales lead remembers well, with hard cases written in advance: a renamed column, a quote shown as sent with a view recorded, a quote past its valid-until date that the tool still shows as viewed, a customer the owner is calling instead, two currencies in one export. The person who runs it checks every line against the quoting tool before any follow-up goes out. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list) describes the record we keep.

- Written by FullyPowered AI.
- Sources and rights reviewed.
- Editorially reviewed on 19 November 2026.
- Package format checked by script on every release.
- Tried once on its example in Claude on 19 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Sales pipeline review](../sales-pipeline-review/)
- [Deal close plan](../deal-close-plan/)
- [Sales proposal preparation](../sales-proposal-preparation/)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-open-quotes-follow-up-list&from=gh-sales-open-quotes-follow-up-list).
