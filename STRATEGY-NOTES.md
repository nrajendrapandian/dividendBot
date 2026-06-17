# SPYI vs. SCHD: growth phase vs. income phase

## Total return vs. yield

Portfolio growth during accumulation is driven by total return (price appreciation + dividends, reinvested), not by current yield. Current yield only converts a finished portfolio into cash flow.

| | SCHD (illustrative) | SPYI (illustrative) |
|---|---|---|
| Current yield | 3.5% | 11–12% |
| NAV/price trend | Grows ~6–7%/yr | Roughly flat to slightly declining |
| Total return | ~10–11%/yr | ~8–9%/yr |

SPYI's covered-call overlay sells away upside in exchange for option premium distributed as yield. In rising markets the calls get exercised and price appreciation is forfeited — that forgone appreciation shows up as distributed income instead, so total return ends up similar to or lower than the underlying index, despite the higher headline yield.

## Tax drag compounds the gap

In a taxable account:
- SCHD's price appreciation is unrealized — untaxed until sold, compounding tax-deferred.
- SPYI's distributions are paid out annually and partially taxed immediately. Even with favorable Section 1256 treatment (60% LTCG / 40% ordinary), a portion is taxed every year, reducing what gets reinvested.

Illustrative example, $20K over 10 years, no further contributions, taxable account:

| | SCHD | SPYI |
|---|---|---|
| Pre-tax ending balance | ~$54K | ~$43K |
| Annual tax drag | Minimal (mostly deferred) | ~0.8–1.2%/yr |
| After-tax ending balance | ~$52K | ~$38K |

**Account placement note:** held inside a Roth IRA, SPYI's tax-drag disadvantage disappears entirely (no annual tax on distributions). The capped-upside effect on total return still applies, but the gap narrows substantially.

## Capital required for $5,000/month by yield

Income-phase math: how big does the portfolio need to be to produce $60K/year ($5K/month) at a given yield?

| Yield | Portfolio needed |
|---|---|
| 3.5% (SCHD) | $1,710,000 |
| 7% (blended) | $857,000 |
| 12% (SPYI) | $500,000 |

Higher yield requires far less capital to hit the same income target — this is the case *for* SPYI, but only once accumulation is largely done.

## The two-phase model

1. **Growth phase** (now → ~2 years before goal date): weight toward SCHD/DGRO/VIG. Total return compounds the pile; tax drag from distributions is minimal since dividends are mostly qualified and most growth is unrealized.
2. **Income phase** (final 1–2 years before goal, and beyond): rotate into SPYI/JEPI-style high-yield funds. At this point the priority shifts from growing the pile to converting it into cash flow — yield now matters more than total return.

Rule of thumb: SPYI is the wrong tool for building the pile and the right tool for milking it once built.

## Revised growth-phase allocation (no SPYI)

| ETF | Allocation | Role |
|---|---|---|
| SCHD | 50% | Core compounder |
| DGRO | 25% | Quality growth screen |
| VIG | 15% | Dividend Aristocrat stability |
| JEPI | 10% | Light income/volatility stabilizer (less upside-capped than SPYI) |

JEPI is kept at a small weight rather than zero — it dampens portfolio swings during downturns without sacrificing as much upside as SPYI.

## Website implementation

The "Goal planner" tab on the dashboard (`index.html`) models this rotation: a toggle ("Shift allocation from growth funds to income funds in the final N years") drives a stacked bar chart showing the growth/income allocation split shifting from 70/30 to 20/80 as the goal date approaches.
