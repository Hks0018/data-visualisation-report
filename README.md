# Data Visualisation Report

A single-page, frosted-glass dashboard for exploring search visibility data for the Adani brand. Open `index.html` in a browser. There is nothing to install or build, and all data is embedded in the page.

## Tabs

- **Overview**: summary cards, charts and a column dictionary for the three tabs below.
- **Prompt List**: 149 prompts with Business, LLM, Topic, Topic Volume and Ai Response Preview.
- **Keyword Analysis**: 9,129 search results for 428 queries, with each query's Volume and Theme, plus section, position, title, link, domain, source, snippet, date and extra.
- **Brand Mention**: 293 mentions with Title, Content, Source, Domain and Category.

## Features

- Search and per-column filters on every tab, with counts that update as you filter.
- Click any bar, ring slice or ledger row to open a pop-up with the matching items and its own filters.
- Detail panel for every entry, with previous and next navigation.
- Sentiment (Positive, Neutral, Negative) on Brand Mention mentions and Keyword Analysis results.
- A "Sentiment by date and search type" graph, a categories-and-overall-sentiment card, and a one-line-per-domain summary table.
- Responsive layout, and animations that respect `prefers-reduced-motion`.

## Notes on the data

- **Sentiment is assigned by reading text.** It is not a field in the underlying data. Each mention and result was labelled from its title, snippet or content, judged by stance toward the Adani brand. Treat the labels as a first pass and spot-check before relying on them.
- **Dates.** Only 1,466 of the 9,129 results carry a date. Relative dates such as "2 months ago" are placed using late October 2026.
- Fonts load from Google Fonts. Everything else is self-contained.
