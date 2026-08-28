# Visual Data Discovery — Paris & Barcelona Airbnb

Coursework project for COMP10002 Data Warehouse Environment, University of the West of Scotland.

I picked Paris and Barcelona partly because I'd visited Paris myself and wanted to understand its short-term rental market better, and partly because a family member described Barcelona as an incredibly lively city that I wanted to dig into. Turned out to be a good analytical pairing too — both are major tourist cities with large, active Airbnb markets, but they regulate short-term rentals very differently, and that shows up clearly in the data.

## Data

Sourced from Inside Airbnb, a project that scrapes and publishes Airbnb listing data specifically to support housing policy research.

- Paris: 82,216 listings, 18 columns
- Barcelona: 18,198 listings, 19 columns

The price column was empty in both datasets — a known gap in recent Inside Airbnb exports — so the analysis leans on availability, minimum nights, review counts and host listing counts instead.

## What the numbers show

Paris has a mean minimum-night requirement of 44 days against Barcelona's 16.6, even though both cities share a median of just 3. That gap is a small cluster of Paris listings with very high minimums, almost certainly a reaction to France's 120-night annual cap on short-term lets.

Barcelona listings are available for 210 days a year on average versus 127 in Paris, and Barcelona's availability distribution actually skews negative (-0.43) — meaning the bulk of listings sit at the high end. Combined with entire-home listings dominating both markets (88% in Paris, roughly two-thirds in Barcelona), it points to both cities being run largely by commercial operators rather than casual hosts renting out a spare room now and then.

Buttes-Montmartre is the single densest neighbourhood in Paris, with around 8,500 listings, and the top neighbourhoods all show high average availability — consistent with professionally managed short-term rental stock rather than people renting out a room occasionally.

## Visualisations

Eight built in Tableau Public:

1. Geographic map of Paris listings by neighbourhood
2. Room type breakdown, Paris
3. Top 10 Paris neighbourhoods by listing count
4. Average availability by neighbourhood
5. Reviews vs. availability scatter
6. Room type treemap, Paris
7. Room type breakdown, Barcelona
8. Combined dashboard — map, room types and top neighbourhoods together

## Evaluating Tableau

I ran the System Usability Scale after finishing the build and scored it 60/100 — just under the 68 mark usually treated as the line between "acceptable" and "good." Honestly that tracks. The output quality (especially the map and dashboard) is genuinely strong, but getting there meant learning the dimensions-vs-measures distinction, converting lat/long into individual dimensions rather than aggregates, and building separate worksheets before you can even start assembling a dashboard. None of that is obvious on a first attempt. Three to six months for a team to get properly comfortable with it sounds about right based on this experience.

## Repo layout

```
paris-listings.xlsx       raw Paris dataset (Inside Airbnb)
barcelona-listings.xlsx   raw Barcelona dataset (Inside Airbnb)
airbnb-comparison.twb     Tableau workbook with all 8 visualisations
report.pdf                full written report, definitions, market context and findings
```

## Tools

Tableau Public, Excel for the descriptive stats, data from Inside Airbnb.

## Data source

Listings data © Inside Airbnb, used under their open data terms for non-commercial analysis — [insideairbnb.com](http://insideairbnb.com/about/)

Find more of my work at [github.com/hashimmohamedcogc](https://github.com/hashimmohamedcogc).
