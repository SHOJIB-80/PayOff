# PAYOFF — Elementor / Novamira handoff

This is a practical rebuild guide for the static HTML/CSS/JS reference. Use Elementor Containers, nested Flexbox/Grid, ordinary text/image widgets, custom CSS, and native details/accordion behavior wherever possible. No section needs WebGL, a bespoke backend, a slider plugin, or scroll-jacking. The brand name PAYOFF is a working creative recommendation and still needs business-owner/domain/trademark clearance. Replace every bracketed item and any illustrative result before public launch.

## System-wide design recipe

- **Movement:** independent strategy journal crossed with print-shop proof sheets; tactile and precise, not a prebuilt SaaS template.
- **Palette:** paper `#F1EEE5`; ink `#17211D`; persimmon `#E65337`; chartreuse `#C6D36B`; ash `#B8B5AC`. Use solid inks only, no gradient/glow treatment.
- **Type:** Manrope for display and body, Instrument Serif italic for a limited number of emphasis words, DM Mono for folios, labels and source notes. Load with system fallbacks.
- **Grid/spacing:** max content width about 1440px; page gutters use `clamp(1.1rem, 5.2vw, 5.7rem)`; a broad 12-column desktop grid with asymmetric spans. Use a smaller mobile gutter, then deliberately re-order components. Section spacing varies; do not normalize every panel into identical padding.
- **Signature motif:** one persimmon decision rule with occasional registration ticks; small monospaced edge annotations; large type as an architectural element. Do not repeat the motif on every line.
- **Buttons:** squared corners, high-contrast paper/ink fills, concise verb-first label and a small arrow. Focus outline is always visible.
- **Motion:** brief reveal only on selected headings; hero and Services photos are visible immediately and do not depend on JavaScript; native disclosure rows; header settles after scroll. Support `prefers-reduced-motion`; make the no-JS state visible. No fake numeric count-up. Desktop case-study image may be sticky; mobile disables it.
- **Reusable elements:** folio/index label; red registration rule; proof/source note; editorial list row; button with arrow; metadata line; native `<details>` disclosure.
- **Imagery:** use the six licensed Pexels photographs listed in `assets/image-sources.md` for the hero, services visual band, case-study format and selected-work formats. Keep visible disclosures that all stock scenes are illustrative—not PAYOFF staff, client work, results or endorsements. Pinterest can inspire the art direction, but do not reuse unlicensed Pinterest reposts or watermarked previews. Keep the team portrait aperture as an explicit slot for an approved real person; replace client-format imagery with approved client assets before launch.

## Section-by-section implementation notes

### 1. Hero — `#top`
- **Objective:** immediately position PAYOFF around commercial handoffs, not generic growth language.
- **Composition:** 12-column asymmetry; left cover-like headline and actions, right 4:3 stock photograph of a creative team reviewing work; top folio line and small edge label. Keep image physically framed with a slight offset outline.
- **Final copy:** “Attention is the start, not the strategy.” / “The handoff is where growth earns its keep.” / “PAYOFF connects strategy, creative, acquisition and conversion—so every next move has a better chance of paying for itself.” CTA “Find the growth constraint”; secondary “Read the approach.”
- **Visual:** Pexels photo `hero-team-review.webp`, with a visible caption “Illustrative stock / not PAYOFF staff”; paper, ink, persimmon and a small chartreuse mark.
- **Interaction:** the photo is visible immediately; use only a subtle hover scale if desired. CTA arrow shifts slightly on hover/focus. No blocking image mask or intro animation.
- **Responsive:** stack headline, body/actions and image; retain only a single edge label; crop the stock photo to 4:3 on mobile without hiding its alt-described meaning.
- **Elementor:** parent Container, two-column nested Container; Heading and Text widgets left, Button widgets, Image widget in clipped overflow container right. Use CSS `aspect-ratio`, `object-fit: cover`, a pseudo-element outline and optional Motion Effects only for an understated reveal.

### 2. Trust / client signal
- **Objective:** establish credibility while accurately communicating that the business has not supplied proof.
- **Composition:** narrow, dark horizontal evidence band; four measurable-looking content units separated by fine rules, plus a source note.
- **Final copy:** “GOOD WORK SHOULD SHOW ITS WORK.” Slots: `$XXM+ revenue influenced`; `XXX+ campaigns launched`; `XX% average conversion lift`; each explicitly says “replace with verified data.”
- **Visual:** chartreuse values, restrained label type, no logo wall or badge row.
- **Interaction:** static; no invented/animated claims.
- **Responsive:** wrap into a two-column compact list with the disclosure/source text visible.
- **Elementor:** one dark Container with five child Containers; Text/Heading widgets and separator borders; set responsive columns 4→2→1 or 2.

### 3. Business problem — `#problem`
- **Objective:** prove the agency understands the systemic growth leak.
- **Composition:** oversized title set off the index rail; four horizontal editorial rows with short constraint, business implication and a red downward mark.
- **Final copy:** headline “The leak is rarely the channel. It’s the gap between them.” Rows: “Traffic without a landing decision.” / “More visits make the same uncertainty more expensive.”; “Creative without a learning loop.” / “A launch is not a lesson until the next brief changes.”; “Spend without attribution.” / “Activity reports cannot tell you what deserves another dollar.”; “Acquisition without retention.” / “When the first order is the last, paid growth has a ceiling.”
- **Visual:** type contrast and margin notes; no icon grid.
- **Interaction:** subtle arrow movement on row hover; selected heading reveals, never hide copy by default.
- **Responsive:** each row becomes a three-line sequence with number at the edge.
- **Elementor:** section Container, heading Container, repeated row Containers using CSS Grid; red mark as Text widget or pseudo-element. Keep native stacking order.

### 4. Point of view
- **Objective:** articulate how marketing choices connect to unit economics and customer value.
- **Composition:** one deep-ink full-width field with a large statement, offset explanatory paragraph and small horizontal chain.
- **Final copy:** “A click is a cost. What happens after it decides whether it was worth buying.” Supporting copy: “The promise, the offer, the page, the follow-up and the second purchase are one commercial conversation. Treat them as separate channels and you pay for the gaps.” Link: “See the full handoff.”
- **Visual:** warm paper headline, chartreuse serif phrase, red connecting rule. No interface screenshot.
- **Interaction:** reveal the main statement; no pinned scroll effect.
- **Responsive:** line-break headline deliberately and wrap the chain into short connected labels.
- **Elementor:** full-bleed background Container with inner max-width Container; Heading, Text, Link widgets, and a flex row of labels/rules. Use CSS variable colors and simple breakpoint wrap.

### 5. Services — `#services`
- **Objective:** clarify scope, why each capability matters, and its business outcome.
- **Composition:** open service index of eight expanding rows, each numbered and split into service name, short phrase and expanded three-part explanation.
- **Final copy:** section headline “The right work at the right friction.” Capabilities: Growth strategy; Paid acquisition; Creative strategy; Content systems; Landing pages; Conversion optimization; Funnels & follow-up; Retention & analytics. Each row has `What`, `Why`, `Outcome` text in the HTML. End note: “Scope is set by the constraint, not a prepackaged retainer.”
- **Visual:** native fine rules and typographic scale; no six-card grid or icons. Below the service rows, add a split photo band: a wide overhead creative/color-planning stock photo on one side, the heading “A sharper brief makes better work possible.” and supporting copy on the other. Label the image “Stock photo · not PAYOFF staff.”
- **Interaction:** native keyboard-accessible `<details>/<summary>`; first row opens on load. Optional close-siblings behavior is not required.
- **Responsive:** service number sits beside title; short descriptor wraps below; expanded copy becomes a vertical reading list.
- **Elementor:** section Container plus repeated Accordion widget panels, with each panel body built from three child text Containers. Below them, use a two-column Container with an Image widget (cropped with `object-fit: cover`) and a text Container; switch to a single column and 4:3 image at mobile. Preserve the HTML wording. If native details is unavailable, implement an accessible accordion with button `aria-expanded` states.

### 6. Performance proof
- **Objective:** make measurable business outcomes visually dominant without claiming unsupplied results.
- **Composition:** deep-ink section, offset headline and four large measures divided by subtle lines.
- **Final copy:** “Make the economics move, not just the activity.” Slots: `XX% qualified pipeline lift`, `X.X× blended return on ad spend`, `XX% lower cost per acquisition`, `$X.XM revenue influenced`; each labelled “Illustrative placeholder · verify source.” Footnote: “No vanity metrics without a business question.”
- **Visual:** chartreuse figures, persimmon units, restrained data-source notes. No fake chart/dashboard.
- **Interaction:** static until verified numeric data is provided; only then may a brief count-up be applied.
- **Responsive:** two-by-two stat arrangement with each description/source clear.
- **Elementor:** background Container, four-column flex/grid Container; Text widgets for numbers/labels. Do not add number counter widgets while figures are placeholders.

### 7. Featured case study — `#work`
- **Objective:** communicate problem → insight → decision → action → result and show how to replace the example with real proof.
- **Composition:** paper-deep section; image on left, narrative on right; sticky image on desktop only. Keep five story rows with source fields and 2–4 metric slots.
- **Final copy:** Mark “Illustrative structure · not verified client work”; title `[Client / industry]`; headline “A better result starts with a better question.” Story placeholders: `[What was limiting growth?]`, `[What did the evidence reveal?]`, `[What changed in the plan?]`, `[What was built, tested and distributed?]`, `[Verified outcome + measurement window]`; metrics `XX%`, `X.X×`, `XX%` labelled placeholder.
- **Visual:** Pexels stock photo `featured-marketing-review.webp`, visibly captioned “Illustrative stock / not client work”; retain the annotation “Replace with approved client asset.”
- **Interaction:** sticky media on large screens and subtle scale only if desired; no animated numbers until verified.
- **Responsive:** image becomes a normal first item; story follows, with no sticky scroll.
- **Elementor:** two-column Container with image Container and story Container. Use Sticky top position for desktop image, turn sticky off at mobile/tablet breakpoint; use Grid/list rows for the causal chain.

### 8. Additional project formats
- **Objective:** show possible breadth and make project proof fields easy to populate later, without inventing client wins.
- **Composition:** three varied-size image-led modules; first large, the following two smaller offset modules. Use three distinct Pexels stock scenes, not fictional campaign artwork.
- **Final copy:** “Good work has more than one shape.” Three clearly marked formats: `[Client / sector]`, `[Challenge]`, `[Service]`, `[Verified metric]`; categories consumer brand, B2B services, subscription. Mark each “Format example — not client work.”
- **Visual:** use `work-whiteboard-session.webp`, `work-chart-review.webp` and `work-creative-office.webp`, one per format. Each image has a visible caption “Format example — not client work / illustrative stock.” Keep editable client, challenge, service and verified-outcome fields below each image.
- **Interaction:** small editorial hover detail only; never make information hover-dependent.
- **Responsive:** stack as three distinct articles, preserving different visual heights and copy.
- **Elementor:** use non-uniform nested Containers with Image widgets, individual image crops and responsive ordering; first image is tall, following images are shorter. Avoid the Posts/Grid widget's identical card treatment.

### 9. Method — `#approach`
- **Objective:** show a repeatable process and reassure visitors that growth is a system.
- **Composition:** persimmon full-width panel; six numbered steps in two rows of three with one concise working note each.
- **Final copy:** “Not a funnel. A feedback system.” Steps: Find the constraint; Choose the lever; Build the handoff; Put it in market; Read the economics; Reinvest what works. Closing: “Every loop should buy us a better next question.”
- **Visual:** chartreuse indices and light rule grid; minimal accents.
- **Interaction:** no mandatory scroll animation; selected steps may reveal by viewport.
- **Responsive:** one vertical timeline with numbered left rail.
- **Elementor:** background Container, repeated child Containers in 3-column Grid; at mobile switch to one column. Use borders and labels rather than custom diagram plugin.

### 10. Customer journey — `#journey`
- **Objective:** show how capabilities connect from first attention to repeat growth.
- **Composition:** five connected points along one line; each has work domains and a business question.
- **Final copy:** “Every stage should make the next one easier.” Attention — “Will the right person stop?”; Acquisition — “Is the cost supportable?”; Conversion — “Is the next step clear?”; Retention — “Does value keep arriving?”; Expansion — “What should grow next?”
- **Visual:** thin red route with a larger conversion marker, labels and precise whitespace.
- **Interaction:** static educational diagram; line can draw in with CSS only if reduced motion is respected.
- **Responsive:** reflow into a vertical route; keep each stage’s work and question visible.
- **Elementor:** row Container with five child Containers and a pseudo-element line; switch direction to column on mobile; add vertical pseudo-element/left border.

### 11. Differentiators
- **Objective:** make the operating model concrete rather than claiming “innovative” or “data-driven.”
- **Composition:** dark field; left-offset headline and four full-width statements, each with a lettered margin label and supporting paragraph.
- **Final copy:** “Less theatre. More useful tension.” Claims: “Senior strategy stays close to the work.” “Creative gets measured, not flattened.” “Weekly learning changes the next move.” “Reporting reaches the business question.”
- **Visual:** paper type and small persimmon markers on ink; no feature cards.
- **Interaction:** subtle reveal as a group; text remains visible without JS.
- **Responsive:** labels above statements; copy below each statement.
- **Elementor:** dark Container, nested typography Containers, top/bottom borders. Use Flex/Grid; no icon widgets.

### 12. Experimentation — `#learning`
- **Objective:** prove a disciplined test loop and list useful areas for learning.
- **Composition:** oversized heading, one horizontal six-step sequence and a compact lever row.
- **Final copy:** “A hypothesis is a better starting line.” Hypothesis → Build → Launch → Measure → Learn → Scale. Levers: Messaging / Creative / Audience / Offers / Landing pages / Funnel steps. Note “Illustrative method / add approved experiment examples if available.”
- **Visual:** plain typographic sequence, fine baseline, red arrows; no data visual falsely implying a completed experiment.
- **Interaction:** only hover/focus accent; no circular animation that confuses order.
- **Responsive:** sequence wraps into two short rows or a vertical timeline; lever list wraps.
- **Elementor:** Flexbox sequence with simple Arrow text widgets; use a mobile breakpoint to wrap. If using Elementor Loop, preserve order and labels.

### 13. Client voice
- **Objective:** establish room for credible social proof while avoiding fabrication.
- **Composition:** full persimmon field, one large quote area, clear attribution and note.
- **Final copy:** `[Insert an approved client quote here.]` `[Name] · [Role] · [Company]` `[Optional verified outcome]`; visible label “Placeholder / replace with approved wording.”
- **Visual:** giant quotation mark and chartreuse line, no carousel or avatar.
- **Interaction:** static, no slider.
- **Responsive:** quote line-breaks naturally; attribution moves under it.
- **Elementor:** full-width Container, Heading/Text widget for the quote, separate Attribution Container. Do not insert any unapproved quotation.

### 14. Operating transparency
- **Objective:** explain the cadence, communications and visibility after engagement begins.
- **Composition:** editorial heading with four rows aligned as cadence, review, decision/output.
- **Final copy:** Weekly — Performance snapshot; Biweekly — Creative/experiment review; Monthly — Strategic growth review; Always — Shared reporting. Add “Cadence / align to the actual engagement before launch.”
- **Visual:** table-like rules and a warm serif output phrase, no app mockup.
- **Interaction:** no special behavior.
- **Responsive:** each row becomes a stacked time / deliverable / purpose unit.
- **Elementor:** parent Container, repeated flex row Containers, borders, child text widgets; collapse columns at tablet/mobile breakpoint.

### 15. Team and expertise — `#about`
- **Objective:** humanize the agency through a real point of view and real expertise.
- **Composition:** a portrait aperture beside an annotated profile with name/role, specialty, experience and philosophy fields.
- **Final copy:** “Good strategy needs a person who owns the call.” Supporting paragraph says to replace the profile with the real lead; fields remain visibly bracketed placeholders.
- **Visual:** current dark field is a graphic placeholder, not a fake portrait. Replace with a consented real image and genuine biography.
- **Interaction:** no portrait parallax or fake social links.
- **Responsive:** graphic/photo first, profile second, with labels preserved.
- **Elementor:** image widget in a fixed-aspect-ratio overflow Container; text/data widgets alongside. Replace only with approved real materials.

### 16. Client fit
- **Objective:** help qualified prospects recognize themselves and politely filter poor-fit expectations.
- **Composition:** two open columns—likely fit and probably not—with plus/minus mark and concise criteria.
- **Final copy:** “We’d rather find the right tension.” Good fit: established business with proven demand, a real acquisition/conversion/retention constraint, willing to act on evidence. Probably not: overnight hacks, disconnected channel output, vanity-metric reports.
- **Visual:** open rule-separated text, no cards.
- **Interaction:** none required.
- **Responsive:** one column, positive fit first.
- **Elementor:** two-column Container, heading/list Text widgets and borders; stack at mobile.

### 17. FAQ
- **Objective:** answer the eight high-intent questions without inventing policies or guarantees.
- **Composition:** narrow left title and right native disclosure list.
- **Final copy:** answers timing, company size, creative scope, contract length, reporting, internal-team collaboration, onboarding and success measurement. Exact wording is in `index.html`; contractual details are explicitly subject to confirmation.
- **Visual:** quiet paper-deep area, fine rules and small red disclosure plus sign.
- **Interaction:** native keyboard-accessible `<details>/<summary>`; no carousel or custom keyboard traps.
- **Responsive:** title appears before full-width question list.
- **Elementor:** native Accordion widget with one question per item; preserve semantic heading level and no fabricated minimum spend, contract, guarantee or start date.

### 18. Final conversion — `#contact`
- **Objective:** translate the accumulated trust into a useful conversation.
- **Composition:** dark closing panel with text left and a typographic sign-off artwork right; CTA appears before the decorative art on mobile.
- **Final copy:** “Let’s find where growth stops paying back.” CTA: “Book a Growth Strategy Call.” Microcopy: “30 minutes. No generic sales deck. We identify where growth is currently leaking.” Visible note tells the owner to replace the destination with a real booking URL.
- **Visual:** original brand system, not a hero image reused; text motif and persimmon line finish the narrative.
- **Interaction:** CTA arrow shift and optional reduced reveal.
- **Responsive:** stack with CTA early; artwork follows as nonessential decoration.
- **Elementor:** dark parent Container, two-column text/graphic containers, button widget; add verified calendar destination before launch and do not leave placeholder mailto.

### 19. Footer
- **Objective:** make services, work, about, contact, insights, social, legal and location fields discoverable without fabricated destinations.
- **Composition:** large PAYOFF sign-off, smaller closing phrase, navigation columns, business metadata and return-to-top.
- **Final copy:** “Make the handoffs pay.” Navigation links Services / Work / About / Insights / Book a call; clearly marked `[Add business email]`, `[Add LinkedIn URL]`, `[Add location if applicable]`, and `Privacy policy — add verified URL` / `Terms — add verified URL`.
- **Visual:** large wordmark with custom handoff mark and restrained chartreuse accent.
- **Interaction:** normal anchor navigation and back-to-top link.
- **Responsive:** stack brand/links; use grouped links and adequate tap area.
- **Elementor:** footer parent Container, brand Container, navigation Containers and metadata Text widgets; replace placeholder links after verified values and legal pages exist.

## Photo placement, source and crop handoff

The live reference uses the uploaded project-storage paths listed below. The ZIP includes matching optimized local WebP copies under `assets/images/`; in Elementor/Novamira, upload those local files to the site's media library and select them in Image widgets. The exact photographer, original Pexels page and license reference are in `assets/image-sources.md`.

| Placement | Local WebP | Live project-storage path | Desktop / mobile treatment | Visible framing |
|---|---|---|---|
| Hero | `assets/images/hero-team-review.webp` | `/manus-storage/hero-team-review_c4315516.webp` | Framed 4:3 editorial crop at all breakpoints; focal point near center/48%. | “Illustrative stock / not PAYOFF staff.” |
| Services image band | `assets/images/creative-color-planning.webp` | `/manus-storage/creative-color-planning_4cd4b833.webp` | Wide split-image band; mobile 4:3; keep the color swatches and people in frame. | “Stock photo · not PAYOFF staff.” |
| Featured case-study format | `assets/images/featured-marketing-review.webp` | `/manus-storage/featured-marketing-review_a7de6504.webp` | Desktop sticky image in the 1.05:1.13 frame; mobile 4:3, no sticky behavior. | “Illustrative stock / not client work.” |
| Selected-work format 01 | `assets/images/work-whiteboard-session.webp` | `/manus-storage/work-whiteboard-session_3ecb51e3.webp` | Tall image for the large lead module; crop to preserve the whiteboard and participants. | “Format example — not client work / illustrative stock.” |
| Selected-work format 02 | `assets/images/work-chart-review.webp` | `/manus-storage/work-chart-review_9b268222.webp` | Shorter landscape image; focal point near center/42%. | Same stock/work-format disclosure. |
| Selected-work format 03 | `assets/images/work-creative-office.webp` | `/manus-storage/work-creative-office_d0a210a3.webp` | Shorter landscape image; focal point near center/50%. | Same stock/work-format disclosure. |

Do not describe any pictured person as PAYOFF staff, a named client or a testimonial. Do not pair stock imagery with unverified outcomes in a way that implies the photo documents that result. Replace the illustrative photo only when approved in-house, team or client assets are supplied.

## Before public launch: replace or verify

Replace the working agency name if needed after clearance; agency logo/identity; factual metrics and their sources/time windows; client names/logos; every case-study challenge, insight, decision, execution and result; additional project names/assets; testimonials and attributions; team name/photo/credentials; booking destination/contact email/social links/location; privacy/terms destinations; exact start/contract/service policy; and suggested reporting cadence. The current page labels unsupplied facts as placeholders and must not be treated as proof of actual client outcomes.
