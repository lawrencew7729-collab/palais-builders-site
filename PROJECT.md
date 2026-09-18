# PALAIS BUILDERS — roofleakingkl.com

Project archive. Last updated: 2026-09-18

---

## Identity

| Field | Value |
|---|---|
| Company | PALAIS BUILDERS (SSM: NS0299720-T) |
| Tagline | A Renovation Company |
| Domain | https://roofleakingkl.com |
| www | https://www.roofleakingkl.com → 308 redirect to apex |
| Business address | No 10, Jalan 5/2F, BTP 5, Bandar Tasik Puteri, 48020 Rawang, Selangor |
| Service area | Kuala Lumpur, Selangor, Negeri Sembilan |
| Years in business | 17 |

### Contact (as shown on site)

| Person | Phone | WhatsApp |
|---|---|---|
| Mr Yap | 012-429 2468 | wa.me/60124292468 |
| Mr Lim | 011-1083 8688 | wa.me/601110838688 |

No email published (owner decision, 2026-09-18).

---

## Hosting & repo

| Item | Value |
|---|---|
| Local folder | `C:\Users\Lawrence PA\Desktop\palais-builders-site` |
| GitHub | https://github.com/lawrencew7729-collab/palais-builders-site (public) |
| Branch | `master` |
| Vercel project | `palais-builders-site` |
| Project ID | `prj_YVGVofR4NDwhyOZS2QAaGr1cCKN8` |
| Team ID | `team_zYcaTVVBfNNI7QeVpwABxkan` |
| Domain registrar | Vercel (nameservers ns1/ns2.vercel-dns.com) |

### Deploy procedure

```bash
cd "C:\Users\Lawrence PA\Desktop\palais-builders-site"
git add -A && git commit -m "..." && git push origin master
export VERCEL_TELEMETRY_DISABLED=1
vercel deploy --prod --yes
```

Both the GitHub push (auto-deploy) and the CLI deploy are in use. CLI deploy is the
reliable path — run it after every push.

---

## Architecture

- **Single file**: `index.html` (~19KB), no build step
- **CSS**: Tailwind CDN 3.4.17 (play CDN)
- **Icons**: Lucide 0.263.0 (CDN)
- **Font**: Poppins (Google Fonts)
- **Brand colours**: `#1a237e` deep blue primary, `#283593` gradient, `#facc15` yellow CTA banner
- **Images**: all self-hosted in `assets/` — no external image host (Imgur hotlinks
  were blocked by the browser during the original build; self-hosting fixed it)

### File map

```
palais-builders-site/
├── index.html
├── robots.txt
├── sitemap.xml
└── assets/
    ├── logo.jpg          (781x800, white bg — header is white to match)
    ├── roof-1.jpg        (old, from Melaka site)
    ├── roof-2.jpg        (old, from Melaka site)
    ├── roof-3.jpg        (owner-supplied: straw-hat worker applying sealant)
    ├── roof-4.jpg        (owner-supplied: hard-hat worker caulking tile crack)
    ├── plumbing-1.jpg  plumbing-2.jpg
    ├── aircond-1.jpg   aircond-2.jpg
    └── whatsapp.png
```

### Section order (owner-specified)

```
Header → Hero (+ yellow contact banner) → Intro → Roofing → Plumbing → Aircond → Footer
```

Note: service order is **Roofing → Piping → Aircond**, deliberately different from the
sibling sites (aircondservicekl.com.my and aircondservicemelaka.com, which lead with
Aircond). This site leads with Roofing to match the domain.

---

## Sibling sites (same customer)

| Site | Brand | Service order |
|---|---|---|
| aircondservicekl.com.my | KW MEGA AIRCOND & PLUMBING | Aircond → Plumbing → Roof |
| aircondservicemelaka.com | HW MEGA AIRCOND & PLUMBING | Aircond → Plumbing → Roof |
| **roofleakingkl.com** | **PALAIS BUILDERS** | **Roof → Piping → Aircond** |

Source for this site was derived from the Melaka source ZIP the owner supplied.
The company name and domain differ deliberately: `roofleakingkl` was chosen for SEO
friendliness; Rawang is the registered business address, not the primary market.

---

## SEO state (as of 2026-09-18)

### On-page (done)

| Item | Value |
|---|---|
| Title | `Roof Repair KL, Selangor & Negeri Sembilan \| Roof Leaking & Waterproofing Specialist \| PALAIS BUILDERS` |
| H2 | `Your Trusted Roof Repair Specialist & Roofing Contractor.` |
| Schema | `RoofingContractor`, 11 areasServed, 7 serviceType |
| Canonical | https://roofleakingkl.com/ |

### Keyword coverage (from Google Autocomplete MY data)

| Keyword | Count | Type |
|---|---|---|
| roof repair | 14 | primary |
| roof leaking repair | 9 | primary |
| ceiling leaking | 7 | long-tail (hidden traffic entry) |
| waterproofing | 15 | commercial |
| roof repair specialist | 1 | high-intent long-tail |
| atap bocor | 5 | Malay |
| tukang atap bocor | 2 | Malay |
| bumbung | 1 | Malay |

Location terms covered: KL, Selangor, Negeri Sembilan, Klang, Puchong, Subang Jaya,
Petaling Jaya, Shah Alam, Rawang, Seremban, Kajang, Cheras, Ampang.

### Google Search Console

| Item | Status |
|---|---|
| Property | `https://roofleakingkl.com/` (URL-prefix type) |
| Google account | lawrencew7729@gmail.com |
| Verification | HTML tag — `<meta name="google-site-verification" content="KNJc70A_HWEa3gR2fkhqKL2FlHhesxT6Wfg2B_cYFmw" />` |
| Sitemap submitted | ✅ 2026-09-18 |
| Indexing requested | ✅ 2026-09-18 |
| Index state | `Discovered - currently not indexed` (expected for a new site) |

> ⚠️ **The verification meta tag must NEVER be removed** from `index.html`. Removing it
> drops Search Console ownership.

### Automated monitoring

Cron job: `roofleakingkl.com SEO health check` (job id `3195048d1c1a`)
- Schedule: every Monday 10:00
- Script: `~/AppData/Local/hermes/scripts/roofleakingkl_seo_check.py`
- Behaviour: silent when healthy; alerts if site down, verification tag missing,
  sitemap or robots.txt unreachable
- Verified: healthy path = silent; fault-injected path = alerts

---

## Pending / not done

| Item | Status | Owner |
|---|---|---|
| Google Business Profile | Not started — needs laptop | Lawrence |
| Service-area landing pages (Klang / Puchong / Seremban) | Owner said "wait" | TBD |
| High-res / transparent logo | Using 781x800 white-bg JPG; header is white to suit it | Awaiting designer file |
| Email address on site | Deliberately omitted | Lawrence |

---

## Gotchas learned

1. **Imgur hotlinks were blocked in-browser** even though `curl` fetched them fine
   (200 + correct bytes). Images were `naturalWidth === 0` in the page. Downloading
   all assets locally resolved it. Don't trust a 200 from curl as proof an image renders.
2. **`loading="lazy"` images report `naturalWidth === 0`** until scrolled into view —
   that is expected, not a broken image. Remove the attribute before asserting in tests.
3. **The screenshot browser only captures the viewport.** The page uses
   `h-full overflow-auto`, so `document.body.scrollHeight` stays at the viewport
   height. Neutralise the wrapper styles before a full-page screenshot, or the
   capture only shows the top.
4. **Imgur URL form matters**: `imgur.com/x.png` vs `i.imgur.com/x.png`. The original
   Melaka source used the non-`i.` form for some images.
5. **Vercel `link --yes` writes `.env.local`** with a `VERCEL_OIDC_TOKEN` and appends
   `.env*` to `.gitignore`. Gitignored, never deployed, but it is a local credential file.
