# Claude Code Website Workflow — Short Version

A practical guide for creating websites with Claude Code while keeping strategy, copy, design, code, and Figma delivery aligned.

---

## Workflow Objective

Create professional websites using Claude Code in a controlled and repeatable way, avoiding context loss, rework, excessive credit usage, and misalignment between planning, layout, and implementation.

The main logic is:

> Plan properly → approve copy and sitemap → generate in code → refine in the browser → import into Figma at the end.

---

## When to Use This Workflow

Use this process when the project involves:

- Creating or redesigning an institutional website, landing page, or service page
- Using Claude Code to generate HTML/CSS/JS
- Delivering a prototype or final design in Figma
- Working with a design system, approved sitemap, approved copy, and organized assets
- Building multi-page websites that require strong visual consistency

---

## Recommended Folder Structure

```txt
Project/
├── Assets/
│   ├── Photos/
│   ├── Icons/
│   ├── Logos/
│   └── Fonts/
├── Brand Guide/
├── Copy/
├── Plan/
│   ├── 00_Full-Plan.md
│   ├── 01_Brand-Analysis.md
│   ├── 02_Website-Audit.md
│   ├── 03_Sitemap-Strategy.md
│   ├── 04_Full-Sitemap.md
│   └── 05_Brand-Direction-Review.md
├── Build/
│   └── Homepage/
│       ├── index.html
│       ├── style.css
│       ├── HANDOFF.md
│       └── IMAGE-PROMPTS.md
└── .claude/
    └── skills/
```

---

## Model Usage Policy

### Use Claude Sonnet for

- Planning
- File organization
- Initial audits
- Documentation
- Copywriting
- Simple refactors
- Image prompt writing
- Mechanical or repetitive tasks

### Use Claude Opus for

- First critical visual generation
- Homepage refinement
- Important UX/UI decisions
- Accessibility audits
- Visual and responsive polish
- Strategic high-conversion pages

### Practical Rule

Start with Sonnet. Escalate to Opus only when visual quality, strategic judgment, or design-critical decisions justify the cost.

---

# Workflow in 6 Steps

---

## 1. Strategy and Planning

Before generating any layout, create the strategic foundation of the project.

### Required Inputs

- Brand guide
- Current website
- Client briefing
- Business goals
- Target audience
- Final production platform
- Technical constraints
- Deadlines
- References and anti-references

### Expected Outputs

- `Plan/00_Full-Plan.md`
- `Plan/01_Brand-Analysis.md`
- `Plan/02_Website-Audit.md`
- `Plan/03_Sitemap-Strategy.md`

### Gate Before Moving Forward

Move forward only when:

- Brand positioning is clear
- The website goal is defined
- The final platform is documented
- The main pages are justified
- The design direction is named

---

## 2. Sitemap, Structure, and Copy

Turn the strategy into a website structure, then into usable copy.

### What to Do

- Create the full sitemap
- Define the sections for each page
- Specify the purpose of each section
- Define CTAs
- Write copy by page
- Separate approved copy from provisional copy

### Expected Outputs

- `Plan/04_Full-Sitemap.md`
- `Copy/Homepage.md`
- `Copy/<Page>.md`

### Gate Before Moving Forward

Move forward only when:

- The sitemap is approved
- The homepage structure is clear
- The copy is approved or clearly marked as `SAMPLE COPY`
- Main CTAs are defined
- Navigation and footer are documented

> Avoid generating layouts with undefined copy. Major copy changes after generation create visual and structural rework.

---

## 3. Design System, References, and Assets

Prepare the visual foundation before asking Claude to generate the page.

### What to Prepare

- Colors
- Typography
- Spacing
- Buttons
- Cards
- Hover/focus states
- Grid and breakpoints
- Icons
- Real images or placeholders
- Visual references
- Anti-references

### Expected Outputs

- Design system page in Figma
- Visual sitemap page in Figma
- Organized `Assets/` folder
- List of references and anti-references
- Documented platform limitations

### Gate Before Moving Forward

Move forward only when:

- The design direction is clear
- Claude has enough visual references
- The minimum visual structure exists in Figma
- Real assets or placeholders are defined
- Technical limitations are known

---

## 4. Claude Code Setup

Before generating code, load the right context and activate the required skills.

### Context Claude Should Receive

- Brand analysis
- Website audit
- Approved sitemap
- Approved copy
- Design system
- Visual references
- Final platform
- Folder structure
- Accessibility rules
- Handoff rules

### Base Prompt to Activate Skills

```txt
Before we build the homepage, please activate the following skills for this task:
ui-ux-pro-max and frontend-design.

Use them together throughout the generation. Follow the approved sitemap, copy, brand direction, design system, and platform limitations. Prioritize production-grade visual output, accessibility, responsive behavior, and clean code.
```

### Gate Before Moving Forward

Move forward only when:

- Claude has access to the right files
- Skills are activated
- `HANDOFF.md` exists
- The page folder is created
- The homepage is the next logical page to generate

---

## 5. Generation, Review, and Refinement

Generate the homepage first. It becomes the visual standard for the rest of the website.

### What to Generate

- HTML
- CSS
- Minimal JS, if needed
- Reusable components
- Hover/focus states
- Responsive behavior
- Image placeholders
- `IMAGE-PROMPTS.md` with prompts for each missing asset

### Review in the Browser

Check:

- Visual hierarchy
- Spacing rhythm
- Responsiveness
- Accessibility
- Contrast
- Focus states
- Scroll behavior
- Images
- Alignment
- Component consistency

### Refine in Code

Polish the page in code, not in Figma.

Adjust:

- Padding
- Gaps
- Font sizes
- Line heights
- Image crops
- Cards
- CTAs
- Header/footer
- Breakpoints
- Microinteractions

### Gate Before Moving Forward

Move forward only when:

- The homepage is visually approved
- The code is clean
- Responsive behavior is validated
- Basic accessibility has been reviewed
- `HANDOFF.md` is updated
- `IMAGE-PROMPTS.md` is complete, if there are pending images

---

## 6. Pattern Codification, Inner Pages, and Delivery

After the homepage is refined, turn its patterns into project-scoped Claude skills.

### Create Local Skills

Create them inside:

```txt
.claude/skills/
```

Minimum required skills:

```txt
<project>-design-system
<project>-page-builder
```

The design system skill must be based on the refined homepage code, not only on the brand guide.

### After That

Generate inner pages in this order:

1. Main pages
2. Conversion pages
3. Institutional pages
4. Secondary pages
5. Support pages or subpages

### Final Delivery

- Website in HTML/CSS/JS
- Published page on a temporary or final URL
- Final assets organized
- Copy in Markdown
- Figma file with design system, sitemap, and imported pages via HTML.to.design
- Final handoff

---

# Quick Checklist Before Generating the Homepage

Confirm:

- [ ] Brand analysis exists
- [ ] Audit exists or was intentionally skipped
- [ ] Sitemap is approved
- [ ] Homepage copy is approved or marked as sample
- [ ] Design direction is defined
- [ ] Visual references are attached
- [ ] Anti-references are documented
- [ ] Final platform is documented
- [ ] Assets are organized
- [ ] Placeholders are defined
- [ ] Claude skills are activated
- [ ] `HANDOFF.md` is created
- [ ] Folder structure is ready

---

# Homepage Review Checklist

Check:

- [ ] The first fold communicates the value proposition clearly
- [ ] The main CTA is visible
- [ ] Visual hierarchy is strong
- [ ] The design is aligned with the brand
- [ ] The layout does not feel generic
- [ ] Components are consistent
- [ ] Spacing follows a clear rhythm
- [ ] Mobile is well resolved
- [ ] Hover and focus states exist
- [ ] Contrast is appropriate
- [ ] Images are correct or documented as placeholders
- [ ] Code is clean enough to be reused
- [ ] `HANDOFF.md` has been updated

---

# Common Risks and How to Avoid Them

## 1. Copy Changes After Layout

**Risk:** visual rework and broken hierarchy.

**How to avoid it:** approve copy before generation or clearly mark it as `SAMPLE COPY`.

---

## 2. Claude Loses Context

**Risk:** inconsistency between sessions.

**How to avoid it:** keep `HANDOFF.md` updated and read it at the start of every session.

---

## 3. Spending Too Many Credits

**Risk:** the project gets stuck during refinement.

**How to avoid it:** use Sonnet for mechanical tasks and Opus only for critical design decisions.

---

## 4. Generating Inner Pages Before the Homepage Is Refined

**Risk:** visual inconsistency across the whole site.

**How to avoid it:** approve and refine the homepage first. Then codify the patterns into local skills.

---

## 5. Importing Into Figma Too Early

**Risk:** manual rework in Figma.

**How to avoid it:** refine in code first and import via HTML.to.design only when the page is stable.

---

## 6. Images Lack Direction

**Risk:** assets become misaligned with the brand.

**How to avoid it:** archive every prompt in `IMAGE-PROMPTS.md`, including placement, intent, and visual direction.

---

# Base Prompt to Generate the Homepage

```txt
Using the approved brand analysis, sitemap, copy, design system, visual references, and platform constraints, generate the homepage as a complete production-ready HTML page.

Requirements:
- Use semantic HTML
- Use embedded or linked CSS
- Use minimal JavaScript only where needed
- Follow the approved section order exactly
- Preserve the approved copy
- Apply the project design direction
- Use accessible contrast, focus states, landmarks, and responsive behavior
- Create reusable component patterns
- Use placeholders for missing images
- For every missing image, write a corresponding prompt into Build/Homepage/IMAGE-PROMPTS.md
- Do not invent new sections
- Do not change the approved sitemap
- Do not rewrite approved copy unless explicitly requested
```

---

# Base Prompt to Review the Homepage

```txt
Review the generated homepage against the approved sitemap, copy, design system, brand direction, and accessibility expectations.

Identify:
- Visual inconsistencies
- Weak hierarchy
- Generic sections
- Spacing issues
- Typography issues
- Component inconsistencies
- Mobile/responsive problems
- Accessibility issues
- Missing hover/focus states
- Any deviation from the approved plan

Then propose specific code-level refinements before making changes.
```

---

# Base Prompt to Create Project Skills

```txt
Analyze the refined homepage code and extract the implemented design system into project-scoped Claude skills.

Create:
1. <project>-design-system
2. <project>-page-builder

The design-system skill must reflect the actual implemented homepage, including:
- Tokens
- Typography
- Spacing
- Colors
- Components
- Hover states
- Focus states
- Accessibility rules
- Section patterns

The page-builder skill must explain how to generate future pages using:
- Plan/04_Full-Sitemap.md
- Copy/<Page>.md
- The implemented design-system skill
- Existing homepage patterns

The live/refined homepage code is the source of truth.
If the skill and the code disagree, update the skill.
```

---

# Main Rule

> Do not use Claude Code as a loose layout generator. Use it as the executor of a system that has already been planned.

This workflow works best when strategy, sitemap, copy, design system, and handoff already exist before visual generation begins.