# ScraperAPI Pay As You Go: What Is It, Which Plans Include It, How Much Does It Actually Cost, and Is It Worth It? (Full Plan Breakdown + Credit Multiplier Guide)

If you've ever Googled "ScraperAPI pay as you go" in a mild panic at 11pm because your credits just hit zero mid-project and your scraper's sitting there doing nothing — this article is for you.

The concept sounds simple. Pay for what you use, stop when you stop. But the reality of ScraperAPI's pay-as-you-go system is a little more nuanced than the marketing suggests. It's not available on every plan. The "extra credits" rate isn't prominently advertised. And if you don't understand the credit multiplier system underneath all of it, even PAYG can turn into a surprise at the end of the month.

So let's walk through the whole thing — what ScraperAPI's pay-as-you-go feature actually is, which plans include it, how credits work (with the multiplier math most reviews skip), and what every plan looks like side by side.

---

## What "Pay As You Go" Actually Means on ScraperAPI

Here's the thing that trips people up: on ScraperAPI, "pay as you go" is **not** a standalone pricing model you can choose instead of a subscription. It's an **overage mechanism** — a safety net that kicks in when you exhaust your monthly credit allowance before your billing cycle resets.

When your plan's credits run out, a pop-up in your dashboard gives you the option to continue scraping at a fixed, predictable per-credit rate rather than being hard-stopped. You can also set a monthly spending cap on this overage so it never goes above a number you're comfortable with. The service will not exceed that cap unless you manually change it.

This is a meaningful feature if you run unpredictable or bursty scraping workloads — a sudden spike in product monitoring, a one-off research crawl, a client project that grew larger than expected. Instead of getting cut off and scrambling to upgrade a plan, you just keep going and pay for what you used.

But here's the critical catch: **pay as you go is only available on the Scaling plan and above.** If you're on Hobby, Startup, or Business, and you burn through your credits before the month ends, you're stopped. Your options are upgrading to the next tier or contacting support about a custom arrangement. There's no PAYG overflow.

> **PAYG availability summary:**
> - **Free, Hobby, Startup**: ❌ No PAYG overage
> - **Business**: ❌ No PAYG overage (upgrade required)
> - **Scaling, Professional, Advanced, Enterprise**: ✅ PAYG overage available at a fixed per-credit rate

👉 [Start your free 7-day trial on ScraperAPI — no credit card required](https://www.scraperapi.com/?fp_ref=coupons)

---

## The Credit System: The Part Every Review Skips

Before you can evaluate whether PAYG is right for you — or whether any plan is right for you — you need to understand how credits actually get consumed. Because the headline credit number on each plan (100,000, 1,000,000, etc.) is almost never the real number of pages you'll scrape.

Every API request burns credits, but not the same number. The cost depends on two things: the domain you're scraping, and the parameters you pass.

**Domain-based credit costs (automatic — you don't choose these):**

| Domain / Site Type | Credits Per Request |
|---|---|
| Standard HTML pages (blogs, news, docs) | 1 |
| E-commerce sites (Amazon, Walmart, eBay) | 5 |
| Search engines (Google, Bing and subdomains) | 25 |
| Social media (LinkedIn) | 30 |

**Parameter-based credit costs (optional — you choose these):**

| Parameter | Extra Credits |
|---|---|
| `render=true` (JavaScript rendering) | +10 |
| `premium=true` (premium proxy pool) | +10 |
| `screenshot=true` | +10 |
| `ultra_premium=true` | +30 |
| `premium=true` + `render=true` combined | +25 total (not +20) |
| `ultra_premium=true` + `render=true` combined | +75 total (not +40) |

That last row deserves a second look. Combining ultra-premium proxies with JavaScript rendering doesn't cost the sum of the parts — it costs **75 extra credits per request**, nearly double the individual add-on total. This non-linear stacking is documented in ScraperAPI's docs, but it's buried, and it's the main reason people watch credits disappear faster than expected.

To put it in concrete terms: the Hobby plan's 100,000 credits translates to very different actual page counts depending on your target:

| What You're Scraping | Credits Per Request | Actual Pages from 100K Credits |
|---|---|---|
| Simple HTML blog / news | 1 | ~100,000 pages |
| Amazon product page (no render) | 5 | ~20,000 pages |
| Amazon + JavaScript rendering | 15 | ~6,667 pages |
| Google SERP | 25 | ~4,000 pages |
| Google SERP + JS render | 35 | ~2,857 pages |
| Protected site (ultra-premium + JS) | 75 | ~1,333 pages |

One more important rule: **credits do not roll over**. Unused credits reset at the end of each billing cycle. So buying more credits than you'll realistically use in a month means paying for capacity you'll never get back.

---

## Full ScraperAPI Plan Comparison Table

Here's every plan currently available, including all configurations, prices, and whether PAYG overage is included:

| Plan | Monthly Price | Annual Price (per mo) | API Credits/Month | Concurrent Threads | Geotargeting | PAYG Overage | Link |
|---|---|---|---|---|---|---|---|
| **Free** | $0 | — | 1,000 | 5 | ❌ | ❌ |  [Start Free](https://www.scraperapi.com/?fp_ref=coupons) |
| **Hobby** | $49 | $44.10 | 100,000 | 20 | US & EU only | ❌ |  [Get Hobby Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Startup** | $149 | $134.10 | 1,000,000 | 50 | US & EU only | ❌ |  [Get Startup Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Business** | $299 | $269.10 | 3,000,000 | 100 | Global (50+ countries) | ❌ |  [Get Business Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Scaling** | $475 | $427.50 | 5,000,000 | 200 | Global | ✅ |  [Get Scaling Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Professional** | $975 | $877.50 | 10,500,000 | 300 | Global | ✅ |  [Get Professional Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Advanced** | $1,975 | $1,777.50 | 21,500,000 | 500 | Global | ✅ |  [Get Advanced Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Enterprise** | Custom | Custom | 22,000,000+ | 500+ | Global | ✅ |  [Contact Sales for Enterprise](https://www.scraperapi.com/?fp_ref=coupons) |

**What every paid plan includes regardless of tier:** JS rendering, premium proxies, JSON auto-parsing, rotating proxy pool, custom headers, CAPTCHA and anti-bot bypass, custom sessions, automatic retries, unlimited bandwidth, 99.9% uptime SLA.

**What higher tiers add:** Global geotargeting (from Business), unlimited analytics history (from Business), PAYG overage option (from Scaling), higher concurrent thread limits throughout.

---

## So Which Plan Is Right for You?

Let's be practical about this. The numbers above only matter in the context of what you're actually scraping.

**The Hobby plan ($49/month)** makes sense if you're building something for yourself — a personal price tracker, a side project, testing an idea. 100,000 credits covers a lot of ground for basic HTML pages. Just understand that the moment Amazon or Google enters the picture, those credits shrink fast.

**The Startup plan ($149/month)** is where most small-scale production users land. A million credits per month with 50 concurrent threads is a meaningful step up. Still capped at US/EU geotargeting, but that covers the majority of use cases for developers running early-stage products or small agency workloads.

**The Business plan ($299/month)** is the first tier that unlocks global geotargeting — if you need to route requests through proxies in specific countries outside the US and EU, this is your floor. The 3 million credit allowance and 100 concurrent threads also push you into comfortably handling larger jobs.

**The Scaling plan ($475/month)** is where pay-as-you-go overage becomes available. This is the plan to pick if your workload is variable — sometimes you're within budget, sometimes you blow past it, and you'd rather pay a bit extra for the overflow than get cut off at a critical moment. It's also the most commonly labeled "best value" tier on the pricing page.

**Professional ($975/month) and Advanced ($1,975/month)** are for teams running data pipelines at scale — e-commerce monitoring across thousands of SKUs, SERP tracking for hundreds of keywords, market research crawls that run around the clock. At this scale the PAYG overage plus priority support matters.

**Enterprise** is custom everything — pricing, credits, concurrency, SLA. If you're processing 22 million+ requests per month, you're not choosing a plan from a dropdown anyway.

---

## Pay As You Go vs. Upgrading: The Real Math

Here's a scenario that comes up a lot: you're on the Startup plan ($149/month, 1,000,000 credits) and you're consistently hitting 80-90% of your credit limit with occasional months where you go over. Should you upgrade to Business for $299? Or would PAYG overage serve you better — except you can't get PAYG on Startup, so the question is really whether to jump straight to Scaling for $475.

The honest answer is: run the math for your specific usage.

On the **Business plan** at $299/month, you're paying $0.0001 per credit (3 million credits for $299). If you're regularly using 1.2–1.5 million credits a month, Business is probably overkill — you'd be paying for capacity you won't use, and unused credits don't roll over.

On the **Scaling plan** at $475/month, you get 5 million credits plus PAYG overflow. If your typical usage is 1.2–1.5 million credits but occasionally spikes to 2–3 million, the PAYG option lets you handle that spike without pre-buying a higher plan tier. The PAYG rate on Scaling is a fixed per-credit rate that ScraperAPI discloses in the billing section of your dashboard when you activate the feature.

The spend-cap feature is your friend here. Set a monthly PAYG cap equal to roughly what you'd pay to upgrade to the next plan, and you'll never get surprised.

👉 [Compare all ScraperAPI plans and start free](https://www.scraperapi.com/?fp_ref=coupons)

---

## What ScraperAPI Is Actually Good At (And Where It Struggles)

If you're evaluating whether ScraperAPI is the right tool before committing to any plan, here's the honest read based on independent benchmarks and real user feedback.

**Where ScraperAPI genuinely shines:**

ScraperAPI is well-regarded for e-commerce and real estate scraping. Independent testing puts its success rate at around 98% on Amazon, nearly 100% on Zillow, and strong numbers across Walmart and Etsy. The structured data endpoints for Amazon, Google, Walmart, eBay, and Redfin return parsed JSON directly — no HTML parsing required — which saves real development time. For teams doing product monitoring, SERP tracking, or real estate data collection, this is a legitimate differentiator.

The setup process is also genuinely simple. You're essentially replacing a direct URL call with a ScraperAPI-wrapped version of the same request. For developers who already have a scraping workflow, the integration is typically done in under an hour.

**Where it falls short:**

Social media is a hard no — Instagram, Twitter/X, and Booking.com all show 0% success rates in benchmarks. Sites requiring login are explicitly off-limits by ScraperAPI's terms of service. And the performance gap between easy targets (Amazon, standard HTML) and harder targets (rotating bot detection, some travel sites) is significant.

One complaint that shows up consistently in user reviews: the credit math isn't intuitive until you've been burned by it once. A business that was quoted a rate based on 60 million credits later discovered a 5× multiplier had applied to all their Amazon requests — an 80% reduction in effective capacity they didn't see coming. This isn't a bug, it's documented behavior, but it's the kind of thing you want to understand before your scraping bill lands.

> **User sentiment summary:** ScraperAPI sits at 4.4/5 on G2, 4.6/5 on Capterra, and 4.5/5 on Trustpilot. Ease of use scores consistently at 4.9/5. The most common complaints are around pricing transparency and variable performance on harder targets.

---

## Practical Tips for Staying on Budget

Whether you're on PAYG-eligible plans or not, a few habits will save you a lot of grief:

**Test your real credit cost before you commit.** Use the 7-day free trial (5,000 credits, no card required) to run actual requests against your target sites — not toy examples. Watch the dashboard to see how many credits each request actually burns. Then multiply by your expected monthly volume to find your real plan fit.

**Disable rendering and premium proxies unless you need them.** ScraperAPI doesn't auto-enable these, but domain multipliers (Amazon = 5×, Google = 25×) are automatic. Know which sites you're scraping and factor those base costs into your plan math.

**Set a PAYG spending cap the day you activate it.** The cap is set to unlimited by default, which means without a cap, overage can run freely. Set a hard monthly limit equal to roughly one plan tier upgrade cost as a starting point.

**Check the dashboard regularly in your first month.** There are no proactive alerts when credits are running low — no email, no SMS. Until you develop intuition for your burn rate, manual checks prevent surprises.

**Use structured data endpoints for supported sites.** Amazon and Google structured endpoints return clean JSON at 5× and 25× credit costs respectively — the same base cost as scraping those domains yourself, but with no parsing code to write or maintain.

---

## Is ScraperAPI's Pay As You Go Worth It?

If your scraping volume is predictable and you stay comfortably within a plan tier every month, PAYG overage is mostly a backup you'll never use — which is fine. That's what backup features are for.

If your volume is genuinely variable — project-based work, agency scraping, research crawls that vary by month — then being on the Scaling plan or above and having PAYG as an overflow safety net is a meaningful operational improvement over being hard-stopped mid-job.

The Scaling plan at $475/month isn't cheap, but it's the entry point for the most useful operational flexibility. You get 5 million credits, 200 concurrent threads, global geotargeting, and the ability to keep scraping when you go over — all with a cap so the bill never runs away from you.

If you're not sure whether your use case justifies Scaling, the rational path is: start the free trial, test your real per-request costs, project monthly volume, and compare the result against the plan table above. ScraperAPI's 7-day no-questions-asked refund policy also means you're not stuck if you pick the wrong tier in the first month.

👉 [Start your free ScraperAPI trial — 5,000 credits, no card needed](https://www.scraperapi.com/?fp_ref=coupons)

---

## Frequently Asked Questions

**Is ScraperAPI pay as you go available on all plans?**

No. PAYG overage is only available on the Scaling ($475/month), Professional ($975/month), Advanced ($1,975/month), and Enterprise (custom) plans. On Hobby, Startup, and Business, exhausting your credits means being cut off until the next billing cycle.

**How much does ScraperAPI's pay-as-you-go overage cost per credit?**

ScraperAPI describes the PAYG rate as a "fixed, predictable rate" per credit but doesn't publish a universal per-credit overage price prominently. The exact rate varies by plan tier and is disclosed in the billing section of your dashboard when you activate PAYG. Activating the spend cap at the same time prevents any surprise billing.

**Can I set a spending limit on pay-as-you-go usage?**

Yes. The dashboard includes a monthly cap setting for PAYG. Your service will not exceed the cap unless you change the setting. This is a spending limit, not a pre-charge.

**Do ScraperAPI credits roll over if I don't use them all?**

No. Unused credits reset at the end of each billing cycle, regardless of plan. There's no credit carry-forward on any tier.

**Is there a free plan or trial?**

Yes. ScraperAPI offers a permanent free tier with 1,000 credits/month and 5 concurrent connections — no card required. New sign-ups also get a 7-day trial with 5,000 credits to test at a larger scale before committing to any paid plan.

**What's the cheapest plan with global geotargeting?**

The Business plan at $299/month is the lowest tier with global (50+ country) geotargeting. Hobby and Startup are limited to US and EU proxy locations only.

👉 [See all current ScraperAPI plans and start for free](https://www.scraperapi.com/?fp_ref=coupons)
