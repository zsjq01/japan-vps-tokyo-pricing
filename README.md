# Cheap Japan VPS: What ¥630 a Month Buys in Tokyo, How Much RAM You Actually Need, and the IP, Route and Renewal Details That Change the Bill

A 1 GB Tokyo VPS starts at **¥630 a month** on the Japanese market, and a 2 GB box at **¥695**, according to a comparison of 242 Japan-hosted plans updated in November 2026. Those figures are in yen and already include 10% consumption tax plus a paid IPv4 address, which is why they look higher than the dollar headlines you see elsewhere.

Below the floor, things get murkier. Sub-$3 offers are usually IPv6-only, promo-priced for the first term, or sized so small that a single Docker image fills the disk. This article covers JustHost's Tokyo ladder, how to size a plan without overbuying, the three costs that appear only after signup, and how the well-known budget names line up on the same specs.

> **Quick pick:** for one small site, a WireGuard endpoint or a chat bot, a **1 GB / 1 core Tokyo plan at roughly $3–4 a month** is enough. For a game server or a multi-user API, go to **4 GB / 2 cores at about $9 a month** on the same ladder. Prices come from an independent review of JustHost's Tokyo TYO2 range, so confirm the live figure and the billing currency on the order page. 👉 [See JustHost's current Tokyo plans and prices](https://justhost.asia/?ref=196392)

## JustHost Tokyo plans and prices

The table below reproduces the Tokyo TYO2 range as recorded by an independent review in April 2026. All plans are KVM with NVMe storage and advertised unlimited traffic on a fair-share basis, and port speed scales with the plan from 300 Mbps to 1 Gbps.

| Plan (RAM / vCPU) | NVMe | Port | Approx. price/month | Order |
| --- | --- | --- | --- | --- |
| 1 GB / 1 core | 20 GB | 300 Mbps | ~$3.23 | [ Order](https://justhost.asia/?ref=196392) |
| 2 GB / 1 core | 30 GB | 300 Mbps | ~$4.61 | [ Order](https://justhost.asia/?ref=196392) |
| 2 GB / 2 cores | 40 GB | 400 Mbps | ~$5.99 | [ Order](https://justhost.asia/?ref=196392) |
| 4 GB / 2 cores | 80 GB | 500 Mbps | ~$8.96 | [ Order](https://justhost.asia/?ref=196392) |
| 4 GB / 4 cores | 120 GB | 750 Mbps | ~$12.20 | [ Order](https://justhost.asia/?ref=196392) |
| 8 GB / 4 cores | 200 GB | 750 Mbps | ~$18.63 | [ Order](https://justhost.asia/?ref=196392) |
| 8 GB / 5 cores | 300 GB | 750 Mbps | ~$22.08 | [ Order](https://justhost.asia/?ref=196392) |
| 12 GB / 6 cores | 400 GB | 750 Mbps | ~$30.36 | [ Order](https://justhost.asia/?ref=196392) |
| 16 GB / 8 cores | 500 GB | 750 Mbps | ~$40.71 | [ Order](https://justhost.asia/?ref=196392) |
| 24 GB / 8 cores | 600 GB | 750 Mbps | ~$54.51 | [ Order](https://justhost.asia/?ref=196392) |
| 32 GB / 8 cores | 700 GB | 750 Mbps | ~$82.11 | [ Order](https://justhost.asia/?ref=196392) |
| 32 GB / 12 cores | 1000 GB | 1 Gbps | ~$109.71 | [ Order](https://justhost.asia/?ref=196392) |

Two things to verify before you pay. **Billing currency:** one review of this brand quotes entry plans in yuan, another in US dollars, so the number on the checkout page is the only one that counts. **Price basis:** check whether the figure shown is a true monthly rate or a rate that assumes prepaying 12 months.

Where the ladder is worth climbing: the jump from 1 GB / 1 core at ~$3.23 to 2 GB / 2 cores at ~$5.99 doubles the cores, doubles the disk and lifts the port to 400 Mbps for about $2.76 more. That is the best value step in the whole list. Higher up, paying $22.08 instead of $18.63 buys the same 8 GB of RAM and a bigger disk rather than more compute, and the two 32 GB plans differ mainly in storage and port speed. Buy cores when your CPU graph is pinned, not before.

The platform itself has a few features that matter for people who move around: one-click data-centre switching and one-click IP switching from the client area, free IPv6, and payment via card, PayPal, Alipay, UnionPay and crypto. A third-party profile traces the brand back to 2006 with 77 locations. 👉 [Check the plan list and available payment methods](https://justhost.asia/?ref=196392)

## Why pay for Tokyo at all, and when it is the wrong buy

A Japan-located server removes the round trip to Europe or the US for anyone in Japan, and the same box covers South Korea and Taiwan well enough that a single deployment can serve several East Asian markets. That is the entire argument for the location, and it is a solid one if your users are actually there.

Tokyo is not a latency guarantee, though. How fast a visitor reaches the machine depends on the route their traffic takes, not the distance on a map. KernelHost says as much on its own Tokyo page, and the practical consequence is that two hosts in the same city can feel completely different from the same city.

So test before you commit. Ask support for a test IP, or ping a looking-glass node from the network you care about. If most of your visitors are in Germany, a Frankfurt box is the better purchase and no amount of Tokyo branding fixes that.

## The three costs that never appear in the banner price

**1. The annual prepay discount is not uniform.** Work out 12 × monthly against the yearly rate before you commit. Discounts tend to be steepest on the smallest plan and thin out as you climb: on one Tokyo provider's list, the 512 MB tier at $19.99/month becomes $119.99/year (about 50% off), while the 4 GB tier at $49.99/month only drops to $499.99/year (about 17% off). Do that arithmetic on JustHost's own numbers rather than assuming a flat percentage, and ask whether the renewal invoice uses the discounted rate or the list rate.

**2. Tax and IPv4 are sometimes inside the price and sometimes not.** The yen figures in the market table below include 10% consumption tax and a paid IPv4 address. Most US-dollar price lists exclude VAT, and a few hosts bill IPv4 separately. A $4 plan that adds tax and an IP charge is not a $4 plan.

**3. Switching location or IP is usually irreversible.** A data-centre switch or IP switch gives you a new address and, at most hosts, the old instance is gone. That means DNS records, mail reputation, API whitelists and game-server bookmarks all need updating. KernelHost is upfront about this and refuses location changes after ordering entirely. If you plan to move, keep DNS TTL low from day one.

## Limits that decide whether the cheap plan actually works

**Fair-share traffic has a ceiling, and it is the port.** Unlimited transfer on a 300 Mbps port is not the same product as unlimited on 1 Gbps. Sustained saturation on a budget plan gets you throttled or asked to move up a tier.

**Cheap Tokyo routes are not China-optimised.** An independent test of a TYO2 machine found all three Chinese carriers on international routes, with some traffic transiting the US and noticeably worse performance at peak. If mainland China access matters, budget for a relay or pick a host that sells premium China routes in a specific location.

**IP geolocation is not something a host controls.** The same review recorded IPv4 geolocation entries pointing at the UAE on a Tokyo machine, while streaming and AI services still treated it as Japanese. Geolocation databases update on their own schedule, and KernelHost explicitly refuses to guarantee what a third-party lookup will return. Any provider promising that your IP will always resolve to Japan is overselling.

**Windows and IPv6 are not universal.** Some budget ranges ship Linux only, and some cheap entry plans are IPv6-only, which breaks anything that still needs IPv4. Check the OS list and the IP stack before ordering, not after.

## How the budget names compare on the same specs

These are third-party figures from the same November 2026 comparison, in yen, including 10% consumption tax and a paid IPv4. LightNode is quoted in US dollars from its own page and excludes tax, so do not read the two columns as a like-for-like race.

| Provider and plan | vCPU / RAM | Disk / transfer | Per month |
| --- | --- | --- | --- |
| Gcore Basic G2S (Tokyo) | 1 / 1 GB | 25 GB / unmetered | ¥630 |
| HostHatch NVMe (Tokyo) | 1 / 2 GB | 10 GB / 0.5 TB | ¥695 |
| Kamatera Basic (Tokyo) | 1 / 1 GB | 20 GB / 1 TB | ¥695 |
| AWS Lightsail (Tokyo) | 2 / 0.5 GB | 20 GB / 1 TB | ¥869 |
| Linode (Osaka) | 1 / 1 GB | 25 GB / 1 TB | ¥869 |
| Vultr Cloud Compute (Osaka) | 1 / 1 GB | 25 GB / 1 TB | ¥869 |
| HostHatch NVMe (Tokyo) | 2 / 4 GB | 20 GB / 1 TB | ¥1,042 |
| Vultr Cloud Compute (Osaka) | 1 / 2 GB | 55 GB / 2 TB | ¥1,737 |
| Contabo Storage VPS (Japan) | 2 / 4 GB | 300 GB / unmetered | ¥1,841 |
| LightNode Start (Tokyo) | 1 / 2 GB | 50 GB NVMe / 1 TB | $7.71 |

Reading it by need: the lowest 1 GB entry on that page is Gcore at ¥630, and HostHatch gives 2 GB for ¥695 with a smaller disk. If you need a lot of local storage rather than CPU, Contabo's 300 GB at ¥1,841 is a different product category and priced accordingly. LightNode's Start plan pairs 50 GB of NVMe with 2 GB of RAM at $7.71, a reasonable middle option if you want predictable panel-driven management. Vultr and Linode sit at the brand-recognition price, which buys you mature tooling rather than capacity.

## FAQ

**How cheap can a Japan VPS realistically get?**
The lowest 1 GB entry on the November 2026 comparison is ¥630 a month including tax and IPv4. JustHost's reported entry point is around $3.23. Offers under $3 usually mean IPv6-only networking, a first-term promo, or a disk too small to hold a real workload.

**Tokyo or Osaka?**
Both work for East Asian audiences. Osaka appears in the comparison at ¥869 for a 1 GB plan from Vultr and Linode, which reflects supply rather than quality. Pick the city where your users are, then test the route.

**Do I need 4 cores to run a website?**
No. A single core handles a small site with caching. RAM and disk fill up first; cores matter when you run concurrent processes such as a game server, a build runner or several containers.

**Will a cheap Tokyo VPS unlock Japanese streaming and AI services?**
Providers claim it, and those claims are vendor self-tests rather than independent verification. Services change their detection policies without notice, and geolocation mismatches happen even on genuine Japanese IPs. Treat unlocking as a bonus, not a purchase reason.

**Monthly or annual?**
Start monthly. Once you know the box is stable and the route is good, prepay and pocket the discount, after confirming the yearly rate is not simply 12 × the monthly headline.

**Is the IP guaranteed to be registered in Japan?**
Not guaranteed. Hosts control allocation, not the databases that third parties query. Ask for a test IP if a specific lookup result is business-critical.

## Which plan to buy, by situation

- **One small site, a VPN endpoint, a Discord bot:** the 1 GB / 1 core plan at ~$3.23. Cheap enough to replace without regret.
- **A site with images or a growing database:** 2 GB / 2 cores at ~$5.99. The extra disk and 400 Mbps port are what you will hit first.
- **A Minecraft or Palworld server for a handful of friends:** 4 GB / 2 cores at ~$8.96, and check the CPU model before inviting 20 people.
- **Several Docker services, a CI runner, a multi-user API:** 8 GB / 4 cores at ~$18.63.
- **Storage-heavy backups or media:** skip the VPS ladder and look at Contabo's 300 GB storage tier at ¥1,841.

Two checks before you enter card details: the **renewal price** in writing, and the **cancellation and refund terms**, since the review material available for JustHost does not state a refund window and support has to confirm it. Get both in a ticket, keep the reply.

If the numbers above match your workload, start at the entry plan and scale up when a graph tells you to. 👉 [Open JustHost's Tokyo order page and confirm the current price](https://justhost.asia/?ref=196392)
