# best japan vps: Tokyo plans from $6, how to pick between IIJ and SoftBank lines, and the refund rules worth checking before you pay

Searching for the best japan vps usually ends the same way: you find three articles about premium CN2 GIA plans, one about a limited-edition deal that sold out months ago, and no clear answer about what to actually buy. So let's start with the honest answer — "best" depends on two things: which network line your users are on, and how much you're willing to pay for it. On the budget end of that spectrum, GreenCloudVPS is one of the few low-cost providers that runs real Tokyo locations on both IIJ and SoftBank lines, plus a China-optimized CN Premium series with EPYC Milan hardware. This guide walks through their current Tokyo plans, the real routing differences between the two lines, and the fine print (spoiler: refunds) that most comparison posts skip.

> **Quick picks**
> - Most people testing the waters: the Budget KVM Sale Tokyo plans (4GB RAM / 35GB / 2 cores, 10Gbps port) — promo pricing shown at checkout, and a mid-October restock reported entry annual plans from **$25**.
> - China-facing projects that need low latency: **CN Premium Optimized Tokyo Plan 1** — 2 cores / 4GB / 40GB NVMe / 1TB at **$45/mo**.
> - 👉 [Check current Tokyo plan availability and pricing on GreenCloudVPS](https://greencloudvps.com/billing/aff.php?aff=6679)

## What "best japan vps" actually depends on

The best Japan VPS for you is decided by the network line first and the CPU specs second. Japan sits in a convenient spot — low latency to East Asia, reasonable routes to the US West Coast — but which route your traffic takes home depends entirely on the provider's upstream.

From there, the practical picture looks like this. Chinese mainland access needs premium lines: CN2 GIA for China Telecom, CU Premium for China Unicom, CMIN2 for China Mobile. General international use works fine on IIJ or SoftBank transit. And here's the catch most articles gloss over: Telecom, Unicom, and Mobile each prefer different upstreams, so there is no single "perfect for all three carriers" line — only lines that match *your* connection. Before buying anything, run a ping or MTR test against the provider's LookingGlass from your own network. Two minutes of testing beats ten review articles.

One more thing worth knowing up front: budget Japanese VPS plans are frequently out of stock. This is normal across the whole budget tier, and it shapes how you should shop — you're often waiting for a restock rather than browsing a catalog.

## GreenCloudVPS Japan plans: the full Tokyo lineup

GreenCloudVPS currently sells Tokyo servers on three separate product lines, and they serve very different needs. The company has been around since 2013, is a registered Delaware LLC, owns its own hardware, and took the #1 Top Provider and #1 Most Stable Provider spots in LowEndTalk's 2024 community awards — relevant context, because the budget VPS world is full of providers that vanish mid-year.

Here's the full Tokyo lineup as shown on the official store pages.

### CN Premium Optimized Tokyo (China-optimized)

This is the flagship for mainland China access: EPYC Milan CPUs, NVMe RAID-10 storage, and the official network annotation **CN2 GIA / CU Premium / CMIN2**. Prices below were verified during the September restock cycle; the shopping cart is always the source of truth since stock moves fast.

| Plan | CPU / RAM | Storage | Traffic / Port | Price | Buy |
| --- | --- | --- | --- | --- | --- |
| Mini | 1 core EPYC Milan / 2GB | 20GB NVMe | 500GB / 500Mbps | $25/mo | [ Get the Mini plan](https://greencloudvps.com/billing/aff.php?aff=6679) |
| Plan 1 | 2 cores / 4GB | 40GB NVMe | 1TB / 1Gbps | $45/mo | [ Get Plan 1 at $45/mo](https://greencloudvps.com/billing/aff.php?aff=6679) |
| Plan 2 | 4 cores / 8GB | 80GB NVMe | 2TB / 1.5Gbps | $85/mo | [ Get Plan 2](https://greencloudvps.com/billing/aff.php?aff=6679) |
| Plan 3 | 8 cores / 16GB | 160GB NVMe | 4TB / 2Gbps | $165/mo | [ Get Plan 3](https://greencloudvps.com/billing/aff.php?aff=6679) |
| Plan 4 | 8 cores / 32GB | 320GB NVMe | 8TB / 3Gbps | $320/mo | [ Get Plan 4](https://greencloudvps.com/billing/aff.php?aff=6679) |

All plans include 1 IPv4 + /64 IPv6, daily backups, and the VirtFusion control panel. Linux only. For most individual users, Plan 1 is the sensible pick — Mini's 500GB traffic and 500Mbps port are tight for anything beyond a test box, and the jump to Plan 2 doubles the price for capacity most single projects never touch.

### Budget KVM Sale Tokyo (IIJ and SoftBank lines)

This is the value line, and where GreenCloud differs from most budget competitors: same cheap promo pricing, but on Tokyo IIJ and Tokyo SoftBank transit instead of the usual US-only budget footprint.

| Plan | RAM / Storage | CPU | Traffic / Port | Line | Buy |
| --- | --- | --- | --- | --- | --- |
| BudgetKVM Tokyo -2 | 4GB / 35GB SSD RAID-10 | 2 cores (E5 v3/v4 on IIJ; Intel Platinum Gen 2 on SoftBank) | 750GB / 10Gbps | Tokyo IIJ | [ Check the IIJ plan](https://greencloudvps.com/billing/aff.php?aff=6679) |
| BudgetKVM Tokyo -3 | 8GB / 60GB SSD RAID-10 | 4 cores | 1500GB / 10Gbps | Tokyo IIJ | [ Check the IIJ -3 plan](https://greencloudvps.com/billing/aff.php?aff=6679) |
| BudgetKVM Tokyo SoftBank -2 | 4GB / 35GB SSD RAID-10 | 2 cores | 750GB / 10Gbps | Tokyo SoftBank | [ Check the SoftBank plan](https://greencloudvps.com/billing/aff.php?aff=6679) |

Note the traffic numbers: APAC locations get lower bandwidth quotas than the same plans in the US (750GB here versus 1.5TB stateside). Every plan includes 1 IPv4 + /64 IPv6, one free backup/snapshot, VirtFusion, and Linux only. These are restock-driven promo plans, so pricing appears at checkout rather than being permanently listed — a mid-October restock was reported with entry annual plans from $25 (1 core / 2GB / 25GB NVMe), and a $6/mo entry tier has been tracked on the Tokyo SoftBank Ryzen line at third-party VPS trackers. If the cart shows stock when you check, that's your window.

## SoftBank or IIJ? The differences most reviews skip

Pick IIJ if your IP staying clean matters; pick SoftBank if raw latency to China Telecom is the priority. That's the short version, and it comes from real measurement, not marketing pages.

A NodeSeek comparison published in late October 2026 tested GreenCloud's Tokyo nodes side by side. The SoftBank node returned **43ms to China Telecom, 94ms to Unicom, 70ms to Mobile** — genuinely good numbers. The IIJ node measured **104ms on both Telecom and Unicom, 75ms on Mobile**. On latency alone, SoftBank wins for Telecom users.

But latency is only half the story, and this is where the comparison gets useful:

- **IP reputation.** The IIJ node was clean with no blocking reports. The SoftBank node carried a higher IP-blocking risk, and GreenCloud charges **$2 per IP change** — not a fortune, but annoying if you're re-running proxies or need a fresh IP repeatedly.
- **IPv6.** On SoftBank, IPv6 routed through the US at 280–395ms, effectively unusable. On IIJ, IPv6 went direct and worked. If anything in your stack depends on IPv6, this alone decides it.
- **Service unblocking.** Both nodes unlocked ChatGPT, YouTube, and TikTok; the IIJ node additionally handled Prime Video. Netflix on both: originals only. Neither line is a full Japan-streaming box.

One more honest caveat from that same test round: the actual CPU delivered can differ from the advertised model (their units arrived as Xeon 8255C and Skylake parts rather than the headline silicon), and budget-tier plans are oversold to some degree. At $5–6/month pricing that's the trade you're making, but it's worth knowing.

## How GreenCloud compares with the usual Japan VPS picks

The cheapest sensible entry point is GreenCloud, and the premium entry point is somewhere else entirely — that's the practical market structure for Japan VPS.

The comparison most people end up making is with BandwagonHost (搬瓦工). Their Tokyo CN2 GIA offering (JPTYO_8, Equinix TY8) runs premium transit on all three Chinese carriers with a 1.2Gbps port, but starts at **$89.99/mo** — that's roughly twice GreenCloud's CN Premium Plan 1 ($45/mo) for the comparable positioning. Bandwagon's Osaka CN2 GIA plans are their better-value China-optimized option, and their limited editions (THE PLAN 2024 at $99/year, SAKURABOX at $79/year) are famous but chronically unavailable. Meanwhile 丽萨主机 (LisaHost) plays a different game: native Japanese IPs with strong local streaming unlocks, from about ¥88/month on their basic native-IP tier with a 48-hour refund window.

Where does that leave GreenCloud? Three honest observations:

1. **Price-to-line ratio.** Getting Tokyo CN2 GIA / CU Premium / CMIN2 at $25–45/mo undercuts every premium competitor's China-optimized Japan pricing by a wide margin.
2. **The budget tier is their real niche.** Most $5–6/mo providers simply don't offer Japan at all, or offer it with unremarkable transit. GreenCloud's IIJ and SoftBank Tokyo locations on the Budget KVM Sale line are unusual at that price.
3. **The trade-offs are structural.** Lower traffic quotas in APAC, restock-driven availability, no refunds on these plans, and the CPU-lottery effect on budget lines. Premium providers charge more partly to avoid exactly these annoyances.

If you need guaranteed premium hardware, formal SLAs, or full Japanese streaming unlocks, the premium competitors fit better. If you need a working Tokyo server at a sane price, GreenCloud's lineup is hard to beat.

## Things to check before you pay

Refunds are the big one, so here it is in plain terms: **the CN Premium Optimized plans and the Budget KVM Sale plans are all marked no refund / money back** on the official store pages. That's printed on every plan's cart entry, and the $168/3-year storage promo follows the same rule. There is no trial period to fall back on, so do your line testing *before* checkout — GreenCloud publishes test IPs for the Tokyo Premium line (IPv4 45.94.40.13, IPv6 2a12:a303:11a:c::a) precisely for this.

Second, mind the stock. At the time of the latest page snapshots, the CN Premium Tokyo plans showed zero available and the Budget KVM Sale had single-digit inventory in most locations. GreenCloud restocks in batches — the CN Premium line was reported back in stock as recently as late September, and multiple Tokyo locations restocked in mid-October. If something is sold out, checking back every few days is genuinely how people buy from this provider.

Third, verify the IP the moment your server is provisioned. The SoftBank line has documented blocking risk, and knowing whether your IP is clean on day one — while you still have options — beats discovering it a month in. And a small detail that matters to some buyers: the Kansas City variants of the Budget KVM Sale only include a /112 IPv6 prefix instead of /64, though that doesn't affect the Tokyo plans.

## FAQ

**What's the cheapest Japan VPS worth buying?**
Entry tiers on GreenCloud's Tokyo lines start around $6/mo when in stock, with annual promo plans reported from $25. Below that price point you're generally looking at unreliable oversold boxes or no Japan location at all.

**Which plan should I get for a website targeting Chinese mainland visitors?**
CN Premium Optimized Tokyo Plan 1 ($45/mo, 2 cores / 4GB / 40GB NVMe / 1TB) covers most small-to-medium projects. Test the route from your own connection first, since Telecom, Unicom, and Mobile users see different performance on the same line.

**Do GreenCloud's Tokyo plans support Windows?**
No. The CN Premium Optimized and Budget KVM Sale Tokyo plans are Linux only. GreenCloud sells separate Windows VPS lines starting at $8/mo, but those are US-based, not Japan.

**Can I get a refund if the line doesn't work for me?**
Not on these plans. The Tokyo CN Premium and Budget KVM Sale plans are all non-refundable, which is why pre-purchase route testing matters more here than with providers offering 48-hour or 30-day windows.

## Where this leaves you

Run your ping/MTR tests against the Tokyo test IPs tonight, then decide by scenario. If your visitors are in mainland China and you want premium transit without premium pricing, CN Premium Optimized Plan 1 at $45/mo is the clear pick. If you're hosting a personal project, a proxy node, or anything where a clean IP and working IPv6 matter more than squeezing out 60ms, the Budget KVM Tokyo IIJ plan is the better value. SoftBank makes sense mainly for Telecom users who've tested it and like what they see — and who accept the IP risk that comes with it. And if you need guaranteed hardware or a refund safety net above all else, the premium-priced competitors do that job; you'll pay two to four times as much for it.

One last practical tip: because these plans restock in waves and sell out fast, decide your pick in advance so you can move when inventory appears. 👉 [Check GreenCloudVPS's current Tokyo stock and prices](https://greencloudvps.com/billing/aff.php?aff=6679) — then test the line before you confirm the order, not after.
