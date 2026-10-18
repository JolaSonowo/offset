# Offset

A guide to tax-loss harvesting, direct indexing and long-short (130/30) strategies, with a calculator that shows what each could be worth to you after taxes and fees.

**Live site:** https://jolasonowo.github.io/offset/

## What the calculator does

It simulates hundreds of possible markets week by week and compares three ways to invest the same money:

- a plain index fund, held untouched;
- direct indexing, which sells individual stocks that fall and buys a similar sector fund;
- a 130/30 long-short strategy, which harvests losses on both its long and short positions.

How it works:

- stocks move with the market, their sector and on their own, with occasional large shocks;
- the wash-sale rule is enforced: no buying back the same security within 30 days of a loss sale;
- every gain and loss is short- or long-term based on how long it was held, netted at year end the way the IRS does, with unused losses carried forward;
- tax saved is reinvested, and fees are charged weekly;
- the simulation runs in parallel across your device's processor cores.

You choose the amount, years, yearly additions, tax bracket, what your losses will cancel, and whether you sell at the end or hold for life.

## Running it

It's a single static file with no build step. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Limitations

The calculator leaves out dividends, trading costs, stock-picking skill and real-world limits on borrowing shares. Rates are based on general US federal tax rules for 2026, mapped from your bracket.

## Disclaimer

For education only. This is not tax, legal or investment advice. Simulated results are hypothetical and don't represent any real product, fund or company. Tickers in the illustrations are made up.
