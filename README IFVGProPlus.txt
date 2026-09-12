IFVG Pro+ [TheTradingPharmD]

A lightweight NinjaTrader 8 indicator that detects and displays confirmed Inverse Fair Value Gap (IFVG) setups while using hidden Higher Timeframe Fair Value Gap and liquidity sweep logic as optional confluence filters.

Developed by TheTradingPharmD.

Overview

IFVG Pro+ was built to keep charts clean and responsive. The indicator only draws confirmed IFVG setups. The HTF FVG and liquidity engines run in the background and do not draw boxes, swing lines, emojis, or labels.

This keeps the confluence logic available without creating unnecessary visual overlap or adding extra chart objects.

Features

Bullish and bearish IFVG detection

Single or Series detection modes

Neutral, Bullish, or Bearish bias options

Optional hidden 15-minute HTF FVG filter

Optional hidden liquidity sweep filter

HTF FVG + liquidity filters use OR logic when both are enabled

Minimum IFVG size filter

Optional 7–15 candle IFVG window

Optional break-even integrity filter

Adjustable setup history

Optional IFVG confirmation line and label

Potential IFVG alerts

Bullish and bearish confirmed IFVG alerts

Failed IFVGs automatically removed from the chart

Performance-focused NinjaScript design

Confluence Filter Logic

The filters work independently:

HTF FVG ON + Liquidity OFF: HTF FVG confluence only

HTF FVG OFF + Liquidity ON: liquidity sweep confluence only

Both ON: either filter can qualify the setup

Both OFF: IFVG logic runs without a confluence filter

The current NinjaTrader build uses a hidden 15-minute HTF FVG engine.

Default Settings

Filter by HTF FVG: On

Filter by Liquidity Sweep: Off

Detection: Single

Bias: Neutral

Allow 7–15 Candle IFVGs: On

Require BE not breached on inversion: On

Number of Setups Displayed: 4

Minimum IFVG Size: 5 points

Show IFVG Line & Label: Off

Alerts: Off

IFVG Failure Logic

Confirmed IFVGs are automatically removed when they fail:

A bullish IFVG is removed after a later candle closes below the bottom of the IFVG.

A bearish IFVG is removed after a later candle closes above the top of the IFVG.

The IFVG box and any associated line or label are removed together.

Installation

Download the NinjaTrader ZIP file and do not unzip it. In NinjaTrader 8, go to Tools → Import → NinjaScript Add-On, select the ZIP file, and complete the import. Then open a chart, right-click → Indicators, add IFVG Pro+ [TheTradingPharmD], and click Apply → OK. If the indicator does not appear immediately, restart NinjaTrader.

Performance Notes

IFVG Pro+ is designed to minimize chart load time:

Hidden HTF FVGs are calculated but never drawn.

Hidden liquidity sweeps are calculated but never drawn.

Hidden engines only run when their corresponding filter is enabled.

Only confirmed IFVG setups create chart objects.

The indicator uses Calculate.OnBarClose for improved performance.

Candidate and setup history are capped to avoid unnecessary long-term tracking.

Alerts

The indicator includes optional alerts for:

Potential IFVG Setup

Bullish IFVG Confirmed

Bearish IFVG Confirmed

Alerts are disabled by default and only fire in real time.

Disclaimer

This indicator is provided for educational and analytical purposes only. It does not constitute financial advice, a recommendation to trade, or a guarantee of future results. Always use proper risk management and independently evaluate any trading setup.

IFVG Pro+ [TheTradingPharmD]
Built for clean charts, focused confluence, and efficient NinjaTrader 8 performance.