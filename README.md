# GuitarTool privacy website

Updated 2026-10-08 for GuitarTool 1.1.2. GitHub Pages serves Chinese at `/` and English at `/en/`, with matching canonical/hreflang and `sitemap.xml`. Legacy `?lang=en` links redirect to the static English page. Language selection works without JavaScript.

The policy covers on-device microphone analysis, add-only Photos, local training presets, local rating-prompt eligibility, seven independently purchased themes, Apple StoreKit, GitHub Pages hosting and voluntary support email. It does not introduce analytics or tracking.

Review source: the companion App workspace `privacy-policy.html`. Generate this repository with `python3 scripts/build_privacy_site.py <privacy-repository-path>` from that workspace. The builder copies the icons and emits both pages from the same bilingual source; do not edit only one generated page. Current App source is not part of this public repository.

Validate both pages with JavaScript disabled and check reciprocal language links, canonical, JSON-LD, update date and visible policy content before pushing `main`. Publishing this repository triggers the existing GitHub Pages build. Check the completed Pages build and public content before marking an update deployed.
