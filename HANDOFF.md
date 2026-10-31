# Counseling and Psychology Research Website

Last updated: October 31, 2026.
Workspace: `D:\counselingWebsite`.

## Current status

Planning only. No website has been implemented or deployed. The user wants to continue this conversation in the ChatGPT desktop app with this folder as the project.

## User-confirmed requirements

- One website with two components: a counseling service and a psychology research lab involving Berry College research students.
- Give counseling and research equal prominence with a clear switch between them.
- Support English and Chinese.
- Minimize hosting costs, ideally using a free tier.
- No clinical scheduling, intake forms, payments, accounts, or other backend features for now. Visitors can contact the counselor directly through email, phone, WeChat, or similar means.
- The user is comfortable having Codex edit files; a visual content editor is not required.

## Reference websites and preferences

- https://www.zhoupsychology.com/ — the user likes the ability to switch between service and research.
- https://indianauresearch.wixsite.com/gratitude — the corrected, working Wix reference. The user prefers its professional presentation. Its research navigation includes Research, Publications, News, Lab Members, and Contact Us, with a mission-focused homepage.
- The user is open to more formats, themes, and layouts and welcomes questions.

## Recommendations discussed, not yet selected by the user

- Build a static site. Direct contact links, a WeChat QR code, language switching, and public research content do not require a custom backend.
- Store source files in GitHub and host the public site on Cloudflare's free static hosting. Cloudflare currently recommends Workers for new projects; Workers Static Assets can serve a purely static website without custom server code. Cloudflare Pages is another supported option.
- GitHub Pages is suitable for a research-only site, but its restrictions on running an online business make it a questionable fit for a combined site advertising paid counseling.
- Wix has a free tier with branding; a custom domain and removal of ads require a paid plan. Hostinger is a paid alternative and is not needed for the initial scope.
- A provider-supplied address can keep hosting costs at zero. A custom domain would be an optional annual expense.
- Suggested visual directions: warm academic (ivory/navy/muted sage), modern research institute, or minimal scholar. The assistant preferred warm academic; the user has not chosen a visual direction.
- Template references: https://academicpages.github.io/ and https://github.com/arthelokyo/astrowind . No template or framework has been selected.

## Proposed information architecture

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

Keep Counseling / Research Lab and English / Chinese switches visible throughout. Each section should have its own relevant navigation and contact details. Make the research section's Berry College affiliation clear. Allow direct links into either section.

## Next steps when the user resumes

Continue the design discussion from these requirements. Gather the counselor/practice name, lab name, research focus, intended audience, existing biography/photos, and public contact details as needed. Do not invent credentials, research findings, student identities, or contact information. Confirm a visual direction before treating an assistant suggestion as the user's choice.

The latest request concerns moving/opening this conversation in the desktop app, not starting implementation or publishing. This file preserves project context; it does not itself move or synchronize the app's chat history. No Git commit or push has been requested.

## Hosting sources consulted during planning

- https://developers.cloudflare.com/workers/static-assets/billing-and-limitations/
- https://developers.cloudflare.com/pages/
- https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
- https://support.wix.com/en/article/what-premium-plans-does-wix-offer
