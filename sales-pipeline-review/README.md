# Sales pipeline review

The whole open pipeline on one page each week: value by stage, what moved, deals at risk and coverage. Figures trace to your export; a person commits it.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** This is a template, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See Sales pipeline review on our website](https://fullypowered.ai/workflows/sales-pipeline-review/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review). Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Quick start**

1. Read EXAMPLE.md to see what a good result looks like.
2. Copy all of TEMPLATE.md into your assistant, then give it your own inputs, or the sample ones from EXAMPLE.md.
3. Read what comes back. It marks what it checked and what is left for you.

*Workflow template · Sales · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/sales-pipeline-review/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review)*

## The outcome

Your sales lead walks into the week holding the entire pipeline, not just the deals that happen to be loudest. The page shows how much sits in each stage and how long it has been there, which deals came in, moved forward, slipped back, closed or quietly vanished since last week, and a bridge that proves last week's total became this week's.

Deals that need attention are named with the exact reasons: a close date that has passed or moved out, no next step, weeks without activity, too long in one stage. Each comes with one question for its owner. Coverage of what is left of your target is a plain ratio against the bar you set.

The forecast stays a human call. The review lays out the figures a forecast rests on and leaves the number blank for the person who commits it. Rates are held back until enough closed deals sit behind them, so nobody steers by a figure built on three deals.

## Who starts the work, and when

The sales lead, the owner or whoever keeps the deal record runs it once a week, on the same day, from that day's export and last week's. It is also worth running the morning of a forecast call or a board update, so the numbers on the table are ones you can trace.

The sales lead reads the review and chooses the week's actions. The person named to commit the forecast fills in the number. The AI assistant changes nothing in your sales system and sends nothing.

## What they supply

- **This week's export.** Every open deal, plus deals closed in recent months, from your sales system or spreadsheet, with fixed columns: deal, account, owner, stage, amount, close date, created date, date it entered its stage, next step and its date, last activity, status and closed date.
- **Last week's export,** in the same columns, so the review can say what moved.
- **Your facts.** The review date, the period you are selling into and its target, your stages in order with an optional weight and day limit for each, and who commits the forecast.

## What comes out

One review in a fixed order:

1. **Coverage:** what was read, what was not, and any deal that was open last week and is missing now.
2. **Headline:** open deals and value, won so far, deals at risk and coverage, in two lines.
3. **By stage:** count, value, last week's value and whether it truly moved, weighted value, average days in stage, missing next steps, quiet deals and deals over the limit.
4. **Since last week:** new, advanced, moved back, close dates changed, amounts changed, won, lost and missing, ending in the bridge.
5. **This period:** won so far, open deals closing in the period, the remaining target and coverage.
6. **Deals at risk,** largest first, each with its reasons and a question for its owner.
7. **Closed-deal baseline:** win rate and cycle length, or the counts alone when there are too few deals.
8. **For the forecast:** the figures a forecast rests on, and a blank line for the person who commits it.
9. **Where to look first:** at most three actions, each tied to a figure on the page, then the gaps in the export.

A good review is one the sales lead can defend number by number, because every number leads back to a row.

See the worked example in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Sales](https://fullypowered.ai/functions/sales/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review): the weekly look at the whole pipeline, done the same way every time.
- [Analytics and reporting](https://fullypowered.ai/functions/analytics-and-reporting/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review): the pipeline turned into figures someone can check.
- [Professional services](https://fullypowered.ai/industries/professional-services/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review): engagements of very different sizes sit side by side, and value by stage tells more than a deal count.
- [Software technology](https://fullypowered.ai/industries/software-technology/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review): many deals move through several stages at once, and a weekly bridge shows where value went.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review): large orders with long cycles, where a close date that keeps moving out is the early warning.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review): contract bids pile up near quarter end, and coverage against the target says whether there is enough in play.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review): the pipeline has outgrown the sales lead's memory and needs one page that everyone reads the same way.

It sits beside [Stalled-deal review](https://fullypowered.ai/workflows/stalled-deal-review/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review), which takes the deals flagged here one at a time and reads each against its stage, and [Sales call preparation brief](https://fullypowered.ai/workflows/sales-call-preparation-brief/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review), which prepares the call where an owner's question gets answered.

## What has to change for your company

- **Your export.** Agree the columns once. If your sales system names them differently, write down which column is which; the assistant stops and asks rather than guess.
- **Your stages.** List them in order. Add a weight for each if you use weighted pipeline, and a day limit if you want long stays flagged.
- **Your thresholds.** How many quiet days count as quiet, how big a change counts as movement, and how many closed deals a rate needs. Sensible starting values are given.
- **Your target and bar.** The target for the period and the coverage you consider healthy. Without them the review shows the pipeline but makes no comparison.
- **Who commits the forecast.** Name the person. The review never fills in that number.
- **Your platform.** The instructions are written to be pasted into ChatGPT, Claude, Copilot or Gemini. It works from the exports you supply and needs no connection to your sales system.

## What has been checked

FullyPowered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried on its example in Claude on 9 November 2026, and the record of that run, which replaced an earlier one from the same day after the instructions were revised, is published with the template. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on past weeks your sales lead remembers well, plus hard cases written in advance, each with its expected behavior: an export whose headers differ, a deal with no amount, a deal that disappears between weeks, a close date pushed out, too few closed deals for a rate. The sales lead checks every figure against the exports before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review) builds that test set, and [What we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review) shows the record.

- Written by FullyPowered AI.
- Sources and rights reviewed.
- Editorially reviewed on 9 November 2026.
- Package format checked by script on every release.
- Tried once on its example in Claude on 9 November 2026. The record is in [TRIAL.md](TRIAL.md).
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

- [Stalled-deal review](../stalled-deal-review/)
- [Sales call preparation brief](../sales-call-preparation-brief/)
- [Sales proposal preparation](../sales-proposal-preparation/)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=sales-sales-pipeline-review&from=gh-sales-sales-pipeline-review).
