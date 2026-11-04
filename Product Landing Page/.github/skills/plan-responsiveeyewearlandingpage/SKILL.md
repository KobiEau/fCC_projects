---
name: plan-responsiveeyewearlandingpage
description: plan-responsiveEyewearLandingPage
disable-model-invocation: true
---
## Plan: Responsive Eyewear Landing Page

Teach the user to build a responsive eyewear product landing page from a clean foundation. Preserve the FreeCodeCamp goal and eyewear product theme, but treat the brand and visual direction as open. The existing HTML and CSS are references for the requirements and assets, not code to repair. Do not audit for mistakes or automatically replace the project. Teach one small step at a time: explain the concept and reasoning, give one bounded exercise, then pause for and review the user's attempt before moving on. Never rewrite the whole project for the user.

**Teaching method**
For each new concept, teach before assigning an exercise:
1. Explain the concept and its purpose in plain language.
2. Show the general mental model with a small neutral example (for example, a navbar is semantic navigation content that may be laid out vertically or horizontally; Flexbox is one layout option, not what makes it navigation).
3. Apply that model to the current project and explain the relevant HTML/CSS roles.
4. Give one bounded exercise with all short related steps in the same message.
5. Review the user's attempt, correct misunderstandings with reasoning, and only then introduce the next concept.
6. Before introducing the next concept, give a brief quiz on the concept just taught. Ask the user to explain it in their own words, predict a behavior, or apply it to a small example. Confirm the reasoning is sound; if not, reteach the unclear part and ask a focused follow-up. Do not advance until the user demonstrates understanding.

Do not present a task list without first teaching the underlying idea. Do not assume a visual result is caused by the HTML semantics: distinguish document structure, layout, and visual styling.

**Steps**
1. **Fluid baseline (first hands-on lesson):** Start with a minimal clean document and stylesheet baseline, not an audit of the existing page. Explain the viewport meta tag, the CSS box model, `box-sizing: border-box`, intrinsic sizing, and why normal block layout usually does not need `width: 100vw`/`100dvw`. Give one small exercise to create a fluid page shell and check it at a narrow and wide viewport. Do not provide the finished implementation; review the user's attempt before continuing.
2. **Responsive foundations:** Build the page structure in small steps, sizing from available space rather than fixed viewport or element dimensions. Teach how fixed and sticky positioning affect document flow, and use DevTools to identify overflow and overlap as the user's new layout grows. Do not frame existing project code as a set of fixes.
3. **Mobile-first layout:** Build the header/navigation and product-card layout with flexible tracks and wrapping, starting with small screens and adding only content-driven breakpoints when needed.
4. **Fluid media and content:** Make product images and video respect their containers; use intrinsic aspect ratio and appropriate object fitting. Keep content unconstrained by arbitrary fixed heights. Improve useful alternative text and section labels.
5. **Navigation, flow, and accessibility:** Build working section targets and anchor behavior; account for sticky navigation when jumping to sections; use semantic markup, visible focus, labels, and native form behavior. Keep all 15 FreeCodeCamp stories below in view throughout the build.
6. **Frontend design iteration:** Establish a clear product/brand direction, typography hierarchy, spacing scale, intentional color system, image treatment, and consistent control/card styling. Teach a reusable color-selection method: start from product, audience, context, and intended mood; compare a few palette directions; consider hue, value, saturation, and real content/images; then assign semantic roles such as page surface, text, primary action, accent, border, and status. Explain contrast as a way to create hierarchy without relying on color alone, and organize chosen colors as reusable CSS custom properties. Check text contrast against WCAG AA guidance (4.5:1 for normal text and 3:1 for large text) and keep controls and focus states distinguishable. Make visual refinements after the responsive structure works.
7. **Advanced responsive polish:** Teach when to use Grid vs Flexbox, fluid sizing, container constraints, intrinsic layout, focus/reduced-motion considerations, and responsive content priorities. Apply only where useful.
8. **Review and verification:** Review the user's attempt after each bounded lesson and explain the underlying rule. Finish by checking the complete acceptance list at ~320px, ~390px, ~768px, ~1280px, and wide desktop.

**Relevant files**
- `Product Landing Page .html` and `Product Landing Page.css` — reference only for project requirements and existing assets; rebuild progressively from the clean baseline instead of patching their current implementation.
- `Images/` — available product photos, logo, and promotional video to evaluate when the build reaches media.

**Acceptance and verification**
1. Confirm `<header id="header">` contains `img#header-img` and `nav#nav-bar`.
2. Confirm at least three clickable anchors inside the nav have class `.nav-link`, each points to a real corresponding section, and the navbar stays at the top of the viewport.
3. Confirm the embedded product `<video id="video">` is watchable.
4. Confirm `form#form` includes `input#email` of email type, a useful placeholder, and native email validation; include `input#submit` and submit to `https://www.freecodecamp.com/email-submit`.
5. Confirm the HTML links to the renamed `styles.css` stylesheet and that its responsive rules include at least one media query and use Flexbox at least once.
6. Run the FreeCodeCamp Product Landing Page tests if available; otherwise inspect each requirement above directly.
7. Use DevTools at the listed viewport widths to check overflow, overlap, navigation, and media. Keyboard-test links and form, check focus visibility and color contrast for text, controls, and interaction states, then review visual consistency.

**Decisions**
- Build from scratch incrementally: teach the concept first, connect a general example to the project, then give one bounded exercise containing all short related steps. Review the attempt and quiz the user on the concept before moving on; reteach and recheck when needed. Do not turn the work into a bug-fixing pass or author large sections on the user's behalf.
- Visual identity is open to redesign, but retain eyewear/product landing-page intent.
- Start with fluid CSS fundamentals before adding page sections or visual polish. Preserve the existing implementation until the user decides to replace it with their new build.
