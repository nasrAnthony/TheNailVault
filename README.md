# The Nail Vault Scheduler

*The Nail Vault Scheduler* is a personal Pinterest helper that **curates**, **lets the owner review**, and then **schedules** high‑quality nail‑design Pins for the [The Nail Vault Pinterest account](https://www.pinterest.com/).

---

## What it does — step by step

| Stage | Action |
|-------|--------|
| **1. Collect** | Collect trending artificial‑nail sets from various sources. |
| **2. Filter** | Uses computer‑vision & BLIP captioning to keep only images that clearly show hands and elegant nail art. |
| **3. **Manual Review** | **Every retained image is presented in a local GUI/CLI prompt (“Publish this Pin? [y/n]”).**  No Pin is created without explicit approval by the account owner. |
| **4. Schedule** | Approved images are queued (≈ 1 pin / 2 h, well under Pinterest’s daily limits) using the official Pinterest v5 API (`pins:write`, `boards:read`). |

---

## Why?

Scrolling AliExpress for cute press‑on nails yields hundreds of low‑quality shots.  
This tool surfaces the best images **and still lets the owner choose each Pin**, preventing spam and ensuring every post fits the brand aesthetic.

---

## Affiliate disclosure

Some approved Pins include AliExpress affiliate links.  
When that happens, the scheduler automatically appends **“#affiliate link”** to the Pin description to stay transparent with followers.

---

## Tech Stack

| Stage | Library / Service |
|-------|-------------------|
| Scrape | Selenium |
| Image filter | OpenCV, MediaPipe, BLIP captioning |
| Manual review UI | Tkinter dialog (or CLI prompt in headless mode) |
| Pinterest upload | Official Pinterest v5 API |
| Scheduler | APScheduler (cron‑style jobs) |

---

## Privacy

See [`privacy-policy.md`](privacy-policy.md).  
TL;DR — The script stores a Pinterest OAuth token **locally** and never shares user data.

---

## Contact

Questions or collaborations?  
**epic2battle3@gmail.com**
