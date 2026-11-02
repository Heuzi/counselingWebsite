# Counseling and Psychology Research Website: Strategic Plan

Last updated: November 2, 2026.
Workspace: `D:\counselingWebsite`.

## Goal and current status

Create a professional bilingual website with two equally prominent components: a counseling service and a psychology research lab involving Berry College research students. Keep initial hosting and maintenance costs as low as possible.

Planning only: no website has been implemented or deployed. Review the numbered points below one at a time, recording decisions here before moving to the next point. Assistant recommendations remain proposals until the user selects them.

## Confirmed requirements

- Counseling and research receive equal prominence, with a clear switch between them.
- Support English and Chinese.
- Use direct contact through email, phone, WeChat, or similar means.
- No clinical scheduling, intake forms, payments, accounts, or custom backend features in the initial version.
- Forms and/or scheduling are planned for a later version. Make those additions possible without rebuilding the public site or unnecessarily changing hosts.
- Website portability is a confirmed design requirement from the beginning: keep the complete project under the user's control and make it practical to change hosting or integration providers while preserving the public site's content and design.
- Prefer free hosting; a paid service is not required simply to achieve a professional appearance.
- The user is comfortable having Codex edit files; a visual content editor is not required.
- The user welcomes alternative designs and questions.

## Review sequence

| Point | Topic | Status |
| --- | --- | --- |
| 1 | Names, identity, and audience | Pending |
| 2 | Site structure and navigation | Proposed |
| 3 | Visual direction | Proposed |
| 4 | Content and bilingual presentation | To define |
| 5 | Technology, hosting, and costs | Phased functionality and portability confirmed; providers pending |
| 6 | First version and review | Future step |
| 7 | Launch and ongoing updates | Future step |

### 1. Names, identity, and audience

Decide the public name of the counseling practice, the research lab, and the overall site. Clarify whom each section serves: prospective counseling clients, Berry College research students, and any other intended visitors. Establish the lab's research focus and a short description of each component.

Recommendation: keep the two components connected through a shared introduction, while making each section's purpose and contact details clear. Identify the research lab's Berry College affiliation explicitly.

Decision: pending.

### 2. Site structure and navigation

Recommendation: a shared homepage with a short introduction and two equal entrances. Keep Counseling / Research Lab and English / Chinese switches available throughout. Allow visitors to link directly to either section.

Proposed structure; individual items may be sections or separate pages depending on available content:

```text
Home: short introduction and two equal entrances
Counseling
  About the counselor
  Services and approach
  Contact: email, phone, WeChat
Research Lab
  Research
  People
  Publications
  News
  Join the lab / Contact
```

Decision: pending.

### 3. Visual direction

Reference preferences:

- [Zhou Psychology](https://www.zhoupsychology.com/): the user likes the ability to switch between service and research.
- [Gratitude Interventions and Practices Lab](https://indianauresearch.wixsite.com/gratitude): the user prefers its professional presentation. Its mission-focused homepage and Research / Publications / News / Lab Members navigation are useful models for the lab section.

Options discussed:

| Direction | Appearance | Intended benefit |
| --- | --- | --- |
| Warm academic | Warm ivory, navy, muted sage, elegant headings, generous spacing, portrait and lab photographs | Balance an approachable counseling service with academic credibility |
| Modern research institute | White background, strong typography, wide photographs, restrained accent color | Give the lab and student work a prominent professional presentation |
| Minimal scholar | Simple typography, compact navigation, emphasis on text and publications | Keep a growing research section straightforward to maintain |

Assistant recommendation: warm academic, with related visual styles across the two sections. This is not yet the user's choice.

Template references for comparison: [Academic Pages](https://academicpages.github.io/) and [AstroWind](https://github.com/arthelokyo/astrowind). No template has been selected.

Decision: pending.

### 4. Content and bilingual presentation

Gather the existing material needed for the agreed structure: counselor biography, services and approach, public contact details, lab mission and research topics, member information, publications, news, and student involvement opportunities. Identify available portraits and lab photographs.

English and Chinese support is confirmed. Decide whether both sections will have complete translations, which language opens by default, and which Chinese writing system to use. Keep the language switch distinct from the counseling/research switch.

Use supplied or verified content. Do not invent credentials, research findings, student identities, or contact information. Publish only the contact methods the user chooses.

Decision: content inventory and translation scope pending.

### 5. Technology, hosting, and costs

Assistant recommendation: build the public website as a static site, keep the source files in GitHub, and host it using Cloudflare Workers Static Assets on the free plan. Add forms and scheduling as separate integrations when needed. Those additions should normally be changes to the contact/booking part of the site, rather than a move to a different host.

Proposed progression:

| Stage | Public website | Contact or booking behavior | Cost approach |
| --- | --- | --- | --- |
| Initial launch | Bilingual counseling and lab pages | Display email, phone, WeChat, and other selected contact details | Aim for zero hosting cost; optional annual domain registration |
| Add forms | Keep the site and its URLs | Connect a suitable hosted form service, or add a small endpoint for ordinary inquiries if needed | Select the service and plan after defining the information collected |
| Add scheduling | Keep the site and its URLs | Add a booking link or supported embedded scheduler from the chosen provider | Public hosting can remain free; scheduling service fees are separate |
| Custom functionality, only if justified | Preserve the public pages | Add selected server endpoints or a separate backend | Use free allowances where suitable; estimate storage, email, and other services separately |

Portability requirements (confirmed):

- Keep complete source files, English/Chinese content, images, and other required assets in a user-controlled project/repository. GitHub remains the proposed repository service.
- Make the initial public site deployable as standard static files on another compatible host. Keep any hosting-specific configuration or future server adapters separate from the main content and design.
- Keep form and scheduling integrations separate and configurable, so replacing a provider does not require rebuilding the public site. Evaluate data export/import capabilities before choosing a future provider; transferring appointments or submissions may require additional work.
- If the user chooses a custom domain, retain control of it and preserve public paths when changing hosts. Purchasing a domain remains optional and undecided.
- Document local setup, build commands, required configuration, and deployment steps, including an alternative compatible hosting path. Keep credentials out of tracked source files.

Implementation recommendations, not yet selected:

- Astro is a suitable starting point: generate static pages initially, with the option to add server-rendered pages or endpoints later using an appropriate adapter. Configuration and deployment work would still be needed for that change.
- For counseling appointments or intake, prefer a suitable healthcare service linked from the public site. Evaluate its handling of patient information and required agreements before collecting information. If HIPAA applies, relevant cloud providers handling electronic protected health information require a business associate agreement; free public website hosting is not itself a clinical data solution.
- Distinguish general lab inquiries from counseling appointment/intake information when choosing the future form service. The exact fields and scheduling workflow remain undecided.

Hosting findings from the earlier discussion:

- Cloudflare: the preferred free hosting candidate. Static asset requests are free and unlimited, subject to platform limits on assets and other resources. Workers can add custom server logic later; its paid plan currently starts at USD 5/month plus applicable usage and other service costs. A paid Workers plan is not required merely to link to a booking provider. Cloudflare Pages is another supported option.
- Netlify: the main alternative if built-in handling of ordinary inquiry forms is the priority. The current Free plan includes 300 credits/month; forms are free and unlimited on credit-based plans, while deployments, traffic, and other metered features use credits. The Personal plan currently starts at USD 9/month. These form features should not be assumed suitable for clinical information.
- GitHub Pages: suitable for a research-only site, but restrictions on running an online business make it a questionable fit for a combined site advertising paid counseling. Storing source files in GitHub is separate from using GitHub Pages as the host.
- Wix: a visual editor and free hosting with Wix branding; connecting a custom domain and removing ads require a paid plan.
- Hostinger: a paid alternative that is unnecessary for the initial requirements.

Cost approach: keep public hosting free for as long as it meets the site's needs. A provider-supplied address avoids domain registration costs; a custom domain offers a stable public address independent of the host. Budget for any future form/scheduling subscription separately. The hosting figures above were checked November 2, 2026; recheck terms and limits before setup.

Decision: launch with direct contact, add forms/scheduling later, and design for website portability from the beginning are confirmed. Cloudflare hosting, Astro, the domain approach, and future form/scheduling providers remain recommendations or open choices.

### 6. First version and review

After the earlier choices are settled, build a small first version around the agreed homepage and two sections. Review its appearance and navigation before expanding content.

Check the result on desktop and mobile, including readable English/Chinese text, working section and language switches, direct links, and the chosen email/phone/WeChat contact options. Review factual content and translations with the user before launch.

Verify portability before launch: confirm the site builds from a clean checkout using the documented steps, produces standard static output for the initial version, and has a documented deployment path to another compatible host without replacing its content or design. This does not require purchasing or deploying to a second host.

Decision: implementation has not started.

### 7. Launch and ongoing updates

Once the first version is ready, configure the selected host and address, then verify the live pages and links. Maintain member information, publications, news, and contact details through file edits with Codex. Keep this handoff updated with decisions and remaining work.

Forms and scheduling are planned for a later version, using the staged approach in Point 5. Payments, accounts, and other backend features are not currently planned. No Git commit, push, hosting account setup, or deployment has been requested yet.

Decision: launch timing and update routine pending.

## Where to resume

The user is currently discussing Point 5: economical hosting and adding forms/scheduling later. Website portability from the beginning is now confirmed. Hosting, framework, domain, and integration providers are still undecided. Continue with the remaining choices in this point, then return to the unresolved planning points. Discuss one topic at a time, record the user's answers, and do not reopen confirmed requirements unless the user changes them.

## Hosting sources consulted during planning

- https://developers.cloudflare.com/workers/static-assets/billing-and-limitations/
- https://developers.cloudflare.com/workers/platform/pricing/
- https://developers.cloudflare.com/pages/
- https://www.netlify.com/pricing/
- https://docs.netlify.com/manage/forms/usage-and-billing/
- https://docs.astro.build/en/guides/on-demand-rendering/
- https://support.simplepractice.com/hc/en-us/articles/115004734123-Adding-the-appointment-request-widget-to-your-website
- https://www.hhs.gov/hipaa/for-professionals/faq/may-a-hipaa-covered-entity-or-business-associate-use-cloud-service-to-store-or-process-ephi/index.html
- https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
- https://support.wix.com/en/article/what-premium-plans-does-wix-offer
