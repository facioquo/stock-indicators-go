---
title: Exponential Moving Average (EMA)
description: Exponentially [weighted] Moving Average is a rolling moving average that puts more weight on current price.
permalink: /i/ema/
type: moving-average
layout: indicator
---

# {{ page.title }}

[Exponentially weighted moving average](https://en.wikipedia.org/wiki/Moving_average#Exponential_moving_average) is a rolling moving average that puts more weight on current price.
[[Discuss] &#128172;]({{site.dotnet.discussions}}/256 "Community discussion about this indicator")

![chart for {{page.title}}]({{site.dotnet.charts}}/Ema.png)

```go
// Go usage syntax (with Close price)
[...]
```

## Parameters

**`lookbackPeriods`** _`int`_ - Number of periods (`N`) in the moving average.  Must be greater than 0.

### Historical quotes requirements

You must have at least `2×N` or `N+100` periods of `quotes`, whichever is more, to cover the convergence periods.  Since this uses a smoothing technique, we recommend you use at least `N+250` data points prior to the intended usage date for better precision.

`quotes` is a collection of generic `TQuote` historical price quotes.  It should have a consistent frequency (day, hour, minute, etc).  See [the Guide]({{site.baseurl}}/guide/#historical-quotes) for more information.

## Response

```go
[...]
```

- This method returns a time series of all available indicator values for the `quotes` provided.
- It always returns the same number of elements as there are in the historical quotes.
- It does not return a single incremental indicator value.
- The first `N-1` periods will have `null` values since there's not enough data to calculate.

>&#9886; **Convergence warning**: The first `N+100` periods will have decreasing magnitude, convergence-related precision errors that can be as high as ~5% deviation in indicator values for earlier periods.

### EmaResult

**`Timestamp`** _`DateTime`_ - date from evaluated `TQuote`

**`Ema`** _`double`_ - Exponential moving average

### Utilities

...

See [Utilities and helpers]({{site.baseurl}}/utilities#utilities-for-indicator-results) for more information.

## Chaining

This indicator may be generated from any chain-enabled indicator or method.

```go
// example
[...]
```

Results can be further processed on `Ema` with additional chain-enabled indicators.

```csharp
// example
[...]
```
