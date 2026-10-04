# Buy residential proxy: pay-per-GB or pay-per-IP, what each tier actually costs, and how to test before you commit

Most people searching for this end up on a pricing page showing something like "$0.018 per IP" or "$0.68 per GB" — and then discover that number belongs to the largest bulk tier on the page, not the package they're about to buy. The gap between the headline rate and the checkout total is where most residential proxy budgets go wrong.

So this is a buying guide, not a list of who claims to be cheapest. It covers the two billing models that every provider quotes (per IP and per GB), the checks worth doing before you pay, and 9Proxy's current published tiers as a concrete example — including the June 2026 price change that moved its IP packages up and left bandwidth rates alone.

## The two billing models behind every quote

Residential proxies are sold one of two ways, and the choice matters more than the brand name on the invoice.

**Pay per GB.** You buy a block of traffic — 5 GB, 100 GB, 1 TB — and generate as many rotating endpoints as you like. Every request that goes through the proxy deducts from that bucket. Requests themselves cost nothing; data does. This suits work where each request pulls very little: ad verification, geo-checks, price sampling, API polling, SERP spot checks, and anything that rotates IPs aggressively.

**Pay per IP.** You buy a number of residential IP addresses and bandwidth on them is unmetered. Scrape 100 pages or 10,000 through the same IP, the cost doesn't move. This suits sustained sessions, account-based tasks, long-running crawls, and anything where you can't predict the data volume in advance.

|  | Pay per GB | Pay per IP |
| --- | --- | --- |
| What you're buying | Traffic volume | IP addresses, unlimited data |
| Best for | High rotation, light requests | Sticky sessions, heavy transfers |
| Typical risk | Burning through the bucket early | Paying for IPs you barely use |
| Rotation | Automatic, per request or per sticky session | Manual or via an auto-rotation port |

A rough rule of thumb before you commit to either: a plain HTML fetch is measured in kilobytes, while a full page with images, fonts and scripts can run to a few megabytes. Multiply that by your page count per day and you'll know whether a 5 GB pack lasts a week or an hour. If your arithmetic lands anywhere near the boundary, buy the smaller package first and measure.

9Proxy sells both models and also bundles them together. You can 👉 [compare 9Proxy's current IP-based and GB-based packages](https://bit.ly/9-Proxy) while reading the rest — the tables below use its published rates.

Worth separating three product types that get mixed up in this conversation, because the price difference is large. Residential proxies route through IPs assigned by consumer ISPs to real home connections. ISP (often called static residential) proxies are hosted on servers but registered to ISP-owned ranges — faster, less diverse. Datacenter proxies are cheap and fast and get flagged far more often. If a seller advertises residential pricing at datacenter prices, check which pool you're actually getting.

## The pre-purchase checklist

No provider's own marketing page will tell you all of this, and every item below has cost someone money at some point.

**1. Trial availability.** 9Proxy's trial is limited and depends on current availability — you request it from support rather than clicking a free-tier button. Third-party reviews note that trial codes get issued during promotions, so availability varies by month. Ask before you buy a large package.

**2. Expiry rules.** This is the quiet budget killer. On 9Proxy's IP-based packages, unused IPs never expire. On GB-based packages, traffic is valid for 180 days, with enterprise tiers carrying unlimited validity. If your project is one intensive month followed by three quiet ones, that distinction decides which model is cheaper for you.

**3. Targeting depth.** Country, city, state and ISP-level targeting are all advertised, and the vendor's own product description also lists ZIP code. One independent comparison flags city-level targeting at 9Proxy as more limited than the mid-market providers — if your workflow depends on hitting a specific metro, verify it on a small package rather than assuming.

**4. Protocol support.** HTTP/HTTPS and SOCKS5. The SOCKS5 support matters if you're wiring proxies into anti-detect browsers, proxychains, or custom Python scripts, since it avoids protocol translation hacks.

**5. Session control.** Rotation on every request, sticky sessions that hold for a set window, or a mix. On the per-IP model there's no natural rotation at all — each IP stays live from a few hours up to roughly 24 hours — so rotation is handled through a dedicated auto-rotation port if you need it.

**6. Whether a client is required.** This is the most common surprise. 9Proxy's IP-based product authenticates through its desktop app (local port forwarding, with optional proxy authentication). The GB-based product works straight from the dashboard using username/password or an IP whitelist. If you're deploying on a headless server, that difference is decisive.

**7. What happens when an IP fails.** Third-party reviews cite a replacement window of about 60 seconds for failed proxies, plus a "Today List" feature that lets you reuse IPs at no extra cost. Both are worth confirming with support, since "failed" is the word that does the arguing.

**8. Payment methods.** Cards, bank cards, crypto (USDT, BTC, ETH, LTC, DOGE), Alipay, Apple Pay and Google Pay, plus a region-specific checkout option. If you need to pay from a corporate card or an invoice flow, check first.

> Buy the smallest package that covers your real target list, break it on your hardest target, and only then size up. A refund policy you never had to use is worth more than a discount you took on faith.

## What 9Proxy charges right now

On 1 June 2026, 9Proxy raised prices for the first time since launching — IP-based packages and bundles went up, GB-based packages did not move at all. Older reviews still quote the pre-June numbers ($20 for 100 IPs, $25/$150/$600 bundles), so treat anything published before mid-2026 as historical. The tiers below reflect the adjusted structure.

### IP-based packages (unlimited bandwidth)

| Package | Price per IP | Total | Buy |
| --- | --- | --- | --- |
| 100 IPs | $0.24 | $24 | [Order the 100 IP pack](https://bit.ly/9-Proxy) |
| 500 IPs | $0.144 | $72 | [Order the 500 IP pack](https://bit.ly/9-Proxy) |
| 1,000 IPs + 500 bonus | $0.084 | $126 | [Order the 1,500 IP pack](https://bit.ly/9-Proxy) |
| 2,500 IPs | $0.084 | $210 | [Order the 2,500 IP pack](https://bit.ly/9-Proxy) |
| 5,000 IPs | $0.072 | $360 | [Order the 5,000 IP pack](https://bit.ly/9-Proxy) |
| 15,000 IPs | $0.048 | $720 | [Order the 15,000 IP pack](https://bit.ly/9-Proxy) |
| 25,000 IPs | $0.035 | $863 | [Order the 25,000 IP pack](https://bit.ly/9-Proxy) |
| 50,000 IPs | $0.029 | $1,438 | [Order the 50,000 IP pack](https://bit.ly/9-Proxy) |
| 100,000 IPs (Business) | $0.023 | $2,300 | [Order the 100,000 IP pack](https://bit.ly/9-Proxy) |
| 200,000 IPs (Business) | $0.021 | $4,140 | [Order the 200,000 IP pack](https://bit.ly/9-Proxy) |
| 500,000 IPs (Business) | $0.018 | $8,625 | [Order the 500,000 IP pack](https://bit.ly/9-Proxy) |

Two things stand out. The 1,000-IP tier ships with 500 bonus IPs, which is why its effective rate sits level with the 2,500 tier rather than between the 500 and 2,500 rows. And the "$0.018 per IP" figure you'll see in ads belongs to the half-million-IP tier — at the 100-IP entry point you're paying $0.24 per IP, roughly 13 times more.

### GB-based packages

| Package | Price per GB | Total | Validity | Buy |
| --- | --- | --- | --- | --- |
| 5 GB | $3.00 | $15 | 180 days | [Order the 5 GB pack](https://bit.ly/9-Proxy) |
| 50 GB + 5 GB bonus | $2.10 | $105 | 180 days | [Order the 55 GB pack](https://bit.ly/9-Proxy) |
| 100 GB | $1.50 | $150 | 180 days | [Order the 100 GB pack](https://bit.ly/9-Proxy) |
| 200 GB | $1.00 | $200 | 180 days | [Order the 200 GB pack](https://bit.ly/9-Proxy) |
| 1,000 GB | $0.80 | $800 | 180 days | [Order the 1,000 GB pack](https://bit.ly/9-Proxy) |
| 2,000 GB | $0.75 | $1,500 | 180 days | [Order the 2,000 GB pack](https://bit.ly/9-Proxy) |
| 3,000 GB | $0.72 | $2,160 | No expiry | [Order the 3,000 GB pack](https://bit.ly/9-Proxy) |
| 6,000 GB | $0.70 | $4,200 | No expiry | [Order the 6,000 GB pack](https://bit.ly/9-Proxy) |
| 10,000 GB | $0.68 | Quoted at checkout | No expiry | [Order the 10,000 GB pack](https://bit.ly/9-Proxy) |

The 5 GB pack at $3.00/GB versus the 1,000 GB pack at $0.80/GB is the whole economics of this model in two rows. You are paying a steep convenience premium for the small tier — which is fine, if you treat it as a test rather than a production contract. Also note where the validity clock changes: from 3,000 GB upward, purchased traffic does not expire.

### Bundle packages

| Bundle | Contents | Price | Terms | Buy |
| --- | --- | --- | --- | --- |
| Starter | 100 IPs + 5 GB | $30 | IPs never expire; traffic valid 180 days | [Order the Starter bundle](https://bit.ly/9-Proxy) |
| Popular | 1,500 IPs + 50 GB | $180 | IPs never expire; traffic valid 180 days | [Order the Popular bundle](https://bit.ly/9-Proxy) |
| Pro | 5,000 IPs + 500 GB | $720 | IPs never expire; traffic valid 180 days | [Order the Pro bundle](https://bit.ly/9-Proxy) |

Bundles suit mixed workloads — some accounts that need a stable IP, some jobs that just need traffic — and you avoid running two separate purchases. The same caveat as above applies: bundles were part of the June 2026 adjustment, so older reviews listing $25, $150 and $600 describe the previous structure.

## Matching a package to the work you actually do

| Workload | Better model | Sensible starting point |
| --- | --- | --- |
| Testing whether a target even accepts the pool | GB | 5 GB |
| Ad verification and geo-checking across regions | GB | 100–200 GB |
| SERP tracking across multiple countries | GB | 200 GB–1,000 GB |
| Multi-account management with stable identities | IP | 500–2,500 IPs |
| Long crawls where bandwidth is unpredictable | IP | 1,000+500 IPs or 5,000 IPs |
| Reselling or running agency inventory | IP | 25,000 IPs and up |

The mistake worth avoiding is buying on volume rather than fit. Somebody running 3,000 SERP checks a month does not need 5,000 IPs; somebody keeping 800 accounts logged in will find bandwidth pricing useless no matter how cheap the per-GB rate looks. If your work is light on data but heavy on identity stability, the IP model wins. If it's the reverse, don't pay for addresses you'll never touch — 👉 [grab the 5 GB package](https://bit.ly/9-Proxy) and find out what your real daily consumption is before scaling.

## Discounts, payment methods, and the invite route

9Proxy runs its own affiliate program with commission up to 15% and a 5% discount for users who sign up through a partner invite — which is what the link in this article carries. There's also a documented bonus for selected payment methods: either 5% off or a 5% product bonus depending on the option you pick.

Seasonal coupon campaigns come and go, and they're worth understanding as a pattern rather than a fixed discount. During Lunar New Year 2026 the team issued a code giving 8% off regular IP and GB packages alongside limited large-volume tiers. In April 2026, a GB-focused promotion automatically issued a personal 9% coupon (format X9_…) to accounts after their first paid GB order of the month, usable on a later GB order and expiring 30 June 2026. Both campaigns have ended, and both carried the same restriction: coupons apply to GB orders only, are single-use, and cannot be stacked with other active codes.

Payment options cover major cards, bank cards, crypto (USDT, BTC, ETH, LTC, DOGE and others), Alipay, Apple Pay and Google Pay, plus a local payment route that surfaces region-specific methods at checkout. If you're paying with crypto, the bonus mentioned above is where the extra few percent usually comes from.

## What happens after you check out

The flow is short: create an account, pick a package, then choose how you want to reach the network. Four access routes exist, and which one you can use depends on the product you bought.

- **Desktop app (Proxy Program).** Required for IP-based packages. Routes traffic at the OS layer via local port forwarding, so applications without native proxy settings still work. It's the main reason the mobile-device story is weaker on per-IP plans — one app per machine, which is less convenient than a browser extension if you're juggling several devices.
- **Proxy2Web.** Zero-install, browser-based, standard user:pass authentication. The fastest way to sanity-check a package on a single target.
- **ProxyHub / ProxyHub Lite.** Mobile device management, with a desktop version for centrally switching and assigning mobile proxies.
- **Public API.** Programmatic session control and usage stats, for pipelines that need to provision endpoints from code.

Authentication differs by model: GB-based packages accept username/password or an IP whitelist, while IP-based packages go through the app. If your deployment is a Linux box with no GUI, plan around that before you pay.

## The trade-offs, stated plainly

The pool is over 20 million residential IPs across 90+ countries, which is respectable but a fraction of what Bright Data's 150M+ pool covers. One 2026 cost comparison places 9Proxy in the budget tier alongside DataImpulse at roughly $1–$1.30/GB, with Tier-1 success rates above 99% but noticeably weaker results on hard Tier-3 targets — the same comparison rates mid-market and premium providers higher on those. Another review measured about 99.5% success and roughly 0.6-second average response in its own tests, which is squarely in the usable range for scraping and monitoring but not a performance crown.

Other things worth knowing before purchase: IPs on the per-IP model live anywhere from a few hours to about 24 hours and don't rotate on their own. Per-IP packages depend on a desktop client. Free trials exist but are availability-gated and issued by support rather than through a self-serve button. On the plus side, unused IPs never expire, traffic on larger enterprise tiers carries no expiry at all, and there's a reseller program with wholesale rates if you're buying for clients rather than yourself.

## FAQ

**How much should a residential proxy cost per GB?**
Wide range, and it depends mostly on volume. 9Proxy runs from $3.00/GB on the 5 GB tier down to $0.68/GB at 10,000 GB. For context, Decodo's monthly plans start around $3.75/GB on a 3 GB plan and fall to about $2/GB at 1 TB, Rapidproxy advertises from $0.65/GB, and CatProxies starts at $2.50/GB. Anything advertised below roughly $0.60/GB deserves scrutiny about how the pool is sourced.

**Is per-IP or per-GB cheaper?**
Neither, in the abstract — it depends on the ratio between your page count and your session length. Heavy data on few identities makes per-IP almost always cheaper because the bandwidth is unmetered. Wide rotation with small requests makes per-GB cheaper because you're not paying for addresses that sit idle.

**Does 9Proxy offer a free trial?**
It has offered limited trials for new users depending on availability, distributed as codes by the support team. Third-party reviews consistently describe it as promo-dependent rather than a permanent free tier, so ask before assuming.

**Do I need the desktop app?**
Only for IP-based packages, where local port forwarding handles authentication. GB-based packages work directly from the dashboard with credentials or a whitelist, which is the better fit for servers and headless setups.

**Can I resell the IPs?**
Yes — there's a reseller program with wholesale pricing across both billing models and dedicated support. The vendor's own note to resellers is straightforward: buy inventory ahead of price changes to protect your margins.

If you're still deciding, the cheapest way to answer the question is to stop comparing rate cards and start testing targets. 👉 [Open a 9Proxy account, start with the smallest package that fits your workload](https://bit.ly/9-Proxy), and run your own URLs through it. A $15 test that tells you the success rate on your actual targets is worth more than a week of reading comparisons — including this one.
