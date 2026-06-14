# Fidelity Investments GraphQL Schema

## Overview

Fidelity Investments is one of the largest financial services companies in the world, providing investment management, retirement planning, brokerage, and wealth management services. This conceptual GraphQL schema models the core domain entities and relationships that underpin Fidelity's platform, including brokerage accounts, retirement accounts, portfolio holdings, market data, trading, and customer management.

Fidelity does not operate a public developer portal. Partner integrations are delivered through curated marketplace relationships and through Fidelity Institutional / Wealthscape for registered investment advisors. This schema is a conceptual representation based on publicly documented capabilities, product offerings, and standard financial services domain models.

## Schema Source

Conceptual — derived from Fidelity's public product documentation, Fidelity Institutional / Wealthscape advisor platform, NetBenefits retirement platform, Active Trader Pro capabilities, and standard brokerage/financial services domain models.

## Key Domain Areas

### Account Management
Models the full spectrum of Fidelity account types including individual taxable brokerage accounts, joint accounts, trust accounts, IRAs (Traditional, Roth, SEP, SIMPLE), employer-sponsored plans (401k, 403b, 457b), 529 college savings plans, HSAs, and CDs. Each account type carries its own tax treatment rules, contribution limits, and distribution rules.

### Portfolio and Positions
Tracks holdings across all asset classes supported by Fidelity: equities (stocks, ETFs), fixed income (bonds, CDs, Treasuries), mutual funds (including Fidelity's own ZERO expense-ratio funds), options contracts, annuities, and alternative investments available through Fidelity's platform.

### Trading and Orders
Covers the full order lifecycle from placement through execution and settlement. Supports market, limit, stop, stop-limit, and trailing stop orders. Models multi-leg options strategies and extended-hours trading. Order status flows from pending through partial fills to complete execution or cancellation.

### Market Data
Provides real-time and delayed quotes, OHLCV historical data, options chains with Greeks, dividend and split histories, earnings calendars, and analyst ratings. Fidelity's Active Trader Pro platform surfaces institutional-grade market data.

### Research and Analysis
Models Fidelity's proprietary equity research, third-party analyst ratings, portfolio analysis tools, and screener capabilities. Includes the Fidelity Equity Summary Score and sector/industry classification.

### Documents and Reporting
Covers account statements, trade confirmations, tax documents (1099-DIV, 1099-B, 1099-INT, 1099-R, 5498), cost basis reports, and year-end summaries. NetBenefits surfaces plan-specific statements and benefit summaries.

### Alerts and Watchlists
Models price alerts, portfolio alerts, research alerts, and custom watchlists used across Fidelity's web, mobile, and Active Trader Pro platforms.

### Customer and Profile
Captures customer identity, contact information, beneficiary designations, trusted contacts, and account linkage across the household.

## Types Summary

| Category | Types |
|---|---|
| Accounts | Account, IndividualAccount, JointAccount, TrustAccount, IRA, RothIRA, TraditionalIRA, SEPAccount, 401kAccount, 403bAccount, 457bAccount, 529Account, HSAAccount, BrokerageAccount, NetBenefitsAccount |
| Balances | AccountBalance, Cash, Margin, Securities |
| Holdings | Positions, Position, Holding, Investment |
| Assets | Stock, Bond, ETF, MutualFund, OptionContract, CD, Annuity |
| Trading | TradeOrder, OrderStatus, MarketOrder, LimitOrder, StopOrder, StopLimitOrder, Quote, Trade, Symbol |
| Market Data | Price, HistoricalData, OHLCV, OptionChain, OptionLeg, GreeksData, OpenInterest |
| Corporate Actions | Dividend, DividendHistory, SplitHistory, Earning |
| Documents | Statement, ConfirmationSlip, TaxDocument, Form1099, CostBasisReport |
| Analysis | PortfolioAnalysis, PortfolioHolding, PortfolioPerformance |
| Research | MarketData, NewsArticle, Research, Analyst, Rating |
| Notifications | Alert, WatchList, WatchListItem |
| Customer | Customer, Profile, Beneficiary, Contact, Household |
| Auth | Auth, Token, Webhook |

## References

- Fidelity Investments: https://www.fidelity.com/
- Fidelity Institutional / Wealthscape: https://institutional.fidelity.com/
- NetBenefits: https://nb.fidelity.com/
- Fidelity Marketplace: https://www.fidelity.com/go/marketplace/overview
- Fidelity GitHub: https://github.com/fidelity
- Active Trader Pro: https://www.fidelity.com/trading/active-trader-pro
