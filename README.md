# The Nail Vault Auto‑Poster

*The Nail Vault* is a personal automation tool that feeds fresh, high‑quality nail‑design inspiration to the **[The Nail Vault Pinterest account](https://www.pinterest.com/)**.  
It does three things, end‑to‑end:

1. **Scrape** – Collects trending artificial‑nail sets from AliExpress.  
2. **Filter** – Uses computer‑vision + captioning to keep only images that clearly show hands and elegant nail art.  
3. **Publish** – Uploads the best images to a Pinterest board, adding an affiliate link to the product so followers can buy the exact set.

No user data—other than my own Pinterest access token and board ID—is stored or shared.

---

## Why?

Finding cute press‑on nail ideas means scrolling through pages of mixed‑quality results.  
This tool curates them automatically:

* consistent aesthetic (hands, not packaging)
* affiliate links only when a design passes the quality filter
* steady posting cadence (≈ 1 pin every 2 hours) to keep the board fresh

---

## Tech Stack

| Stage | Library / Service |
|-------|-------------------|
| Scrape | Selenium |
| Image filter | OpenCV, MediaPipe, BLIP captioning |
| Pinterest upload | Official Pinterest v5 API |
| Scheduler | Python + APScheduler |

---

## Privacy

See [`privacy-policy.md`](privacy-policy.md).  
TL;DR: the script stores a Pinterest OAuth token **locally** and never shares data with third parties.

---

## Contact

Questions or collaborations?  
**thenailvault@example.com**
