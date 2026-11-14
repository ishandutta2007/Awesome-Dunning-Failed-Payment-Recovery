# Awesome Dunning & Failed Payment Recovery [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated directory of software platforms, SaaS tools, and open-source GitHub repositories for **dunning management**, **failed payment recovery**, **smart retries**, and **involuntary churn prevention**.

Failed credit card charges, expired tokens, and bank declines cause up to 40% of customer churn in subscription businesses. This guide evaluates both commercial SaaS solutions and self-hosted open-source dunning engines designed to automate payment retries, coordinate customer outreach, update payment details, and recover lost Monthly Recurring Revenue (MRR).

---

## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS & Hosted Platforms](#saas--hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [Key Features & Evaluation Criteria](#key-features--evaluation-criteria)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## Sector Overview & Market Dynamics

The global **Subscription and Billing Management** market is valued at approximately **$7.5B to $8.8B in 2025–2026** (growing at a ~14–16% CAGR), with the dedicated **dunning and payment recovery software** segment representing a **$1.4B+** market addressing an estimated $100B+ in annual global revenue leakage from failed recurring payments. The sector exhibits a **moderately fragmented, bifurcated structure**: top-layer infrastructure is heavily concentrated around global billing/payment gatekeepers (Stripe, Chargebee, Zuora, Paddle), while specialized dunning, AI retry agents, and cancellation-flow optimization remain highly fragmented among specialized SaaS providers and an emerging generation of self-hosted open-source billing engines.

---

## SaaS & Hosted Platforms

The table below details commercial platforms for automated dunning and involuntary churn prevention, sorted in descending order of company size (valuation / estimated market capitalization / revenue).

| Product | Company Size (Valuation / Revenue) | Description | Pricing (Starting Tier) | Free Tier / Trial Limits |
| :--- | :--- | :--- | :--- | :--- |
| **[Stripe Smart Retries](https://stripe.com/billing)** | **$70B+ Valuation** (~$16B ARR) | Machine-learning-driven retry engine optimizing retry timings across billions of global network transactions. Combined with Adaptive Acceptance, recovers an estimated 55–57% of soft card declines without manual intervention. | **$0 / Included** with Stripe Billing (standard Stripe Billing starts at **0.5% – 0.8%** of transaction volume) | **Free forever plan**: Smart Retries and Adaptive Acceptance are permanently included at zero extra surcharge with Stripe Billing. |
| **[Chargebee Revive & Smart Dunning](https://www.chargebee.com/)** | **$3.5B Valuation** (~$150M+ ARR) | Multi-mode recovery inside Chargebee Billing: Revive (ML engine analyzing 200+ transaction signals) and Smart Dunning (rules-based schedules, up to 12 configurable retries on soft declines). | Starter plan starts at **$0/mo** (first $250k cumulative billing); Flow plan starts at **$99/mo + 0.65%** of monthly invoicing. | **14-day free trial** with full sandbox access; plus a permanent **Starter tier ($0/mo)** for early-stage startups processing up to $250k cumulative revenue. |
| **[Zuora Collections](https://www.zuora.com/)** | **$1.7B Acquisition** (~$440M ARR) | Enterprise-grade accounts receivable, automated collections workflows, and multi-tier dunning engine designed for complex multi-entity quote-to-cash enterprises. | Contract tiers start at approximately **$75,000/year** ($6,250/mo) for growth editions plus implementation fees. | **No free tier or public self-serve trial**; private demo, proof-of-concept (PoC), and custom enterprise trial environments provided via sales. |
| **[ProfitWell Retain (Paddle)](https://www.profitwell.com/retain)** | **$1.4B Valuation** (~$90M+ ARR) | Pure pay-for-performance dunning service. Charges exclusively on incremental churn recovered above your existing organic/Stripe baseline with a guaranteed customer lifetime retention threshold. | Performance-based fee (percentage of verified incremental recovered revenue) or standalone custom tiers starting around **$500/mo**. | **No free trial for Retain**; however, companion **ProfitWell Metrics** is 100% free forever for real-time subscription churn and MRR analytics. |
| **[Recurly Dunning Management](https://recurly.com/)** | **~$50M+ ARR** (Accel-KKR Portfolio) | Subscription billing platform featuring automated multi-campaign dunning, account updaters, and predictive repair algorithms configured across distinct subscriber cohorts. | Starter plan starts at **$249/mo + 0.9%** of billing volume (includes up to $40K/month processing). | **90-day free trial** for new Starter accounts; access to full sandbox environment. |
| **[Chaser](https://www.chaserhq.com/)** | **~$4M ARR** (~$6M Total Funding) | Credit-control and accounts-receivable automation suite delivering multi-channel dunning sequences across automated email reminders, SMS, customer payment portals, and debtor tracking. | Compact plan starts at **$259/mo** (or £199/mo billed monthly; £179/mo billed annually) for businesses with turnover under £4M. | **10-day free trial** with access to core reminder templates, automated workflows, and test environment; no credit card required. |
| **[Gravy Solutions](https://gravysolutions.io/)** | **~$7M ARR** (~$5M Total Funding) | Tech-enabled, human-powered recovery service pairing retention agents with digital outreach to contact customers personally for high-value subscription tiers. | Managed services start at a baseline of **$997/mo** flat fee or **10% – 25%** revenue share of successfully recovered receivables. | **No free trial** due to human-agent onboarding and bespoke setup; complimentary historical payment data audit and consultation demo available. |
| **[Churn Buster](https://churnbuster.io/)** | **Bootstrapped** (~$1M ARR) | Specialized passive churn toolkit providing automated dunning sequences, card-update landing pages, real-time retry coordination, and Model Context Protocol (MCP) data access. | Dunning or Cancellation Flows individually start at **$269/mo** (MRR-scaled, month-to-month); bundled suite starts at **$430/mo**. | **Free forever plan (Measure Tier)**: includes payment recovery audit, baseline analytics, and MCP queries; 14-day trial available on paid plans without contract. |

---

## Open-Source GitHub Projects

Self-hosted dunning engines and open-source subscription infrastructure provide total control over payment credentials, avoid revenue-cut percentage fees, and enable customized smart-retry algorithms.

The repositories below are sorted in descending order of GitHub star count:

| Project | Stars | Language / Stack | License | Description |
| :--- | :---: | :--- | :--- | :--- |
| **[Lago](https://github.com/getlago/lago)** | [![Stars](https://img.shields.io/github/stars/getlago/lago?style=social&color=white)](https://github.com/getlago/lago/stargazers) | Go, Ruby, TypeScript | AGPL-3.0 | API-first, open-source metering and billing infrastructure. Features automated overdue invoice management, customer-level dunning policies, programmatic retry endpoints (`/invoices/:id/retry_payment`), secure customer payment-update URLs, and webhook hooks for building automated recovery workflows. |
| **[Kill Bill](https://github.com/killbill/killbill)** | [![Stars](https://img.shields.io/github/stars/killbill/killbill?style=social&color=white)](https://github.com/killbill/killbill/stargazers) | Java | Apache-2.0 | The open-source subscription billing and payments engine standard. Features a modular payment control architecture with configurable overdue rules, multistep dunning matrices, automated state transitions, and pluggable retry processors for payment gateways. |
| **[BillaBear](https://github.com/billabear/billabear)** | [![Stars](https://img.shields.io/github/stars/billabear/billabear?style=social&color=white)](https://github.com/billabear/billabear/stargazers) | PHP (Symfony) | Functional Source (FSL) | Self-hosted billing, checkout, and subscription management application built on Stripe. Includes automated failed payment retries, customizable customer email notification cadences, dunning state machines, and invoice recovery dashboards. |
| **[UniBee](https://github.com/UniBee-Billing/unibee)** | [![Stars](https://img.shields.io/github/stars/UniBee-Billing/unibee?style=social&color=white)](https://github.com/UniBee-Billing/unibee/stargazers) | Go, Vue | Apache-2.0 | Complete open-source subscription billing platform designed for SaaS. Includes automatic payment retry intervals, dunning campaigns, integrated admin/customer self-service portals for payment method updates, and analytics for recovered transactions. |
| **[Recurso](https://github.com/recurso-dev/recurso)** | [![Stars](https://img.shields.io/github/stars/recurso-dev/recurso?style=social&color=white)](https://github.com/recurso-dev/recurso/stargazers) | Go, PostgreSQL | MIT | Modern open-source billing engine built with a multi-armed bandit retry algorithm for intelligent dunning optimization. Incorporates a Collections operator layer, double-entry ledger compliant with ASC 606, tax rules, and zero-rebilling migration tools from Stripe and Chargebee. |
| **[GetPaidHQ](https://github.com/getpaidhqco/getpaidhq)** | [![Stars](https://img.shields.io/github/stars/getpaidhqco/getpaidhq?style=social&color=white)](https://github.com/getpaidhqco/getpaidhq/stargazers) | Go, React, PostgreSQL | MIT | Lightweight developer-first subscription and usage billing system. Features adaptive retry intervals tailored to gateway decline reason codes, pre-dunning card expiration alerts, and hosted customer payment update links. |
| **[ERPNext Dunning](https://github.com/alyf-de/erpnext_dunning)** | [![Stars](https://img.shields.io/github/stars/alyf-de/erpnext_dunning?style=social&color=white)](https://github.com/alyf-de/erpnext_dunning/stargazers) | Python (Frappe) | GPL-3.0 | Automated dunning level configuration, reminder letter generation (*Mahnungen*), and overdue receivables tracking for Frappe/ERPNext systems. |
| **[OpenLup](https://github.com/openlup/openlup)** | [![Stars](https://img.shields.io/github/stars/openlup/openlup?style=social&color=white)](https://github.com/openlup/openlup/stargazers) | TypeScript | MIT | Open-source TypeScript subscription and dunning packages designed for physical recurring commerce, scheduled renewals, and self-hosted cardholder payment-update interfaces. |
| **[Billing for Laravel](https://github.com/pushery/billing-for-laravel)** | [![Stars](https://img.shields.io/github/stars/pushery/billing-for-laravel?style=social&color=white)](https://github.com/pushery/billing-for-laravel/stargazers) | PHP (Laravel) | MIT | Modular Laravel billing toolkit with out-of-the-box support for subscription dunning sequences, failed payment webhooks, retry management, and customer-facing payment update components. |

---

## Key Features & Evaluation Criteria

When selecting a dunning and payment recovery solution, evaluate platforms against these operational requirements:

1. **Smart Retry Scheduling (ML vs. Rule-Based)**:
   - Evaluates decline codes (e.g., `insufficient_funds`, `do_not_honor`, `expired_card`).
   - Adapts retry schedules dynamically to cardholder payday patterns, bank processing windows, and local acquiring bank behavior rather than static daily retries.
2. **Account Updater Integrations**:
   - Automated real-time card updater connectivity (Visa VAU, Mastercard ABU, American Express) to silently refresh expired or re-issued cards without bothering customers.
3. **Frictionless Customer Update Pages**:
   - Passwordless, secure, one-click payment method update landing pages accessible directly from SMS, email, or in-app modals.
4. **Retry Conflict Prevention**:
   - Avoiding dual-engine retry collisions (e.g., when Stripe Smart Retries and an external tool retry the same charge concurrently, triggering fraud flags or network decline penalties).
5. **Incentive Alignment & Attribution**:
   - Distinguishing between organic/baseline recovery (payments that would have succeeded on a basic 2nd attempt) versus true incremental lift generated by the tool.

---

## How to Contribute

We welcome community contributions to keep this ecosystem accurate and up-to-date!

1. Fork the repository.
2. Add your SaaS product or open-source tool following the existing tabular format:
   - For **SaaS platforms**: include product name, link, company size (valuation/revenue), concise description, specific starting tier pricing, and exact free tier/trial limits.
   - For **Open-Source projects**: include repository link, stargazers social badge, language/stack, license, and technical summary.
3. Keep entries strictly factual and free of promotional hyperbole.
4. Open a Pull Request with a brief explanation of the change.

---

## Disclaimer

- This list is community-curated for informational and architectural evaluation purposes; it does not constitute financial, legal, or payment processing advice.
- Payment retry operations interact directly with card networks and payment processor compliance rules. Always comply with PCI DSS standards and monitor gateway decline limits to prevent merchant account penalties.

---

**Star this repository on GitHub** if you find it helpful for your billing architecture, finance engineering, or subscription operations!
