# Awesome-Dunning-Failed-Payment-Recovery

# Top Dunning & Failed Payment Recovery Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Smart Retries, Failed Payment Recovery & Involuntary Churn Prevention*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Dunning & Failed Payment Recovery**. These tools help subscription businesses recover revenue lost to failed payments—covering intelligent retry scheduling, automated customer outreach, and card-update workflows that reduce involuntary churn.

**Examples** include Chargebee Revive, Stripe Smart Retries, Recurly Dunning, Churn Buster, ProfitWell Retain, Gravy Solutions, Recurso, and dunningkit (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted dunning automation, open-source billing recovery, and community-driven payment retry logic—ideal for organizations seeking data sovereignty and avoiding percentage-of-recovery fees. The open-source landscape is genuinely nascent: **Recurso** provides a complete billing engine with a built-in bandit-retry dunning system , and **dunningkit** offers a lightweight Stripe-specific recovery toolkit . Note that **most commercial dunning is deeply embedded in billing platforms** (Stripe, Chargebee, Recurly)—open-source alternatives require assembling billing infrastructure alongside recovery logic.

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Chargebee Revive & Smart Dunning](https://www.chargebee.com/)** | Two recovery modes inside Chargebee Billing: **Revive** (ML retry engine reading 200+ signals per failed payment) and **Smart Dunning** (rules-based, up to 12 retries on soft declines, holds hard declines for card update). Covers cards, wallets, direct debit, offline, and one-time payments. **Not available if billing runs elsewhere** . | Flow plan: **$0 + 0.80%** of monthly invoicing, or **$99 + 0.65%**; Smart Dunning included. Enterprise custom . | Smart Dunning included with Chargebee Billing; no separate dunning trial |
| **[Stripe Smart Retries](https://stripe.com/billing)** | **Free, built-in retry engine** that optimizes retry timing using ML across the Stripe network. Combined with **Adaptive Acceptance** (recovers false declines at authorization), Stripe reports **55–57% average recovery** and ~9% revenue uplift vs. fixed schedules. Sends one email per failed payment; no multi-step sequences; no retries after hard declines until new payment method added . | **Free** with Stripe Billing (0.5–0.8% of billing volume) | **Free forever**: Smart Retries and Adaptive Acceptance included with Stripe Billing at no extra cost |
| **[Recurly Dunning Management](https://recurly.com/)** | Dunning included on **all Recurly plans**. Default campaign for every site; **Professional and Elite plans** allow up to **50 targeted campaigns** for different plans/segments. Separate cycles for declined automatic payments, past-due manual invoices, and post-trial failures. Account Updater runs indefinitely on overdue accounts. Dunning settings are versioned with campaign analytics . | Starter: **$249/month + 0.9%** of billing volume (first $40K included); All-Access: **<1%** of billing volume (annual, $1M minimum) . | Dunning included on all plans; 1 campaign on Starter, multiple on Professional/Elite |
| **[Churn Buster](https://churnbuster.io/)** | **Flat-fee dunning and cancel flows** priced by MRR tier, **month-to-month with no contract**. Positioned to break even at ~1% recovery improvement—everything beyond is yours. Includes analytics, segmentation, A/B tests, and retention team guidance. Free "Measure" tier includes MCP for Claude/ChatGPT queries . | Dunning or Cancel Flows separately: **$269/mo** (MRR-based); Both: **$430/mo** . | **Free (Measure)**: recovery analytics and baseline, MCP access; no credit card |
| **[ProfitWell Retain (Paddle)](https://www.profitwell.com/retain)** | **Pay-for-performance** recovery service. Charges only on **incremental recoveries above your existing baseline**—not on revenue Stripe already recovered. Guarantees recovered customers stay ≥2 months (minimum 100% ROI; typically 2,000%+). Fully managed by Paddle's retention team; white-labeled and PCI compliant . | Varies based on revenue recovered above baseline | No free tier; performance-based pricing |
| **[Gravy Solutions](https://gravysolutions.io/)** | **Human-powered payment recovery**—real agents call customers to update payment methods. **Revenue share: 10–25% of recovered revenue**. Best for high-value enterprise customers ($500–$5,000/mo subscriptions) where personal outreach outperforms automated emails. 1–2 week onboarding; no cancel flows or churn prediction . | **10–25%** of recovered revenue | No free tier; pay only on recovery |
| **[Zuora Collections](https://www.zuora.com/)** | Enterprise collections and dunning within Zuora's subscription platform. **Pricing on request**; no public plans or free tier listed . | Quote-only (enterprise contract) | No free tier; demo via sales |
| **[Chaser](https://www.chaserhq.com/)** | Credit control and receivables automation with dunning workflows. SMS and phone call add-ons available. Pricing based on credit packages with volume tiers . | Quote-only (credit-based) | No free tier; demo via sales |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Recurso](https://github.com/recurso-dev/recurso)** | [![Stars](https://img.shields.io/github/stars/recurso-dev/recurso?style=social&color=white)](https://github.com/recurso-dev/recurso/stargazers) | **The most complete open-source billing engine with built-in dunning.** MIT licensed, Go + PostgreSQL. Features: **bandit-retry engine** (adaptive retry strategy) + **Collections operator layer**, built-in double-entry ledger with ASC 606 revenue recognition, 8 usage aggregations, 7 charge models, India GST/EU VAT/US sales tax, and self-serve importers from Stripe and Chargebee (preview → commit, no re-billing). **Runs on your infrastructure**—full data ownership. One-command demo: `make demo` . **Best for teams wanting a self-hosted Chargebee/Stripe Billing alternative with dunning included.** |
| **[dunningkit](https://pypi.org/project/dunningkit/)** | — | **Lightweight open-source toolkit for analyzing and recovering failed Stripe payments.** Python package (no dependencies). Focused specifically on Stripe payment recovery—likely provides utilities for identifying failed charges and triggering recovery workflows. **Best for Stripe-only teams wanting a lightweight recovery helper.** |

**Frameworks for building custom systems**: Choose **Recurso** for a complete self-hosted billing engine with dunning, ledger, and tax compliance built in —or **dunningkit** for a lightweight Stripe-specific recovery helper. **If you're already on Stripe, the highest-ROI move is enabling Smart Retries and Adaptive Acceptance first**—they're free and recover 55–57% on average —then evaluate paid tools only for the gap above that baseline.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Dunning platforms handle payment credentials and customer billing data; enforce PCI DSS compliance, tokenized card storage, and secure retry logic. **Retry logic that stacks (rather than replaces) can damage authorization rates**—ensure competing retry engines are disabled .
- **Pricing models vary dramatically and incentive alignment matters.** Chargebee and Recurly bundle dunning into billing platforms (percentage of volume) . **Stripe Smart Retries is genuinely free** and should be your baseline—recovering 55–57% of failures . **Churn Buster charges flat MRR-based fees** ($269–$430/mo) with no contract . **Gravy Solutions takes 10–25% of recovered revenue**—appropriate only for high-value enterprise subscriptions where human calls justify the cut . **ProfitWell Retain charges only on incremental lift above baseline**—the most aligned model for existing Stripe users . **Open-source dunning is nascent**: Recurso is the only complete billing engine with dunning built in , and dunningkit is Stripe-specific . Validate recovery attribution (baseline vs. incremental) and retry conflict policies before committing.

---

**Made for subscription finance teams, revenue operations, and developers building billing recovery infrastructure.**  
Let's make dunning and failed payment recovery more open, transparent, and revenue-aligned.
