# Methodology

**Draft.** This methodology will be finalized and dated before Edition 1 is published. Any change after that is recorded in [CHANGELOG.md](CHANGELOG.md) and on the [methodology changelog](https://aivisibilitycensus.com/changelog/). Canonical version: https://aivisibilitycensus.com/methodology/

![Diagram of the five stages of a Census edition: fixed buyer questions, five AI engines, set dates with repeat runs, every answer coded for mentions and citations, published evidence](https://aivisibilitycensus.com/wp-content/uploads/figures/census-edition-method-diagram.svg)

*The five stages every edition follows, so one edition can be compared with the next.*

## What is measured

The Census records two things in each AI answer, and reports them separately:

- **Mention:** a firm or company is named in the text of the answer.
- **Citation:** a web page is cited or linked as a source for the answer.

A firm can be mentioned without its website being cited, and a page can be cited without the firm behind it being named. Treating them as one number would hide both.

![Diagram of two overlapping circles: mention only, where the firm is named but its site is not cited; citation only, where a page is cited but the firm is not named; and both](https://aivisibilitycensus.com/wp-content/uploads/figures/census-mentions-vs-citations.svg)

*Mentions and citations overlap but are not the same thing. In one August 2026 monitoring project, 12.9% of answers cited a firm’s own website while naming a different firm.*

## Engines

ChatGPT, Microsoft Copilot, Google Gemini, Google AI Overviews and Google AI Mode. Each engine keeps the same chart color in every edition.

### How each engine is collected

Most answers are collected through two third-party data services, Bright Data and SerpApi, which send each question to the engine’s public interface and return the full answer with its cited sources. Every raw answer is archived. This section is a draft: each route will be confirmed in a test run, and the final version dated, before Edition 1 data is collected.

| Engine | Collected by | Location |
| --- | --- | --- |
| ChatGPT | Bright Data, with web search allowed | Ireland |
| Google Gemini | Bright Data. In the 30 October test run, Gemini reported its model as Flash-Lite. | Ireland |
| Google AI Overviews | SerpApi, Google results for Ireland | Ireland |
| Microsoft Copilot | SerpApi | Cannot be set. Reported with each result. |
| Google AI Mode | Bright Data | Ireland |

### Google search results and Google Maps listings

Alongside the AI answers, each edition records two things the engines may draw on, so the results can show how closely AI recommendations follow them.

- **Google search results.** For each question we record Google’s results for the closest everyday search, for example “medical negligence solicitors dublin” for the medical negligence question. Searches are made from Dublin through Bright Data on the same dates as the AI answers. We record the organic results, the local map listings and any AI Overview shown. The search terms are published with the questions.
- **Google Maps listings.** For every firm an engine names, we record its Google Maps listing: rating, number of reviews, category and website, collected through Bright Data in the same week. Each match is checked against the firm’s website. Firms we cannot match are reported as unmatched.
- **How they are used.** We report how many of the firms each engine names also appear in Google’s top 10 results and map listings, and whether firms with more reviews or higher ratings are named more often. These are associations, not proof of cause. An engine may name a firm for the same reasons Google ranks it.

### How answers are coded

- **Named firm.** A firm counts as named when the answer presents it as an option, a recommendation or an example. A firm mentioned only as something to avoid is recorded separately.
- **Order.** Each named firm gets a position by its first appearance in the answer.
- **One firm, one name.** Trading names, branches and spelling variants are matched to a single firm. The full matching list is published with the results.
- **Directories and bodies.** Regulators, professional bodies and directories (for example a law society or a central bank register) are recorded as pointed-to sources, not as firms.
- **No firm named.** Answers that name no firm, or decline to recommend one, are counted as such and stay in the totals.
- **Citations.** A citation is a link the engine shows to the reader, in its list of sources or in the answer text. Pages an engine read but did not show are recorded separately and not counted. Citations are counted separately from mentions, by domain.
- **Checking.** Coding is done with the help of an AI model and then checked against the answer text in a second, independent pass. Disagreements are resolved and logged. Every coded answer is published so anyone can check it.
- **Stable rankings only.** A sector’s firm ranking is published only when the rankings from separate collection dates agree, with a rank correlation (Spearman) of 0.8 or higher. Firms are ranked by their share of answers that name them, and citation counts are shown alongside. Each firm’s share is shown with a 90% range, and firms whose ranges overlap are shown as level. If a sector’s ranking is not stable, we publish the counts without ranking them. The Census100™ uses the same rule.

## Questions

Each sector has a fixed set of buyer questions, written the way a buyer would ask them, for example a question asking which firms to consider for a particular service in a particular place. The same questions are reused across editions so results can be compared. Every question is published in full with each edition. How we write and test buyer questions is explained in [Keyword research for AI search](https://aivisibilitycensus.com/keyword-research-for-ai-search/).

## Collection

Questions are asked on set dates from the market being measured, where the engine allows a location to be set (see the table above). The date, location and engine version (where an engine shows it) are recorded with every answer. AI answers vary between runs, so each question is asked more than once and the variation is reported. In Edition 1, every question is asked once on each engine on each of three dates, giving three answers per question per engine. The Edition 1 sectors and questions are listed on the [editions](https://aivisibilitycensus.com/editions/) page.

## CensusIndex™ and Census100™

Alongside the editions, the Census runs two recurring measures by product category, starting with five: project management, CRM, help desk, email marketing and social media management software. Neither has published results yet. When they do, each release states the methodology version it used.

### CensusIndex: readiness checks

Once a month our crawler, CensusIndexBot, reads a few public files on each site in a category: robots.txt, the home page as plain HTML and in a headless browser, the sitemap, and llms.txt. What it requests and how to opt out are on the [CensusIndexBot page](https://aivisibilitycensus.com/index-bot/).

Each check reports a pass, a warning or a fail, with the fix for anything that fails. Every check also carries one of the evidence grades used across the Census, including in our [free skills](https://aivisibilitycensus.com/tools/):

- **[T] Tested by the Census:** we tested it and published the result.
- **[S] Published study:** a study with a stated method found an effect.
- **[P] Platform documentation:** the search engine or AI company says so in its own documentation.
- **[V] Vendor claim:** claimed by a vendor or practitioner, not independently checked.
- **[U] Untested:** no evidence found either way.

Only [T], [S] and [P] checks count toward a site's result. [V] and [U] checks, such as llms.txt, are shown with their fix but never change the result. A grade changes only when the evidence does. Blocking AI training bots is a business choice, so it is reported and never scored. We publish category totals. Each site's own results page is hidden from search engines unless its owner asks for it to be public.

### Census100: measured AI visibility

Each category has a fixed set of buyer questions, asked on ChatGPT, Google Gemini and Google AI Mode through Bright Data, on at least two separate dates. Gemini answers come from Gemini Flash-Lite, the model Bright Data's Gemini scraper reports, and every Census100 result notes this. Brands are ranked by their share of answers that name them, using the same named-firm rule as the editions. Citation share, the percentage of answers that link to the brand's own website, is shown alongside but does not set the rank. Citations are counted under the same rule as the editions.

To be ranked, a brand must be named in at least three answers (a link to its site without its name does not count), and, in the same month's CensusIndex, its robots.txt must allow Googlebot and Bingbot and its home page must not be marked noindex. A site that turns our own bot away is not failed for that; it is reported as a finding. A brand that would otherwise rank but fails this entry bar is shown as not eligible, with the reason, rather than left out. Rankings follow the stable rankings rule above: each brand's share is shown with a 90% range from resampling the questions, brands whose ranges overlap are marked as level, and a category is published only when rankings from separate dates agree at a rank correlation of 0.8 or higher. Up to 10 brands are listed per category. The list launches with five categories, so it starts with up to 50 brands, and the 100 builds up as categories are added. The Census100 is published quarterly, and each edition is labeled by quarter, for example Q4 2026.

Brand names are matched as whole words. Names that are also everyday words, such as Close or Later, count only when written with a capital letter, and are checked by hand. No brand can pay to be listed. Every brand is treated the same way under the same rules. If anyone who publishes the Census works for a brand in a category, that category's page says so in one line.

## Limits

- Results are a snapshot of what the engines returned on the dates tested, not a measure of a firm's quality.
- Answers can change when engines update their models or sources.
- A firm not named for one question may be named for a differently worded one.

## Corrections

If a result looks wrong, the published question set and dates allow it to be checked. Confirmed errors are corrected and the correction is noted on the edition page.

## License

Edition data and question sets are published under [CC BY 4.0](https://aivisibilitycensus.com/data-license/). Anyone can reuse them with credit, and anyone can rerun the questions to check our results.
