# LowEndBox Deals: Current VPS Offers From $16.99 a Year, What Each Costs per GB of RAM, and When an Annual Prepay Is the Wrong Buy (Full Comparison Table)

The cheapest verified offer in this roundup is ServerHost's 2GB KVM plan at **$16.99/year**. The best value per gigabyte is their 16GB plan at **$109.50/year**, which works out to $6.84 per GB of RAM for twelve months. RackNerd's 1GB plan is the most expensive per gigabyte here at $21.99 for a single gig, and EnderHost is the only provider in this group selling Toronto capacity by the month, at $3.84 for 4GB with their LowEndBox coupon applied.

Below is every plan I could confirm a live price for, the per-gigabyte math behind each one, which specs actually change what a $20 VPS can do, and the situations where paying twelve months up front is the wrong call.

> **Quick pick:** lowest entry price, take the 2GB annual plan at $16.99. Running Docker, a database or a game server, stretch to the 16GB/240GB NVMe plan at $109.50 a year. Not willing to prepay a full year to get a low rate, 👉 [check Evoxt's current VPS plans and prices](https://bit.ly/EvoXt) before you commit.

## All the plans, side by side

| Plan | vCPU / RAM | Disk | Transfer | Price | $/GB RAM per year |
| --- | --- | --- | --- | --- | --- |
| RackNerd 1GB | 1 / 1GB | 20GB SSD | 3TB/mo | $21.99/yr | $21.99 |
| RackNerd 2GB | 2 / 2GB | 35GB SSD | 5TB/mo | $35.99/yr | $18.00 |
| RackNerd 4GB | 3 / 4GB | 60GB SSD | 7TB/mo | $59.99/yr | $15.00 |
| RackNerd 6GB | 6 / 6GB | 100GB SSD | 12TB/mo | $89.99/yr | $15.00 |
| ServerHost 2GB | 1 / 2GB | 30GB NVMe | unmetered | $16.99/yr | $8.50 |
| ServerHost 4GB | 2 / 4GB | 60GB NVMe | unmetered | $27.99/yr | $7.00 |
| ServerHost 8GB | 4 / 8GB | 120GB NVMe | unmetered | $59.99/yr | $7.50 |
| ServerHost 10GB | 4 / 10GB | 150GB NVMe | unmetered | $79.99/yr | $8.00 |
| ServerHost 16GB | 4 / 16GB | 240GB NVMe | unmetered | $109.50/yr | $6.84 |
| ServerHost 32GB | 5 / 32GB | 480GB NVMe | unmetered | $222.22/yr | $6.94 |
| EnderHost 4GB (Toronto) | 2 / 4GB DDR4 | 40GB SSD | 2TB/mo | $3.84/mo ($46.08/yr) | $11.52 |
| EnderHost 6GB (Toronto) | 2 / 6GB DDR4 | 60GB SSD | 3TB/mo | $5.76/mo ($69.12/yr) | $11.52 |
| EnderHost 8GB (Toronto) | 3 / 8GB DDR4 | 80GB SSD | 4TB/mo | $7.68/mo ($92.16/yr) | $11.52 |

RackNerd's plans can be deployed in multiple locations and include full root access and one IPv4. ServerHost's plans are Linux only, with SSH access and a shared 1 Gbps port. EnderHost's Toronto budget line runs on dual Xeon E5-2690 v4 hardware with DDR4 memory and SSD storage, plus DDoS protection and 24/7 support.

## The per-gigabyte number changes the ranking

Sort by sticker price and ServerHost's $16.99 plan wins by a wide margin. Sort by what you actually get, and the 2GB plan is the *worst* ServerHost plan in the lineup at $8.50 per GB-year. Their 16GB plan costs $6.84 per GB-year, and you get 240GB of NVMe with it.

RackNerd sits at the other end. The 1GB plan at $21.99 is $21.99 per GB-year, nearly three times the cost per gigabyte of the same provider's 4GB plan at $15.00. Buying the smallest annual VPS is almost always the most expensive way to buy RAM, and this table makes that plain: the 4GB and 6GB RackNerd plans land on exactly the same per-gigabyte rate.

EnderHost is flat at $11.52 per GB-year across all three Toronto plans, because the coupon takes a fixed 36% off a $1.50/GB base rate. Predictable, but you pay a premium over ServerHost's annual NVMe plans for the privilege of monthly billing and a Canadian location.

Disk is the other half of the value story, and it swings hard:

- ServerHost 16GB: 240GB NVMe for $109.50, about **2.2GB of disk per dollar**
- RackNerd 4GB: 60GB SSD for $59.99, about **1GB per dollar**
- EnderHost 8GB: 80GB SSD for $92.16 a year, about **0.87GB per dollar**

If your workload stores anything (a database, container images, backups, game assets), the ServerHost 16GB and 32GB plans are in a different category from everything else here. 👉 [See Evoxt's per-plan pricing](https://bit.ly/EvoXt) if you want a second quote on high-RAM configurations before deciding.

## What the price tags don't say

**Every RackNerd and ServerHost price above is annual.** You pay for twelve months before you know whether the box handles your traffic. At $16.99 that's a cheap experiment. At $222.22 it isn't.

**"Unmetered" is not "unlimited speed."** ServerHost's plans include unmetered bandwidth on a 1 Gbps shared port. You aren't billed per gigabyte, but you're still sharing a port with other tenants, so sustained throughput depends on the node. RackNerd takes the opposite approach: a hard monthly cap of 3TB to 12TB, and you know exactly where you stand.

**vCPU counts at this price are scheduling slots, not dedicated cores.** RackNerd's 6GB plan lists 6 vCPU while ServerHost's 8GB plan lists 4. That does not make the RackNerd box 50% faster. For single-threaded work like a small PHP site or a Discord bot, the per-core clock matters more than the count.

**Promo inventory is finite.** ServerHost ran a 16GB/240GB NVMe plan at $99.99/year in August with only 100 coupons issued. That's $6.25 per GB-year, better than the $6.84 standing price by $9.51 a year. The standing price is what you can actually buy today.

**The Toronto budget line is not the fast line.** EnderHost's $3.84 plan uses DDR4 and SATA-era SSD on Xeon E5 hardware. Their premium tier runs AMD Ryzen 9 9950X with DDR5 and NVMe, priced at $3/GB per month before their 50% LowEndBox discount, which lands at $1.50/GB. That's roughly $6 a month for 4GB, versus $3.84 on the budget node. Pay the difference if you're running anything latency-sensitive.

## Which plan fits which job

**A single small site, a VPN endpoint, or a monitoring node:** ServerHost 2GB at $16.99/year. One core and 30GB NVMe is enough, and it's the least money you can spend here.

**A handful of Docker containers with real storage needs:** ServerHost 16GB at $109.50/year. 240GB of NVMe and 16GB of RAM covers most self-hosted stacks.

**High transfer volume, like a media proxy or seedbox-adjacent workload:** RackNerd 6GB at $89.99/year with 12TB monthly. The 100GB disk is the constraint, not the bandwidth.

**Canadian or US Northeast latency, billed monthly:** EnderHost's Toronto 4GB at $3.84/month. EnderHost states the Toronto pricing isn't introductory, citing owned hardware and competitive colocation rates in the city as the reason they can hold it.

**You don't want to prepay a year at all:** this is the case the table can't solve. Annual pricing is where all the low per-gigabyte numbers live, and the moment you need to walk away in month three, the savings evaporate. 👉 [Compare Evoxt's plan list](https://bit.ly/EvoXt) before you lock in twelve months.

## RackNerd's November giveaway is still open

If you're leaning toward RackNerd anyway, there's a deadline worth knowing about. Their fall giveaway runs through **November 30, 2026**, no purchase required. Prizes include a Meta Quest 3 in 512GB, a Synology DS225+ two-bay NAS, two Acer Nitro 27-inch gaming monitors, five KVM VPS prizes (4GB RAM, 3 vCPU, 60GB SSD, 7TB monthly transfer, first year free, renewing at $59.99/year with no obligation), and ten $50 account credits.

LowEndTalk members get bonus entries, but only accounts that were at least 30 days old as of November 1, 2026 qualify, so a fresh signup won't help this round.

That renewing figure is also the clearest renewal disclosure in this whole roundup: the 4GB plan renews at $59.99/year, the same as its special price.

## Questions people ask before buying

**Will the price go up at renewal?** RackNerd documents $59.99/year renewal on the 4GB plan. For the others, confirm the renewal rate at checkout before paying, since promotional first-term pricing is common in this segment.

**Can I upgrade the plan later?** ServerHost advertises one-click CPU, RAM and disk scaling with a reboot, no migration. RackNerd runs its own in-house control panel for VPS management. Both are worth testing in your first week rather than your fourth month.

**What happens if the coupon runs out?** You pay the standing price. ServerHost's current 16GB list price is $109.50/year, and that's the number to budget for. Treat any lower flash price as a bonus, not a plan.

**Is there a refund window?** Not something I could confirm for these specific offers, so read the provider's terms of service and SLA before paying annually. A $16.99 plan is low-risk; a $222.22 plan deserves five minutes with the policy page.

## Before you pay

Pick by workload, not by the headline monthly figure. Under 2GB of RAM and light disk use, the $16.99 annual plan is the sensible floor. Anything with a database or container images, go to 16GB and 240GB of NVMe at $109.50 and accept the year-long commitment. Need a Canadian IP and monthly terms, EnderHost's $3.84 Toronto plan is the only one here that offers both.

If the annual lock-in is the part that bothers you, price out a monthly alternative first. 👉 [Check Evoxt's current VPS plans and pricing](https://console.evox.com/aff.php?aff=1168) and compare the RAM and disk you'd get for the same money over twelve months.
