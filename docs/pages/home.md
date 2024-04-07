---
title: Stock Indicators for Go
description: >-
  Transform financial market prices into technical analysis insights with Go language library.
permalink: /
layout: base
lazy-images: true
---

<h1 style="display:none;">{{ page.title }}</h1>

**Stock Indicators for Go** is a library package that produces financial market technical indicators.  Send in historical price quotes and get back desired indicators such as moving averages, Relative Strength Index, Stochastic Oscillator, Parabolic SAR, etc.  Nothing more.

Build your private technical analysis, trading algorithms, machine learning, charting, or other intelligent market software with this library and your own [OHLCV]({{site.baseurl}}/guide/#historical-quotes) price quotes sources for equities, commodities, forex, cryptocurrencies, and others.  **Stock Indicators** [**for C# .NET**](https://dotnet.stockindicators.dev/) and [**for Python**](https://python.stockindicators.dev/) are also available.

Explore more information:

- [Indicators and overlays]({{site.baseurl}}/indicators/#content)
- [Guide and Pro tips]({{site.baseurl}}/guide/#content)
- [Utilities and helper functions]({{site.baseurl}}/utilities/#content)
- [Demo site](https://charts.stockindicators.dev/) (a stock chart)
- [Release notes]({{site.github.repository_url}}/releases)
- [Discussions]({{site.dotnet.discussions}})
- [Contributing guidelines]({{site.baseurl}}/contributing/#content)

## Reputable and extensible indicators

You'll get all of the industry standard indicators out-of-the-box.

<img alt="sample indicators shown in chart"
  data-src="https://raw.githubusercontent.com/DaveSkender/Stock.Indicators/main/docs/examples.webp"
  style="aspect-ratio:900/748;"
  class = "lazyload" />

## Easy to use in your application

```go
// example: get 20-period simple moving average
[...]
```

See more [usage examples]({{site.baseurl}}/guide/#example-usage).

## Use chaining for unique insights

Optional chaining enables advanced uses cases; such as, indicator of indicators, slope (direction) of any result, or [moving average]({{site.baseurl}}/indicators/#moving-average) of an indicator.

```go
[...]
```

See the [guide]({{site.baseurl}}/guide/#content) and the [full list of indicators and overlays]({{site.baseurl}}/indicators/#content) for more information.

## Optimized for modern Go frameworks

Our Go library directly targets all current frameworks for peak performance, including the .NET Standard for older framework compatibility.

- ...

## Licensed for everyone

<a href="https://opensource.org/licenses/Apache-2.0"><img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=flat-square&cacheSeconds=259200" alt="Apache 2.0 license badge" width="124" height="20" class="lazyload" /></a>

This repository uses the standard Apache 2.0 open-source license.  Please review the [license](https://opensource.org/licenses/Apache-2.0) before using or contributing to the software.

## Share your ideas with the community

**Need help?**  Have ideas?  [Start a new discussion, ask a question &#128172;]({{site.dotnet.discussions}}), or [submit an issue]({{site.github.repository_url}}/issues) if it is publicly relevant.

## Give back with patronage

Thank you for your support!  This software is crafted with care by unpaid enthusiasts who &#128150; all forms of encouragement.  If you or your organization use this library or like what we're doing, add a &#11088; on the [GitHub Repo]({{site.github.repository_url}}) as a token of appreciation.

If you want to buy me a beer or are interested in ongoing support as a patron, [become a sponsor](https://github.com/sponsors/facioquo).  Patronage motivates continued maintenance and evolution of open-source projects, and to inspire new ones.

## Contribute to help others

This Go package is an open-source project [on GitHub](https://github.com/facioquo/stock-indicators-go).  If you want to report bugs or contribute fixes, new indicators, or new features, please review our [contributing guidelines]({{site.baseurl}}/contributing/#content) and [the backlog](https://github.com/orgs/facioquo/projects/15).

Special thanks to all of our community code contributors!

<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block">
     <a href="{{ contributor.html_url }}" width="75" height="75"><img data-src="{{ contributor.avatar_url }}&s=75" width="75" height="75" class="circle lazyload" alt="{{ contributor.login }} avatar" /></a>
  </li>
{% endfor %}
</ul>

&#187; see our [full list of indicators and overlays]({{site.baseurl}}/indicators/#content)
