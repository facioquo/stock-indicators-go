---
title: Guide and Pro tips
description: Learn how to use the Stock Indicators for Go library in your own software tools and platforms.  Whether you're just getting started or an advanced professional, this guide explains how to get setup, example usage code, and instructions on how to use historical price quotes, make custom quote classes, chain indicators of indicators, and create custom technical indicators.
permalink: /guide/
relative_path: pages/guide.md
layout: page
---

# {{ page.title }}

<nav role="navigation" aria-label="guide page menu">
<ul class="pipe-list">
  <li><a href="#installation-and-setup">Installation and setup</a></li>
  <li><a href="#prerequisite-data">Prerequisite data</a></li>
  <li><a href="#example-usage">Example usage</a></li>
  <li><a href="#historical-quotes">Historical quotes</a></li>
  <li><a href="{{site.baseurl}}/utilities/#content">Utilities and helper functions</a></li>
  <li><a href="{{site.baseurl}}/contributing/#content">Contributing guidelines</a></li>
</ul>
</nav>

## Getting started

### Installation and setup

Find and install the [stock-indicators](https://pkg.go.dev) Go package into your Project.  See more [help for installing packages](https://go.dev/doc/modules/managing-dependencies).

```powershell
[...]
```

### Prerequisite data

Most indicators require that you provide historical quote data and additional configuration parameters.

You must get historical quotes from your own market data provider.  For clarification, the `GetHistoricalQuotes()` method shown in the example below **is not part of this library**, but rather an example to represent your own acquisition of historical quotes.

...

### Example usage

All indicator methods will produce all possible results for the provided historical quotes as a time series dataset -- it is not just a single data point returned.  For example, if you provide 3 years worth of historical quotes for the SMA method, you'll get 3 years of SMA result values.

```go
[..]
```

```console
SMA on 4/19/2018 was $255.0590
SMA on 4/20/2018 was $255.2015
SMA on 4/23/2018 was $255.6135
SMA on 4/24/2018 was $255.5105
SMA on 4/25/2018 was $255.6570
SMA on 4/26/2018 was $255.9705
..
```

See [individual indicator pages]({{site.baseurl}}/indicators/) for specific usage guidance.

More examples available:

- [Example usage code]({{site.baseurl}}/guide/#content) in a simple working console application
- [Demo site](https://charts.stockindicators.dev) (a stock chart)

## Historical quotes

...

### Where can I get historical quote data?

There are many places to get financial market data.  Check with your brokerage or other commercial sites.  If you're looking for a free developer API, see our ongoing [discussion on market data]({{site.dotnet.discussions}}/579) for ideas.

### How much historical quote data do I need?

Each indicator will need different amounts of price `quotes` to calculate.  You can find guidance on the individual indicator documentation pages for minimum requirements; however, **most use cases will require that you provide more than the minimum**.  As a general rule of thumb, you will be safe if you provide 750 points of historical quote data (e.g. 3 years of daily data).

> &#128681; **IMPORTANT! Applying the _minimum_ amount of quote history as possible is NOT a good way to optimize your system.**  Some indicators use a smoothing technique that converges to better precision over time.  While you can calculate these with the minimum amount of quote data, the precision to two decimal points often requires 250 or more preceding historical records.
>
> For example, if you are using daily data and want one year of precise EMA(250) data, you need to provide 3 years of historical quotes (1 extra year for the lookback period and 1 extra year for convergence); thereafter, you would discard or not use the first two years of results.  Occasionally, even more is required for optimal precision.
>
> See [discussion on warmup and convergence]({{site.dotnet.discussions}}/688) for more information.

## Utilities

See [Utilities and helper functions]({{site.baseurl}}/utilities/#content) for additional tools.
