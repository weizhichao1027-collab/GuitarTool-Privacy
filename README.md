# GuitarTool privacy website

Current iOS policy: GuitarTool 1.1.3, effective 2026-10-11. Chinese and English are independent static pages at `/` and `/en/`, with localized metadata, canonical links, language alternates and JSON-LD. English requires no JavaScript. The Chinese page retains compatibility for old `?lang=en` links.

The policy explains on-device tuning, bundled offline Chinese Voice counting and preview, local preferences/training/rating eligibility, Apple StoreKit, GitHub Pages hosting and voluntary support emails. Voice playback needs neither microphone permission nor cloud synthesis. The App Store lists Shanghai Qishan Cultural Communication Co., Ltd. as seller; developer support contact remains weizhichao1027@gmail.com.

The Android/Wear OS policy is preserved at `/android/`, dated 2026-10-10. Existing Android review-demonstration files are retained. The sitemap has three policies with their individual modification dates.

This repository contains generated publishable pages. The reviewed bilingual source, generator and seven generator regression tests live in the private native App workspace:

- `privacy-policy.html`
- `scripts/build_privacy_site.py`
- `scripts/test_build_privacy_site.py`
- `docs/release/website-1.1.3-2026-10-11/`

From that workspace, run the generator with this checkout as output, then run the tests. Do not edit just one generated language page or overwrite the Android policy during an iOS update. Preserve the public IndexNow proof and `.nojekyll` file. GitHub Pages publishes the root of `main`.

The generated output is deterministic and checked for local assets, anchors, privacy facts, static languages and metadata. Search notification and successful hosting do not prove indexing, ranking or AI-search inclusion.
