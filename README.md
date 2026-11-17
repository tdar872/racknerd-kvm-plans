# Buy VPS From $21.99/Year: RackNerd's Five KVM Plans Compared, Which Tier You Actually Need, and What the Price Doesn't Include

RackNerd's KVM specials start at **$21.99 a year** for 1 GB of RAM, and the **2 GB plan at $35.99 a year** is the one most buyers should take. It's the first tier with enough memory for a WordPress site, a VPN plus a few containers, or a bot that has to stay online around the clock. Every plan is unmanaged, provisioned automatically once payment clears, and billed for the full year up front.

Below is the complete plan list with prices and specs, the workload thresholds that decide which tier you need, and the costs the annual sticker price leaves out.

> **Most readers:** 2 GB KVM VPS at $35.99/year (2 vCores, 35 GB SSD, 5 TB transfer), which works out to about $3.00 a month.
> **Only need a VPN endpoint, a Discord bot, or a Linux sandbox:** 1 GB at $21.99/year, about $1.83 a month.
> 👉 [Check the 2 GB KVM special and current pricing](https://bit.ly/RacKnerd)

## RackNerd VPS specials: all five plans

| Plan | vCPU / RAM | SSD storage | Monthly transfer | Price (billed annually) | Order |
| --- | --- | --- | --- | --- | --- |
| 1 GB KVM VPS | 1 vCore / 1 GB | 20 GB | 3 TB | **$21.99/yr** (~$1.83/mo) | [Order the 1 GB plan](https://bit.ly/RacKnerd) |
| 2 GB KVM VPS | 2 vCores / 2 GB | 35 GB | 5 TB | **$35.99/yr** (~$3.00/mo) | [Order the 2 GB plan](https://bit.ly/RacKnerd) |
| 4 GB KVM VPS | 3 vCores / 4 GB | 60 GB | 7 TB | **$59.99/yr** (~$5.00/mo) | [Order the 4 GB plan](https://bit.ly/RacKnerd) |
| 6 GB KVM VPS | 6 vCores / 6 GB | 100 GB | 12 TB | **$89.99/yr** (~$7.50/mo) | [Order the 6 GB plan](https://bit.ly/RacKnerd) |
| 8 GB KVM VPS | 7 vCores / 8 GB | 150 GB | 20 TB | **$119.99/yr** (~$10.00/mo) | [Order the 8 GB plan](https://bit.ly/RacKnerd) |

Two practical notes on this table. RackNerd rotates these specials in batches, and the 4 GB tier has appeared with both 2 and 3 vCores in different batches, so read the configuration in the cart rather than the marketing copy. The 2 GB plan is the one RackNerd flags as most popular, which tracks with where the memory floor sits for a normal site.

### What every plan includes

- KVM virtualization and full root access over SSH, no shared-hosting restrictions
- One dedicated IPv4 address; up to 100 free IPv6 addresses on request in the Los Angeles and France locations
- 1 Gbps network port
- Access to **ctrl**, RackNerd's own control panel, for reboots, OS reinstalls, an out-of-band HTML5 VNC console, root password resets, firewall rules, in-place upgrades and one-click app installs
- Choice of CentOS, Rocky Linux, AlmaLinux, Fedora, Debian or Ubuntu, with custom ISO installs handled through a support ticket
- 24/7 support

The VNC console matters more than it looks. A bad firewall rule that kills SSH is a common way to lock yourself out of a fresh server, and a browser console gets you back in without opening a ticket.

👉 [See the full RackNerd VPS specials list](https://bit.ly/RacKnerd)

## Which tier actually fits your workload

Memory is the constraint that decides this, not core count. A single site rarely uses more than one or two cores, so paying for extra vCPUs while staying at 1 GB is the wrong trade.

**1 GB is for things that idle.** A WireGuard or OpenVPN endpoint, a monitoring agent, a Discord bot, an IRC bouncer, a jump box, or a throwaway environment for learning Linux administration. Twenty gigabytes of SSD is enough for the OS plus a small application. It is not enough for WordPress with a plugin stack, because the database and PHP workers compete for the same gigabyte.

**2 GB is the realistic minimum for a website.** WordPress, a small Laravel or Node app, a reverse proxy with a handful of services behind it, or a VPN that shares the box with something else. RackNerd's one-click catalog puts n8n and Coolify at comfortable from 2 GB, and those two are representative: an automation tool plus its database fits in this tier, a stack of five containers with Postgres does not.

**4 GB and up is for concurrent workloads.** A dynamic site with a busy database, several Docker containers running side by side, or a self-hosted AI stack. Ollama, AnythingLLM, LibreChat and Hermes Agent all want at least 4 GB in RackNerd's own guidance, and that's before you add a model that has to sit in memory. The 6 GB and 8 GB tiers exist for the same reason: OpenClaw asks for 8 GB, and a 100 GB or 150 GB disk is what you need once models, backups and logs start accumulating.

Storage lines up with the same logic. Small projects are fine in 20 to 40 GB; anything past that, whether it's media, a model directory or a growing database, needs the 100 GB tier or larger.

If you're unsure, buy one tier below what you think you need and watch memory usage for a week. Upgrading later is a panel operation, and the money you save on the first year covers the difference.

## The annual price is the whole commitment

These specials are quoted per year, so the number you see is what leaves your account, not a monthly figure that repeats. The effective monthly cost is where the comparison gets interesting:

- 1 GB: $21.99/yr, or **$1.83/month**
- 2 GB: $35.99/yr, or **$3.00/month**
- 4 GB: $59.99/yr, or **$5.00/month**
- 6 GB: $89.99/yr, or **$7.50/month**
- 8 GB: $119.99/yr, or **$10.00/month**

Compare that to hosts that bill monthly at similar specs and the gap is large. OperaVPS, for example, listed its 2 GB plan at $14.39/month on annual billing in July 2024, which is $172.68 for a year at a comparable memory tier. RackNerd's 2 GB is $35.99 for the same twelve months in a different configuration. The OperaVPS price includes a licensed Windows option and a wider location list, so it isn't a like-for-like comparison, but the direction of the difference is clear.

The trade-off is commitment. Paying $119.99 up front for the 8 GB tier means the money is gone whether you use the server for twelve months or two, and that's why the refund terms matter more than usual on annual deals.

Two costs sit outside the sticker price. The first is your own time, because these are unmanaged servers: patching, firewall rules, backups and security hardening are yours to handle. The second is commercial software. ctrl and the free panels in the one-click catalog (CyberPanel and CloudPanel among them) are included, but cPanel or Plesk licences are a separate purchase at any host, and they can cost more per month than the VPS itself.

## How the entry prices compare elsewhere

| Provider | Entry price as listed | What the entry tier buys | Policy note |
| --- | --- | --- | --- |
| RackNerd | $21.99/yr (~$1.83/mo) | 1 GB RAM, 20 GB SSD, 3 TB transfer | Unmanaged; refund terms shown at checkout |
| Infrawire | €8.30/mo | 4 GB RAM, NVMe, 7 locations | 7-day money-back on first payment only; delivery in about 5 minutes |
| is\*hosting | $5.94/mo | Entry configuration not published on the page reviewed | Trial requires an application; 40+ countries |
| OperaVPS | $6.39/mo on annual billing | 0.5 GB RAM, 10 GB storage | 3-day full refund; prices as listed July 2024 |

Currency matters here. Infrawire prices in euros, so €8.30 a month is €99.60 a year at face value, and comparing it to a dollar figure requires an exchange rate that moves. The fair way to compare across providers is per gigabyte of RAM on the same billing cycle, not the headline number.

Where RackNerd is hard to beat is the sub-$5/month band with a full year prepaid. Where it loses: no managed option on these specials, a narrower location list than the 40-country hosts, and no published SLA that I could find on the specials page.

## Four things to confirm before you pay

**1. The configuration in the cart.** Special batches vary. Check vCPU count, RAM and disk on the order form.

**2. That you want unmanaged.** RackNerd describes these specials as unmanaged KVM VPS. ctrl handles power, reinstalls, console access and firewalls, not OS updates or application security. Budget the first hour for system updates, SSH key login, a firewall and fail2ban, plus a backup routine.

**3. The refund window on the order page.** Refund policies vary widely across this price bracket: some hosts offer a 3-day full refund, others 7 days limited to the first payment, and some trials need a separate application. Read the terms attached to the specific plan rather than assuming.

**4. Delivery time and payment method.** Provisioning is automated and reviewers describe logging in within minutes of payment. Across budget hosts the realistic range runs from about five minutes to a few hours, so don't schedule a migration for the same hour you pay. Check which payment methods the checkout accepts before filling a cart.

👉 [Start with the 2 GB KVM plan at $35.99/year](https://bit.ly/RacKnerd)

## Questions that come up before checkout

**Is 1 GB enough to host a website?**
For a static site behind a lightweight server, yes. For WordPress with plugins, no. PHP workers plus MySQL will exhaust a gigabyte under any real traffic, and swapping to disk on a VPS makes the site feel broken. Start at 2 GB.

**Do I need managed hosting?**
Only if you don't want to touch a command line. Managed means the provider handles updates, patches and backups, and it costs meaningfully more everywhere it's offered. RackNerd's specials are self-managed by design, so the honest test is whether you can run `apt upgrade`, configure a firewall and set up backups without help.

**Can I run Docker, n8n or a local LLM?**
Docker and Portainer install in one click from ctrl, or over SSH if you prefer. n8n and Coolify are comfortable from 2 GB. Ollama, AnythingLLM, LibreChat and Hermes Agent want 4 GB or more, and OpenClaw asks for 8 GB.

**Linux or Windows?**
These specials ship Linux distributions. If your stack needs ASP.NET, MSSQL or a Windows desktop, check RackNerd's other product lines before ordering rather than assuming a Windows template is available here.

**Can I get IPv6?**
Yes, up to 100 addresses free on request in the Los Angeles and France locations, via a support ticket after the order. Other locations are listed as coming later.

## The final pick

Match the plan to the job and stop there:

- **VPN endpoint, bot, monitoring agent, or a Linux sandbox:** 1 GB at $21.99/year. The higher tiers buy you nothing you'll use.
- **One WordPress site, a small app, or a handful of light containers:** 2 GB at $35.99/year. This is the default answer for most people.
- **A database-heavy site, a multi-container stack, or a self-hosted AI tool:** 4 GB at $59.99/year, and move to 6 GB or 8 GB if a model has to stay loaded.
- **Several services with real traffic and 100 GB+ of data:** 6 GB or 8 GB, where the disk and transfer allowances stop being the limiting factor.

Before you pay, open the cart and read two things: the exact vCPU and RAM figures for the batch you're buying, and the refund and renewal terms on that plan. Everything else can be changed later from the panel.

👉 [Buy the RackNerd 2 GB KVM VPS and lock in the $35.99 annual rate](https://bit.ly/RacKnerd)
