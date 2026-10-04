# dedicated proxies: what makes an IP actually yours, what it costs per IP, and where 9Proxy's pay-per-IP pool fits

"Dedicated proxy" sounds like a product category. It isn't one. There's no dedicated protocol, no shared standard, no certification. The word describes a commercial arrangement: the exit IP carries your traffic and nobody else's.

That changes the question worth asking. Not "which dedicated proxy should I buy," but "what am I buying the exclusivity for?" A seller panel you log into every morning, an anti-detect browser running forty profiles, and a scraping job pulling two million pages are three different problems. Only some of them are really about owning addresses.

## What actually makes a proxy dedicated

Shared and dedicated proxies run through exactly the same machinery. Your client opens a connection to a proxy, authenticates — usually username and password, sometimes by whitelisting your own IP — and the proxy opens a second connection to the target site from its own address. The target sees the proxy's IP, not yours, and hands the response back.

The only thing that changes is who else is doing that through the same address at the same time.

On a shared or rotating gateway, the address you get may have been used by a stranger ten seconds earlier. On a dedicated one, that address's history belongs to you. If you've ever seen a proxy get blocked on a site you'd never touched, that's the mechanism — you inherited someone else's reputation.

Providers also sell the identical product under the name **private proxy**. One buyer, one address. Read the two phrases as synonyms when you compare offers.

## The three shapes you'll be quoted for

"Where the IP comes from" matters more than "is it dedicated." A dedicated address that a target recognizes as a datacenter range will get flagged regardless of exclusivity.

| Type | Where the IP comes from | What it's normally used for |
| --- | --- | --- |
| Dedicated datacenter | Remote servers, not registered to any internet provider | High-throughput scraping where speed beats stealth |
| Dedicated ISP / static residential | Server-hosted, but registered under a real ISP | Logged-in accounts, long sessions, targets that reject datacenter ranges |
| Dedicated mobile | Mobile carrier networks | The hardest targets, and mobile ad verification — billed the highest |

One naming trap worth knowing: the phrase "dedicated residential" usually isn't a rotating residential IP that only you get. It almost always refers to a static ISP address — hosted in a datacenter for stability, registered under an ISP so it looks residential. That combination is why people pay more for it than for a plain datacenter IP.

## What exclusivity is worth

- **Reputation starts clean.** You begin with an address that hasn't been used for someone else's spam run, and it stays as clean as your own habits keep it.
- **Sessions hold together.** Login state, carts, and multi-step forms survive when the IP doesn't move underneath them.
- **Bandwidth is yours.** Nobody else's traffic is competing for the same pipe.
- **You control rotation.** Static addresses stay put. The moment you want a new one, that's your call, not a scheduler's.

> When a shared address gets blocked, a stranger probably did it. When a dedicated address gets blocked, your own request pattern did — and the fix shows up in your own logs.

## What it costs you

Dedicated addresses are priced per address, and that's the whole problem at scale. Ten IPs is comfortable. A thousand is a line item somebody asks about. Per-IP pricing is the reason rotating pools exist.

The other trade-offs are less obvious. Your pool is only as big as you bought, so there's no spare address waiting when one gets rate-limited — pacing and concurrency suddenly matter in a way they don't on a rotating network. Some targets block datacenter ranges outright, which makes a dedicated datacenter IP expensive and useless for that particular job. And few providers make managing hundreds of individual endpoints pleasant.

## The distinction that trips up most buyers: dedicated is not permanent

This is the part where people waste money.

- **Static** means the same IP for weeks or months. It's what you want for an account you'll log into from the same "location" every day.
- **Session-stable** means the IP is yours for the length of a session — a few hours, sometimes a day — and then it's gone.

Both are dedicated in the sense that nobody else is routing through your connection while you hold it. Only one of them keeps the same address next month. Sellers rarely lead with the difference, and buyers frequently assume the wrong one.

## Where 9Proxy fits in this picture

9Proxy sells residential proxies. That's the whole catalogue: no datacenter range, no mobile tier. What it offers instead of a static-address product is a balance-based way to buy residential IPs by the unit — which lands surprisingly close to what a lot of "dedicated proxy" buyers are actually trying to do.

The network is advertised at 20M+ residential IPs across 90+ countries with 8,000+ servers. Treat pool and uptime figures as vendor claims; the success rate you get depends on your targets, not on the headline number.

## The IP-based model: the closest thing here to a dedicated setup

This is the product to look at first if exclusivity is your reason for searching. Its mechanics, per 9Proxy's own documentation:

- You pay per IP, not per gigabyte. Bandwidth is unlimited while an IP is active.
- One forwarded IP equals one use, deducted from your balance. Unused IPs never expire, so buying a larger package is a bet on future projects, not on a subscription.
- IPs live naturally from a few hours up to roughly 24 hours, depending on the address.
- There's no automatic rotation. If you want addresses to change on a schedule, you turn on the Auto Rotation Proxy and set the interval per port.
- Authentication runs through the 9Proxy desktop app via local port forwarding, with optional proxy authentication. It supports HTTP and SOCKS5.

Set against the static-vs-session distinction above: what you're buying is a large supply of residential addresses you hold for the length of a working session, with the cost predictable in advance because traffic doesn't count.

One thing to verify with support before you commit, if guaranteed single-tenant addresses are a hard requirement for your project: 9Proxy documents the balance mechanics precisely, but it doesn't publish a promise that a given residential IP will never be assigned to another customer. If your use case depends on that guarantee in writing, ask.

## The GB-based model: traffic, not addresses

The second product flips the logic. You buy gigabytes, get unlimited endpoints, and traffic rotates across the pool — either per request or held sticky for a configured session. Validity is 180 days on standard packages and unlimited on the enterprise tiers, which suits bursty work where a monthly expiry would waste what you paid for.

Authentication here is username/password or an IP whitelist, straight from the dashboard. No desktop app needed.

If you're trying to buy a dedicated IP, this is not the product. Rotating traffic isn't an address you own, however long the sticky session runs.

## Bundles: both, for mixed workloads

For teams running a stable-IP job and a rotation-heavy job side by side, the bundle packages combine both resources at a lower total than buying each separately. The bundled traffic keeps the 180-day validity.

## Every 9Proxy plan, with current pricing

9Proxy adjusted **IP-based and bundle pricing on 1 June 2026**, the first change in its history; GB-based pricing was left alone. The figures below reflect that adjustment. All prices are one-time, in US dollars — this is a balance model, not a monthly subscription.

### IP-based residential packages (unlimited bandwidth per IP)

| Package | Price (USD) | Effective rate | Validity | Purchase |
| --- | --- | --- | --- | --- |
| 100 IPs | $24 | $0.24 per IP | IPs never expire until used | Start with the 100 IP package |
| 500 IPs | $72 | $0.144 per IP | IPs never expire until used | Buy the 500 IP package |
| 1,000 IPs + 500 bonus | $126 | $0.084 per IP | IPs never expire until used | Get the 1,500-IP package |
| 2,500 IPs | $210 | $0.084 per IP | IPs never expire until used | Grab the 2,500 IP package |
| 5,000 IPs | $360 | $0.072 per IP | IPs never expire until used | Compare the 5,000 IP package |
| 15,000 IPs | $720 | $0.048 per IP | IPs never expire until used | See the 15,000 IP package |
| 25,000 IPs | $863 | $0.035 per IP | IPs never expire until used | Check the 25,000 IP package |
| 50,000 IPs | $1,438 | $0.029 per IP | IPs never expire until used | View the 50,000 IP package |
| 100,000 IPs | $2,300 | $0.023 per IP | IPs never expire until used | Explore the 100,000 IP business package |
| 200,000 IPs | $4,140 | $0.021 per IP | IPs never expire until used | See the 200,000 IP business package |
| 500,000 IPs | $8,625 | $0.018 per IP | IPs never expire until used | Review the 500,000 IP business package |

### GB-based residential packages

| Package | Price (USD) | Effective rate | Validity | Purchase |
| --- | --- | --- | --- | --- |
| 5 GB | $15 | $3.00 per GB | 180 days | Buy the 5 GB package |
| 50 GB + 5 GB bonus | $105 | $2.10 per GB | 180 days | Get the 50 GB package |
| 100 GB | $150 | $1.50 per GB | 180 days | Grab the 100 GB package |
| 200 GB | $200 | $1.00 per GB | 180 days | Compare the 200 GB package |
| 1,000 GB | $800 | $0.80 per GB | 180 days | See the 1,000 GB package |
| 2,000 GB | $1,500 | $0.75 per GB | 180 days | Check the 2,000 GB package |
| 3,000 GB (Enterprise) | $2,160 | $0.72 per GB | Unlimited | View the 3,000 GB enterprise package |
| 6,000 GB (Enterprise) | $4,200 | $0.70 per GB | Unlimited | Explore the 6,000 GB enterprise package |
| 10,000 GB (Enterprise) | $6,800 | $0.68 per GB | Unlimited | See the 10,000 GB enterprise package |

### Bundle packages (IPs + traffic)

| Package | Price (USD) | What's included | Validity | Purchase |
| --- | --- | --- | --- | --- |
| Starter | $30 | 100 IPs + 5 GB | IPs never expire; traffic 180 days | Try the Starter bundle |
| Popular | $180 | 1,500 IPs + 50 GB | IPs never expire; traffic 180 days | Pick the Popular bundle |
| Pro | $720 | 5,000 IPs + 500 GB | IPs never expire; traffic 180 days | Compare the Pro bundle |

## The features that stop you wasting what you bought

Anyone who has run residential IPs at volume knows the real cost isn't the price per address — it's the addresses that die before they do any work. Three of 9Proxy's features target exactly that:

- **60-second replacement.** If a forwarded IP fails in its first minute, you can swap it free. Most providers count a dead proxy as consumed.
- **The Today List.** IPs you've forwarded within the last 24 hours can be reused at no cost while they're still online. On short jobs and test runs, that reclaims a noticeable share of consumption.
- **Auto Refresh.** Offline IPs get detected and swapped without you babysitting a proxy list.

Also worth knowing: HTTP, HTTPS, and SOCKS5 are all supported, so scrape stacks built on Puppeteer, Playwright, or Scrapy don't need workarounds. Geo-targeting goes to country level generally, with state, city, and ISP-level targeting reported on the GB-based plans — useful for local SEO checks and ad verification where the result genuinely changes by city. Payment options cover cards, crypto (USDT, BTC, ETH, LTC, DOGE and others), bank cards, Alipay, Apple Pay, and Google Pay. Support runs 24/7 through Telegram, email, and tickets.

Free trials exist but aren't automatic, according to independent reviewer reports — they depend on current promotions and you'll likely need to request a code from support.

## Matching the plan to the job

**Anti-detect browsers and multi-account work.** One residential IP per browser profile is the standard setup, and the IP-based packages are built for it. 100 IPs at $24 covers ten profiles with replacements to spare; 500 IPs at $72 is where per-profile costs get comfortable. 9Proxy's residential IPs are widely reported to work with Dolphin Anty and AdsPower.

**SERP tracking and ad verification from a fixed location.** You want the same vantage point repeatedly, so you're holding IPs rather than rotating. Buy the IP pool, enable Auto Rotation only if you actually want the address to change.

**Scraping at volume with unpredictable page weights.** Unlimited bandwidth per IP is the selling point here — a JavaScript-heavy crawl of 100,000 pages costs the same whether the pages weigh 2 MB or 5 MB. Bigger IP packs push the effective rate down toward $0.018–$0.03 per IP.

**Bursty, low-bandwidth automation.** API polling, geo-checks, light monitoring. GB-based plans are cheaper here because you'd be paying for IPs you barely use.

**Mixed workloads or agency work with per-client budgets.** Bundles keep one project's IP supply and traffic in a single package.

## Where 9Proxy is the wrong choice

It's worth being blunt about this, because the search term you arrived with may not match what they sell.

If you need a **permanent static IP** — the same address for months, pinned to a long-lived account — 9Proxy's residential IPs expire naturally within about a day by design. Look at a static ISP or dedicated datacenter product instead.

If you need **datacenter addresses** for raw speed, they don't sell them. The catalogue is residential, plus the GB and bundle variants of the same network.

If you want a **browser extension** with nothing installed, the IP-based model requires the 9Proxy desktop app for port forwarding. iTWire's review flagged that as the main inconvenience, particularly when you want to work across several devices.

And if your target is a **streaming service**, note that the same review reported detection issues on services like Netflix. Residential proxies aimed at scraping and account work don't reliably unlock streaming catalogues, and 9Proxy isn't positioning itself there.

## What to check with any provider before you pay

1. Confirm whether the address you're buying is static or session-based, and how long a session actually lasts in practice.
2. Ask whether the IP is single-tenant for the life of your subscription — in writing, if the answer matters to your account security.
3. Check the bandwidth model. Per-IP with unlimited traffic and per-GB metering produce very different bills at the same workload.
4. Find out what happens to a dead proxy. Free replacement inside a window, or a consumed resource?
5. Check whether unused balance expires. A 180-day clock and a never-expiring balance are not the same purchase.
6. Match the location coverage to your actual targets, not to the country count in the marketing copy.

## Questions people ask before buying

**Are dedicated proxies the same as private proxies?** Yes. One renter, one address. The words are interchangeable across providers.

**Do I need a dedicated IP to scrape a website?** Usually not. Rotating pools exist precisely because a static address gets rate-limited by request volume. You want dedicated IPs when identity continuity matters — logged-in sessions, account isolation, verifying the same ad placement daily.

**How much should a dedicated proxy cost?** Dedicated ISP addresses typically start around $1.25 per IP and rise from there; dedicated datacenter is cheaper per address. 9Proxy's per-IP residential balance sits far below that at volume — $0.084 per IP at 1,500 IPs — because you're buying session-stable residential addresses rather than permanent ones. That's a different product at a different price, and choosing between them comes down to whether the same IP needs to exist next month.

**Can several accounts share one dedicated proxy?** They can, but it defeats the purpose. Mixing profiles on one address recreates exactly the shared-IP risk you paid to avoid. One address per account is the point.

**Is there a way to test before buying a package?** 9Proxy offers limited free trials for new users depending on availability, typically arranged through support. Ask before assuming it's automatic.

If the job in front of you is a stack of browser profiles, a scraping run, or a rank-tracking setup that needs a stable vantage point per project, the per-IP model is the piece worth pricing out — 👉 [check the current 9Proxy packages and pricing](https://bit.ly/9-Proxy) and do the arithmetic against how many addresses you'd actually burn in a month. That number, not the per-IP headline rate, is what your bill will look like.
