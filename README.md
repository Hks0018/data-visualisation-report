# Data Visualisation Report

A single-page dashboard for exploring search visibility data for the Adani brand. Open `index.html` in a browser. There is nothing to install or build, and all data is embedded in the page.

## Tabs

- **Overview**: summary cards, charts and a column dictionary for every table.
- **Prompt List**: prompts for four Businesses (Adani Airports, Adani Energy Solutions, Adani Ports and Adani Connex), in four sub-tabs.
  - **Prompts**: 119 prompts with Brand coverage %, Brand sentiment (avg), Favourable, Neutral and Unfavourable counts, and Brand mentions and Total mentions (Scored answers for Adani Ports).
  - **Citations**: 9,748 citations with Provider, Brand mentioned, Brand sentiment, Sentiment score, Citation URL, Published, Domain, Website type and Cited page of.
  - **Sources**: 1,194 cited domains with Brand or competitor, Website type, Citations, Domain coverage (%), Sentiment score, Sentiment and Scored answers.
  - **Pages**: 1,911 cited pages with URL, Title, Times cited and Brand or competitor.
- **Keyword Analysis**: 9,129 search results for 428 queries, with each query's Volume and Theme, plus section, position, title, link, domain, source, snippet, date and extra.
- **Brand Mention**: 293 mentions with Title, Content, Source, Domain and Category.

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
- Fonts load from Google Fonts. Everything else is self-contained.
