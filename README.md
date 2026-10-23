# Awesome-Web-Photo-Editor-Gallery

## Top Web Photo Editor & Gallery Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Self-Hosted Client Delivery, AI-Powered Photo Libraries & Browser-Native RAW Editing*  

**Last updated: March 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Web Photo Editor & Gallery**. These tools span two related but distinct jobs: editing photos (RAW processing, color grading, filters) and presenting them (client galleries, portfolio sites, shared family libraries) — with a spectrum running from polished subscription services to self-hosted platforms where the photos live on your own hardware.



**Examples** include Immich, PicPeak, LightCraft, CalibRaw, PhotoPrism, and the commercial platforms (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, client delivery without per-gallery fees, and browser-based RAW editing that doesn't upload originals to a stranger's server.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **Adobe Lightroom Web** — Adobe's browser-based Lightroom with Creative Cloud sync, RAW processing, and cloud storage. **Subscription required** (around $120/year). **Best for existing Adobe users** wanting browser access to their familiar editing workflow.



- **Flickr** — Long-running photo hosting and community platform. **Free tier with limits**; Pro subscription removes ads and expands storage. **Best for photographers wanting community discovery** alongside hosting.



- **SmugMug** — Portfolio and client gallery platform with customization and e-commerce. **Subscription-based** per plan tier. **Best for professional photographers** wanting polished client delivery with print sales.



- **Pixieset** — Client gallery platform for photographers. **Plans from $8/month** for basic delivery, scaling with storage and features. **Best for photographers** wanting a hosted, branded gallery experience without self-hosting.



## Open-Source GitHub Projects



- **Immich** — **The benchmark self-hosted Google Photos replacement.** AGPL-3.0 licensed, Docker-based with a companion mobile app for automatic background backup. **Local AI runs entirely on your hardware** — facial recognition clusters photos by person, object and scene detection enables semantic search ("sunset", "car"), and CLIP models power natural-language queries without sending images to a cloud API . **Timeline organization, memories, album creation, multi-user household support**, and partner sharing. **Performance is excellent even beyond 250,000 images**, but **machine learning indexing is resource-intensive** and benefits significantly from GPU or OpenVINO acceleration . **The critical caveat**: **mobile upload into Immich is one copy, not a backup** — you must independently back up both the PostgreSQL database and the upload library . **Best for families and individuals** wanting Google Photos features without handing their library to a cloud provider.



- **PicPeak** — **The self-hosted Pixieset/ShootProof alternative for photographers.** MIT licensed, Docker-based, deployable on a $5/month VPS or Raspberry Pi. **Password-protected, time-limited client galleries** with **white-label branding included free** (no per-feature paywalls), guest uploads, download analytics, and **unlimited storage bounded only by your own server** . **Beyond basic delivery**: signed webhook events for publish/upload/expiry/archive actions (built for n8n/Zapier/Slack), WhatsApp Business API sending, and **exportable selection lists compatible with Lightroom/Capture One** . **Anti-leech features** include watermarking, right-click protection, canvas rendering, and DevTools detection — aimed at wedding and event photographers worried about image theft from shared links . **Best for working photographers** wanting client delivery without monthly per-gallery fees and full data ownership.



- **LightCraft** — **The Rust-based Lightroom alternative for library management and RAW editing.** MIT/Apache dual licensed, available on **Windows, macOS, Linux, and in the browser via WebAssembly** . **Photo library management** with date/album organization, ratings, favorites, and metadata search. **Non-destructive editing** covers exposure, contrast, highlights, shadows, white balance, colors, tone curves, cropping, straightening, black-and-white effects, grain, and vignetting . **RAW support** for Sony, Canon, Nikon, and Fujifilm — though some compressed RAW formats may only display the embedded preview. **The honest caveat**: **still under development**, with missing camera-specific color profiles, printing modules, and AI-based selection tools (sky/subject selection uses traditional methods) . **Best for photographers** wanting a free Lightroom-style library manager and RAW editor without subscription, accepting early-stage limitations.



- **CalibRaw** — **The browser-and-Android RAW editor that feels like Lightroom.** Free and open-source, with desktop and **Android app** versions. **Familiar Lightroom-style sliders** for Light, Color, Tone Curve, Color Grading, Color Mixer, Effects, Masks, Lens Correction, and HDR Merging . **AI object removal runs locally on your device** — no uploading RAW files to cloud services for the AI tools to work . **Presets** apply adjustment groups across collections, and **non-destructive edits** preserve originals for multiple versions . **The caveat**: reliability is the main issue users report, though the project is improving quickly . **Best for Android and desktop users** wanting Lightroom-like RAW editing with local AI processing and no subscription.



- **PhotoPrism** — **The mature self-hosted photo manager for existing archives.** **Excels at indexing and searching large libraries with camera originals, RAW files, videos, and extensive metadata** . **Powerful search filters** by color, subject, location, and metadata. **Trade-offs**: **no native mobile app** (PWA only) and **no automatic phone backup** — requires a companion workflow. **Best for photographers and archivists** with existing large libraries where metadata and search depth matter more than phone-first backup.



### Additional Strong Open-Source Options



- **Ente** — **End-to-end encrypted photo backup** with native mobile apps. Keys never leave your device — even Ente cannot see your photos. Free tier with paid plans . Best for users wanting zero-knowledge encryption without self-hosting.

- **Lychee** — Open-source photo management with album organization, share links, and a clean interface. **Low resource usage** and simple upload workflow . Best for lightweight galleries without AI overhead.

- **Piwigo** — Mature open-source gallery with albums, tags, and plugins. **Low resource usage** and plugin-based face recognition . Best for simple album management.

- **Mediagoblin** — **Decentralized alternative to Flickr** from the GNU project. Self-hosted media publishing with video support and extensibility . Best for users wanting a federated, community-oriented photo platform.



**Frameworks for building custom systems**: Combine **Immich** for AI-powered family photo management with mobile backup, **PicPeak** for client gallery delivery without subscription fees, **LightCraft** or **CalibRaw** for RAW editing without Adobe's subscription, **PhotoPrism** for archival search across large existing libraries, and **Ente** for zero-knowledge encrypted backup — to build a web photo stack tailored to your need for client delivery, family library management, or professional editing.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Web photo editors and galleries differ significantly in scope, resource requirements, and maturity. **Immich requires multiple containers and significant CPU/GPU resources** for machine learning indexing, and **mobile upload is not a backup on its own** — independent backup of the database and library is mandatory . **LightCraft is still under development** — check RAW compatibility for your camera before migrating your library . **CalibRaw's reliability is the main reported issue**, though it is improving quickly . **PicPeak's anti-leech features target event photographers**, not casual users . **Adobe Lightroom's subscription costs around $120/year** — the open-source alternatives exist specifically to avoid that recurring cost.

- Self-hosted open-source solutions require proper Docker deployment, database backups, and storage planning — "free" self-hosted still has a headcount and hardware cost.



---



**Made for photographers, families, and creators choosing web photo tools they can own and control.**

Let's make web photo editing and galleries more open, self-hostable, and subscription-free.
