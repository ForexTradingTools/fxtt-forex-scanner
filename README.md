# FxTT Multi-purpose Forex Scanner – Free MT4 Indicator

![MQL4](https://img.shields.io/badge/MQL4-Indicator-blue?style=flat-square)
![MT4](https://img.shields.io/badge/Platform-MetaTrader%204-informational?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Free](https://img.shields.io/badge/Price-Free-brightgreen?style=flat-square)
![Stars](https://img.shields.io/github/stars/ForexTradingTools/fxtt-forex-scanner?style=flat-square)

> A free, open-source MT4 multi-timeframe scanner that shows Price, Spread, ATR, Volume, RSI, Stochastic, ADX, and Pivot Points for all your currency pairs — at a glance, on a single chart.

![FxTT Forex Scanner on MT4](https://forex-trading-tools-wordpress.caprover.carlosoliveira.me/wp-content/uploads/2018/03/Fxtt-MP-Fx-Scanner.png)

---

## 📌 Overview

Analysing pairs one by one is slow and error-prone. The **FxTT Multi-purpose Forex Scanner** solves this by displaying a real-time dashboard directly on your MT4 chart, showing the most important technical metrics for every symbol in your Market Watch — all in one place.

Built and used by me [Carlos Oliveira](https://forextradingtools.eu) as part of my own live trading workflow, the scanner is designed to be **fast, readable, and fully customisable**.

**Product page & documentation:** [forextradingtools.eu/products/indicators/forex-scanner-free](https://forextradingtools.eu/products/indicators/forex-scanner-free/)

---

## ✨ Features

| Column | Description |
|--------|-------------|
| **Price** | Real-time Bid price for each symbol |
| **Spread** | Current spread in pips |
| **ATR %** | Current bar range as % of ATR — spot volatile pairs instantly |
| **Volume %** | Current bar volume vs. average — detect unusual activity |
| **RSI** | RSI value with overbought (green) / oversold (red) colouring |
| **Stochastic** | %K/%D stochastic with configurable overbought/oversold levels |
| **ADX** | Trend strength interpreted at levels 25, 50, and 75 |
| **Pivots** | Price position relative to the nearest daily pivot level |

Every column can be shown or hidden independently. All timeframes and periods are configurable.

---

## 🖥️ Platform Requirements

- **Platform:** MetaTrader 4 (MT4)
- **File type:** `.ex4` (compiled) / `.mq4` (source)
- **Tested on:** MT4 build 1380+

> ⚠️ This indicator is **MT4 only**. For MT5 versions of other free indicators, visit [forextradingtools.eu/shop](https://forextradingtools.eu/shop/).

---

## 🚀 Installation

1. Download `FxTT-Forex-Scanner.ex4` from the [Releases](../../releases) page  
   *(or compile `FxTT-Forex-Scanner.mq4` yourself in the MetaEditor)*
2. Open MT4 → **File → Open Data Folder**
3. Navigate to `MQL4/Indicators/`
4. Copy `FxTT-Forex-Scanner.ex4` into that folder
5. Restart MT4 (or right-click the Navigator panel → **Refresh**)
6. Find **FxTT-Forex-Scanner** under **Navigator → Indicators**
7. Drag it onto any chart — the scanner panel will appear

---

## ⚙️ Settings Reference

### Display

| Parameter | Default | Description |
|-----------|---------|-------------|
| `Update interval (secs)` | 5 | How often the scanner refreshes. Increase if you notice performance issues. |
| `Font Size` | 9 | Font size of the on-screen text |
| `Font Name` | Arial | Font family used in the panel |

### Columns — Show/Hide & Configure

Each column has a `Show [Column]` toggle (true/false) plus its own timeframe and period settings.

#### ATR
| Parameter | Default | Description |
|-----------|---------|-------------|
| `Show ATR` | true | Show/hide the ATR % column |
| `ATR Timeframe` | H1 | Timeframe for ATR calculation |
| `ATR Period` | 14 | Lookback period for ATR |

#### Volume
| Parameter | Default | Description |
|-----------|---------|-------------|
| `Show Volume` | true | Show/hide the Volume % column |
| `Volume Timeframe` | H1 | Timeframe for average volume calculation |
| `Volume Period` | 20 | Number of bars for average volume |

#### RSI
| Parameter | Default | Description |
|-----------|---------|-------------|
| `Show RSI` | true | Show/hide the RSI column |
| `RSI Timeframe` | H1 | Timeframe for RSI calculation |
| `RSI Period` | 14 | RSI lookback period |
| `RSI Upper Level` | 70 | Overbought threshold (shown in green) |
| `RSI Lower Level` | 30 | Oversold threshold (shown in red) |

#### Stochastic
| Parameter | Default | Description |
|-----------|---------|-------------|
| `Show Stochastic` | true | Show/hide the Stoch column |
| `Stoch Timeframe` | H1 | Timeframe for stochastic calculation |
| `%K period` | 5 | %K period |
| `%D period` | 3 | %D period |
| `Slowing` | 3 | Slowing parameter |
| `MA Method` | 0 (SMA) | Moving average method |
| `Price Field` | 0 (Low/High) | Price field used |
| `Stoch Upper Level` | 80 | Overbought threshold |
| `Stoch Lower Level` | 20 | Oversold threshold |

#### ADX
| Parameter | Default | Description |
|-----------|---------|-------------|
| `Show ADX` | true | Show/hide the ADX column |
| `ADX Timeframe` | H1 | Timeframe for ADX calculation |
| `ADX Period` | 14 | ADX lookback period |
| `ADX Applied Price` | 0 (Close) | Price used in calculation |

#### Pivots
| Parameter | Default | Description |
|-----------|---------|-------------|
| `Show Pivots` | true | Show/hide the Pivots column |

---

## 💡 How to Use It

1. **Filter for volatility** — Sort by ATR % to find the most active pairs right now
2. **Find momentum confluences** — Look for pairs where RSI + Stochastic agree (both overbought or both oversold)
3. **Confirm trend strength** — Use the ADX column to avoid trading choppy, low-ADX pairs
4. **Check pivot proximity** — Trade pairs where price is approaching a key pivot level
5. **Watch spreads** — Filter out pairs with unusually wide spreads before entering

> Tip: Run the scanner on a dedicated background chart (e.g. EURUSD M1) and keep it visible alongside your main trading charts.

---

## 🗂️ Repository Structure

```
fxtt-forex-scanner/
├── src/
│   └── FxTT-Forex-Scanner.mq4    # Full MQL4 source code
├── releases/
│   └── FxTT-Forex-Scanner.ex4    # Compiled MT4 binary (ready to install)
├── screenshots/
│   └── scanner-mt4.png            # Scanner running on MT4
└── README.md
```

---

## 📝 Changelog

### v1.0.0
- Initial public release
- Columns: Price, Spread, ATR, Volume, RSI, Stochastic, ADX, Pivots
- All columns independently configurable

---

## 🤝 Contributing

Contributions are welcome! If you find a bug or want to suggest an improvement:

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/my-improvement`)
3. Commit your changes (`git commit -m 'Add my improvement'`)
4. Push to the branch (`git push origin feature/my-improvement`)
5. Open a Pull Request

For major changes, please open an issue first to discuss what you'd like to change.

---

## ⭐ Reviews

> *"Great scanner, works flawlessly. Thank you again for sharing the code — it is written very well, easy to read and understand, self-explanatory and scalable."*  
> — Alexander

> *"Perfect scanner, the best of all."*  
> — Jedah Landicho

---

## 📄 License

This project is licensed under the **MIT License** — you are free to use, modify, and distribute this code, provided the original copyright notice is retained.


---

## 🔗 More Free Tools

All free indicators and EAs from Forex Trading Tools:

- 🔗 [Strategy Checklist – Free MT4 Indicator](https://forextradingtools.eu/products/indicators/strategy-checklist-free-indicator/)
- 🔗 [MTF Triple Moving Averages – Free MT4 Indicator](https://forextradingtools.eu/products/indicators/mtf-triple-moving-averages-free-indicator/)
- 🔗 [MTF Bollinger Bands – Free MT4 Indicator](https://forextradingtools.eu/products/indicators/mtf-bollinger-bands-indicator/)
- 🔗 [MTF Bollinger Bands MT5 – Free MT5 Indicator](https://forextradingtools.eu/products/indicators/mtf-bollinger-bands-mt5-indicator/)
- 🔗 [Pivot Points – Free MT5 Indicator](https://forextradingtools.eu/products/indicators/pivot-points-mt5-free/)

---

*Made with ❤️ by [Carlos Oliveira](https://forextradingtools.eu) | Forex Trading Tools*
