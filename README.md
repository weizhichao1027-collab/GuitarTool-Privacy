# GuitarTool privacy website

Current iOS policy: GuitarTool 1.1.4, updated 2026-10-20. Its new analytics terms apply when version 1.1.4 first becomes available to users and require explicit opt-in. The page preserves the distinction that published version 1.1.3 contains no third-party analytics SDK. Chinese and English are independent static pages at `/` and `/en/`, with localized metadata, canonical links, language alternates and JSON-LD. English requires no JavaScript. The Chinese page retains compatibility for old `?lang=en` links.

The policy explains on-device tuning, bundled offline Chinese Voice counting and preview, local preferences/training/rating eligibility, Apple StoreKit, GitHub Pages hosting and voluntary support emails. Version 1.1.4 adds optional PostHog analytics, off by default, with device ID, product interaction, purchase history, performance data and other diagnostic data linked to a random installation ID for analytics, without tracking. Analytics is stored in the United States for at most one year from collection; users may request deletion using their in-app analytics ID at weizhichao1027@gmail.com. Switching analytics off clears local pending events and the ID, but does not automatically delete uploaded records. Watch and widgets do not independently initialize the SDK. Voice playback needs neither microphone permission nor cloud synthesis. The App Store lists Shanghai Qishan Cultural Communication Co., Ltd. as seller.

The Android/Wear OS policy is preserved at `/android/`, dated 2026-10-10. Existing Android review-demonstration files are retained. The sitemap has three policies with their individual modification dates.

This repository contains generated publishable pages. The reviewed bilingual source, generator and generator regression tests live in the private native App workspace:

- `privacy-policy.html`
- `scripts/build_privacy_site.py`
- `scripts/test_build_privacy_site.py`
- `docs/release/asc-1.1.4-preparation-2026-10-20/privacy-preparation.md`
- `docs/release/asc-1.1.4-preparation-2026-10-20/privacy-deployment.json`

From that workspace, run `python3 scripts/build_privacy_site.py <this-checkout> --preserve-android` for an iOS-only update, then run `python3 scripts/test_build_privacy_site.py -v`. The preserve flag requires the published Android page to exist and leaves its bytes unchanged, because the native workspace may contain a newer Android draft. Do not edit just one generated language page or overwrite the Android policy during an iOS update. Preserve the public IndexNow proof and `.nojekyll` file. GitHub Pages publishes the root of `main`.

The generated output is deterministic and checked for local assets, anchors, privacy facts, static languages and metadata. Search notification and successful hosting do not prove indexing, ranking or AI-search inclusion.
