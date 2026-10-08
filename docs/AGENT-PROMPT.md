# Copy this prompt into another agent

Use https://github.com/prashaantr/stratum-industrial as the design reference. Clone it, run `python3 -m http.server 4173 --directory dist`, and inspect it in a browser at desktop (1440px), tablet (768px), and mobile (390px). Read PRODUCT.md, DESIGN.md, docs/ASSETS.md, dist/index.html, dist/styles.css, and dist/app.js. Use the implemented result as evidence, not just this description.

Create a reusable agent skill named `industrial-editorial-purple` that enables another agent to build NEW websites in this visual language. Use your skill-creator workflow if available. This is a design system extraction, not a wholesale copy of STRATUM or the upstream brands.

The design blends:
- Palantir-style large photographic panels, topic navigation, dark caption blocks, and editorial scale.
- Mercury-style calm centered composition, generous whitespace, refined typography, and softly rounded controls.
- A deliberate purple system: dark plum, lavender surfaces, purple actions, and readable neutral ink.
- Heavy-industry imagery and clear, evidence-oriented content inspired by Cognite's subject matter.

Deliver a self-contained skill folder containing:
1. SKILL.md with valid frontmatter, clear trigger conditions, a concise workflow, and concrete design rules.
2. references/design-system.md with exact extracted palette, typography, spacing, radii, breakpoints, grids, photo crops, overlays, and semantic token roles. Identify source selectors for each important rule. Resolve the CSS cascade; do not copy superseded base colors.
3. references/patterns.md covering floating navigation, centered photographic hero, large image reel with tabs, split narrative sections, industry selectors, interactive product demo, closing CTA, and footer. Explain when each pattern fits and how it changes on mobile.
4. assets/tokens.css and a small framework-agnostic starter demonstrating the visual grammar. Extract reusable tokens rather than hard-coding STRATUM copy or image URLs.
5. references/quality-checklist.md and an example page that proves the skill works in a different industrial sector.

Preserve the principles, not every section or marketing sentence. Clearly distinguish observed rules from optional extensions. Use original identity and copy for new sites. Do not invent customers, outcomes, ROI, certifications, or operational capabilities. Label synthetic demos. Keep stock-image provenance and font licenses; do not redistribute photographs as part of the skill unnecessarily.

Accessibility and behavior requirements: visible keyboard focus, semantic navigation, keyboard-operable tabs with appropriate ARIA and roving tabindex, labeled carousel controls, reduced-motion support, descriptive image alt text, responsive layouts without horizontal overflow, readable contrast, and controls that actually work. Never add decorative auto-rotating carousels or fake form-success states.

Validate the new skill by using it to produce a small page in another sector, then inspect desktop and mobile screenshots. Report the skill folder, what you extracted, any differences from the reference, and how to invoke the skill. Avoid generic advice such as “make it premium”; specify the concrete choices that produce this design.
