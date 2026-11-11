# Data Visualisation Report

A single-page dashboard for exploring search visibility data for the Adani brand. Open `index.html` in a browser. There is nothing to install or build, and all data is embedded in the page.

## Tabs

- **Overview**: summary cards, charts and a column dictionary for every table.
- **Dashboard**: the metrics framework in four sections, plus sentiment over time.
  - **Over time**: a stacked sentiment-by-date graph (citations or search results; last 7, 30, 90 days or 24 months) and Last 7 days cards with net sentiment against the previous 7 days.
  - **A. AI Visibility**: prompts where Adani is mentioned, average Brand coverage and visibility by AI platform.
  - **B. Narrative**: Favourable, Neutral and Unfavourable classification, negative narrative prevalence and net sentiment.
  - **C. Source**: sources cited, Adani-owned, third-party and competitor citations, and source diversity.
  - **D. BU Discovery**: a Business comparison, competitor visibility, category and query visibility.
  - A Business dropdown applies to Prompt List data. Keyword Analysis and Brand Mention always show everything.
- **Prompt List**: prompts for four Businesses (Adani Airports, Adani Energy Solutions, Adani Ports and Adani Connex), in four sub-tabs.
  - **Prompts**: 119 prompts with Brand coverage %, Brand sentiment (avg), Favourable, Neutral and Unfavourable counts, and Brand mentions and Total mentions (Scored answers for Adani Ports).
  - **Citations**: 9,748 citations with Provider, Brand mentioned, Brand sentiment, Sentiment score, Citation URL, Published, Domain, Website type and Cited page of.
  - **Sources**: 1,194 cited domains with Brand or competitor, Website type, Citations, Domain coverage (%), Sentiment score, Sentiment and Scored answers.
  - **Pages**: 1,911 cited pages with URL, Title, Times cited and Brand or competitor.
- **Keyword Analysis**: 9,129 search results for 428 queries, with each query's Volume and Theme, plus section, position, title, link, domain, source, snippet, date and extra.
- **Brand Mention**: 293 mentions with Title, Content, Source, Domain and Category.
- **Research**: four sub-tabs, each with search, sort, dropdown filters, charts and a detail panel.
  - **Keywords**: 34,973 rows with Platform, Keyword, Position, Intent, Position Type, SERP Type, Sentiment and Theme.
  - **Backlink Sentiments**: 25,542 rows across 19 columns.
  - **RAW Backlinks**: 25,212 rows as exported, with any cells beyond the Comment column shown in "More cells".
  - **Prompts Matrix**: the planning tables for sentiment, language and required keywords, volume and prompts.

## Features

- Search, sort and dropdown filters on every table, with counts that update as you filter. The filter bar can be minimised.
- Click any bar, ring slice or ledger row to open a pop-up with the matching items and its own dropdown filters.
- Detail panel for every entry, with previous and next navigation.
- Sentiment (Positive, Neutral, Negative) on Brand Mention mentions and Keyword Analysis results, and Favourable, Neutral and Unfavourable on prompts and citations.
- A "Sentiment by date and search type" graph and a categories-and-overall-sentiment card.
- A one-line-per-domain table (Domain, Category or Website type, Sentiment, Overall sentiment and count) on Keyword Analysis, Brand Mention and every Prompt List tab. Overall is the most common sentiment for the domain, for example "Neutral · 30".
- Responsive layout, and animations that respect `prefers-reduced-motion`.

## Notes on the data

- **Keyword Analysis and Brand Mention sentiment is assigned by reading text.** It is not a field in the underlying data. Each mention and result was labelled from its title, snippet or content, judged by stance toward the Adani brand. Treat the labels as a first pass and spot-check before relying on them.
- **Prompt List** comes from exported reports. Adani Ports reports Scored answers instead of Brand mentions and Total mentions, and has no Sentiment in Sources and no Pages table. Adani Energy Solutions has no Sources or Pages report. Sources and Pages show the newest report for each Business.
- **Sources sentiment** is Positive or Neutral only. Negative is listed in the chart and filter, but no source has it: the lowest Sentiment score is -5 and Negative starts at -15.
- **Website type** labels can differ between the Citations and Sources exports for the same domain. Each table keeps its own labels.
- **Dates.** Only 1,466 of the 9,129 Keyword Analysis results carry a date. Relative dates such as "2 months ago" are placed using late October 2026.
- **Research** data is stored compressed inside the page and unpacked the first time each sub-tab is opened (about a second). About 1,050 RAW Backlinks rows have cells shifted by one column and some text is garbled in the original; both are shown as exported. Dates display as YYYY-MM-DD. Intent and SERP Type filters merge capitalisation variants; tables show the raw values. The empty "Keywords" block is noted under Prompts Matrix.
- **Dashboard dates** are citation Published dates and search result dates, so they show when content was published, not when an AI platform answered. "Last 7 days" is 20 to 26 Oct 2026, the newest date in the data. Adani Ports citations have no dates. The desired factual narratives, Balanced-context score and credible third-party list are not in the data, so they are shown as not available.
- Fonts load from Google Fonts. Everything else is self-contained.
