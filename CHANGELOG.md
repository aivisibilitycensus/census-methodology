# Methodology changelog

Every change to the Census methodology is recorded here, newest first. Edition results always state which version of the methodology they were produced under. Canonical version: https://aivisibilitycensus.com/changelog/

## 31 October 2026: sites that turn our bot away

- When a site's home page turns CensusIndexBot away (HTTP 401, 403, 429 or 503), the CensusIndex reports it as a finding and does not score it. This is usually a firewall or CDN rule for unverified bots, and it does not show that Googlebot or Bingbot are blocked. The on-page checks for that site show as not checked.
- Census 100 entry bar: a brand fails only if its robots.txt blocks Googlebot or Bingbot, or its home page is marked noindex. A site that turns our own bot away is not failed for that.
- A home page that times out is retried once before the result is recorded. Method version 0.2.
- Status: draft.

## 30 October 2026: Census 100 engines and entry bar

- Perplexity is left out of the Census 100 for now, for the same reason it is left out of the editions. Its collector has failed on every run since setup. The Census 100 uses ChatGPT, Google Gemini and Google AI Mode, collected through Bright Data.
- Entry bar: a brand must be named in at least three answers to be ranked. A link to its site without its name no longer counts toward the three.
- Status: draft.

## 30 October 2026: Google search results and Google Maps listings added

- Each edition now also records Google’s search results for the closest everyday search to each question, searched from Dublin on the same dates, and the Google Maps listing of every firm an engine names.
- The search terms are fixed with the questions and published on the Editions page.
- Used to report how far AI answers overlap with Google rankings and whether review counts and ratings go with being named. Reported as associations, not causes.

## 30 October 2026: Claude and Perplexity left out of the editions for now

- Neither Claude nor Perplexity can currently be collected automatically and reliably with the free services the Census uses, and checking answers by hand on every date would not be repeatable. Both will be reconsidered for later editions.
- Google AI Mode is added, collected through Bright Data from Ireland.
- The editions now cover five engines: ChatGPT, Microsoft Copilot, Google Gemini, Google AI Overviews and Google AI Mode.

## 30 October 2026: Census 100 categories and brand names

- The Census 100 launches with five categories: project management, CRM, help desk, email marketing and social media management software. Each has 20 brands and 25 questions.
- Brand names that are also everyday words, such as Close or Later, count only when written with a capital letter, and every match for them is checked by hand.
- Status: draft.

## 30 October 2026: Names written as one word

- The Census Index and the Census 100 are now written as CensusIndex™ and Census100™. Earlier entries keep the names as they were written at the time.
- No change to the method.

## 30 October 2026: Edition 1 design and coding rules

- Sets out how each engine is collected: ChatGPT, Perplexity and Google Gemini through Bright Data, Google AI Overviews and Microsoft Copilot through SerpApi, and Claude by hand. Copilot cannot be given a location.
- Adds coding rules: what counts as a named firm, order by first appearance, matching name variants, directories and professional bodies recorded as sources, answers that name no firm kept in the totals, and a second independent check.
- Citations: only links shown to the reader count. Pages an engine read but did not show are recorded separately.
- Rankings: by share of answers that name a firm, published only when rankings from separate dates agree at a rank correlation of 0.8 or higher, with 90% ranges. The Census 100 uses the same rule and the same ranking measure.
- Edition 1: five sectors, 40 questions, three collection dates (27 November, 1 December and 4 December 2026), fixed before any data was collected. Listed on the [editions](https://aivisibilitycensus.com/editions/) page.
- Status: draft.

## 30 October 2026: Census 100 cadence and disclosure

- The Census 100 is published quarterly. Editions are labeled by quarter.
- Every brand is treated under the same rules. If anyone who publishes the Census works for a brand in a category, that category's page says so in one line.
- Status: draft.

## 30 October 2026: Census 100 coding and scope

- Census 100 Gemini answers come from Gemini Flash-Lite, and every Census 100 result notes this.
- The list launches with one category of up to 10 brands. The 100 builds up as categories are added.
- Status: draft.

## 30 October 2026: Census Index and Census 100 added

- Adds a [methodology](https://aivisibilitycensus.com/methodology/) section for two recurring measures by product category: the Census Index and the Census 100.
- Census Index: monthly readiness checks by our crawler, [CensusIndexBot](https://aivisibilitycensus.com/index-bot/), with an evidence grade on every check, using the same five grades as our free skills. Only checks graded [T] tested by the Census, [S] published study or [P] platform documentation count toward a site's result.
- Census 100: share of answers that name each brand, with citation share shown alongside, across ChatGPT, Perplexity, Google Gemini and Google AI Mode, with an entry bar and the same stable rankings rule as the editions.
- Status: draft. No Census Index or Census 100 results have been published yet.

## 29 October 2026: draft published

- First public draft of the [methodology](https://aivisibilitycensus.com/methodology/).
- Defines the two measures, mentions and citations, and reports them separately.
- Names the six engines: ChatGPT, Perplexity, Microsoft Copilot, Google Gemini, Google AI Overviews and Claude.
- Sets out fixed question sets per sector, repeated collection, and the recorded date, location and engine version for each answer.
- Status: draft. The methodology will be finalized and dated before Edition 1 is published.
