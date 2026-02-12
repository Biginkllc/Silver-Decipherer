# Silver Decipherer – Functional Specification

## Core Concept

A mobile-first application that displays:
1. Shanghai silver prices converted into USD per troy ounce
2. US silver prices in USD per troy ounce
3. The absolute and percentage spread between them
4. Historical charts and alerts

All information is presented in clear English for non-professional users.

---

## Markets Covered

### Shanghai Silver
Acceptable reference instruments:
- Shanghai Gold Exchange (SGE) silver products (e.g. Ag(T+D), Ag99.99)
- Shanghai Futures Exchange (SHFE) silver futures (AG)

Prices are typically quoted in **RMB per kilogram** and must be normalized.

### United States Silver
- COMEX silver futures (USD per troy ounce)
- Alternative US benchmark if appropriate

---

## Normalization Logic

Shanghai prices must be converted as follows:

RMB/kg → USD/oz

Using:
- 1 troy ounce = 31.1034768 grams
- 1 kilogram = 32.1507466 troy ounces
- USD/CNY FX rate

---

## Core Features (High-End Target)

### Price Display
- Shanghai silver (USD/oz)
- US silver (USD/oz)
- Spread ($)
- Spread (%)

### Charts
- Intraday
- 7D / 30D / 1Y
- Spread history

### Alerts
- Absolute spread threshold
- Percentage premium threshold
- Volatility spikes

### Education Layer
- What each market is
- Why spreads exist
- Difference between spot, futures, and retail prices

---

## Audience

- Retail silver buyers
- Long-term precious metals holders
- Non-professional investors seeking transparency
