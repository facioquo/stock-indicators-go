---
title: Stochastic Oscillator
description: Created by George Lane, the Stochastic Oscillator, also known as KDJ Index, is a momentum oscillator that compares current financial market price with recent highs and lows and is presented on a scale of 0 to 100.  %J is also included for the KDJ Index extension.
permalink: /i/stoch/
type: oscillator
layout: indicator
---

# {{ page.title }}

Created by George Lane, the [Stochastic Oscillator](https://en.wikipedia.org/wiki/Stochastic_oscillator), also known as KDJ Index, is a momentum oscillator that compares current price with recent highs and lows and is presented on a scale of 0 to 100.
[[Discuss] &#128172;]({{site.dotnet.discussions}}/237 "Community discussion about this indicator")

![chart for {{page.title}}]({{site.dotnet.charts}}/Stoch.png)

```go
[...]
```

## Parameters

**`lookbackPeriods`** _`int`_ - Lookback period (`N`) for the oscillator (%K).  Must be greater than 0.  Default is 14.

**`signalPeriods`** _`int`_ - Smoothing period for the signal (%D).  Must be greater than 0.  Default is 3.

**`smoothPeriods`** _`int`_ - Smoothing period (`S`) for the Oscillator (%K).  "Slow" stochastic uses 3, "Fast" stochastic uses 1.  Must be greater than 0.  Default is 3.

**`kFactor`** _`double`_ - Optional. Weight of %K in the %J calculation.  Must be greater than 0. Default is 3.

**`dFactor`** _`double`_ - Optional. Weight of %D in the %J calculation.  Must be greater than 0. Default is 2.

**`movingAverageType`** _`MaType`_ - Optional. Type of moving average (SMA or SMMA) used for smoothing.  Default is `MaType.SMA`.

### Historical quotes requirements

You must have at least `N+S` periods of `quotes` to cover the warmup periods.

...
