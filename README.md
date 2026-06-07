# SaaS Directories — The Open Submission List

A clean, structured list of **921 directories, communities, and review sites** where you can list a SaaS or AI product to earn backlinks, referral traffic, and early users.

The whole thing lives in one file: [`saas-directories.csv`](./saas-directories.csv). Open it in a spreadsheet, import it into Notion/Airtable, or load it in a script — no scraping, no signup, no paywall.

```
priority,name,domain,url,domain_rating,link_type,pricing,category,phase
1,Product Hunt,producthunt.com,https://www.producthunt.com/,91,Dofollow,,Community / launch,Phase 1 — Launch essentials
2,There's An AI For That,theresanaiforthat.com,https://theresanaiforthat.com/,77,Dofollow,,SaaS / startup directory,Phase 1 — Launch essentials
...
```

## What's in the file

| Column | Meaning |
|---|---|
| `priority` | Suggested submission order (1 = do first). |
| `name` | Directory / community name. |
| `domain` | Root domain. |
| `url` | Where to submit or post. |
| `domain_rating` | Ahrefs-style Domain Rating (0–100), where known — a proxy for SEO authority. |
| `link_type` | `Dofollow` (passes SEO value) or `Nofollow` (traffic/exposure only). |
| `pricing` | `Free`, `Freemium`, `Paid`, or blank where unconfirmed. |
| `category` | AI directory · SaaS / startup directory · Review / comparison · Community / launch. |
| `phase` | A rough rollout plan (see below). |

## How to work the list

We group submissions into three phases so you don't burn a weekend submitting to low-value sites first:

- **Phase 1 — Launch essentials (~30).** The non-negotiables: Product Hunt, There's An AI For That, G2, Capterra, Hacker News, Indie Hackers. High authority *and* real traffic.
- **Phase 2 — High value (~120).** Strong backlinks or niche AI/SaaS audiences. Do these over the following weeks.
- **Phase 3 — Long-tail volume (~770).** Easy, mostly-free backlinks for SEO breadth. Batch these.

A practical filter for a busy founder: sort by `link_type = Dofollow`, then by `domain_rating` descending, and work top-down.

```bash
# Top 25 dofollow directories by authority
csvgrep -c link_type -m Dofollow saas-directories.csv \
  | csvsort -c domain_rating -r | head -26 | csvlook
```

## A note on what happens *after* you submit

Getting listed is the easy half. The part that actually moves the needle — and the part most founders quietly dread — is showing up *consistently* afterward: the launch-day posts, the follow-up threads, the carousels, the blog content that keeps a new product visible once the launch bump fades.

That's the problem we spend our days on at **[AI Brand Factory](https://www.aibrandfactory.com)**. We're putting the finishing touches on a tool that turns a few details about your product into ready-to-post blog articles, social posts, carousels, and other content built specifically to promote a SaaS — in your voice, not generic filler. Everything lands in one place — your content **[Vault](https://vault.aibrandfactory.com)** — ready to schedule and ship.

If that's useful to you, we're letting a small group into the Vault early: **[request beta access →](https://vault.aibrandfactory.com)**. No pitch, no spam — just early access and a say in what we build.

## Contributing

Found a dead link, a wrong DR, or a directory we missed? Open an issue or a PR against `saas-directories.csv`. Keep rows in the same column order and the additions are very welcome.

## License

The dataset is released under [CC BY 4.0](./LICENSE) — free to use, share, and adapt, including commercially, with attribution.

---

<sub>Maintained by the team at [AI Brand Factory](https://www.aibrandfactory.com) · we build content tools for SaaS founders. If this list saved you time, a ⭐ helps others find it.</sub>
