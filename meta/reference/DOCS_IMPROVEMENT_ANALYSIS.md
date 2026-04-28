# Documentation Improvement Analysis

Analysis comparing Promptless documentation against Good Docs Project templates and EkLine's Docs Agent landing page.

## Executive Summary

The current Promptless documentation is well-structured with good navigation and visual elements. However, there are opportunities to improve how newcomers understand what Promptless is and how it works, drawing from Good Docs Project best practices and EkLine's clear explanation flow.

**Key opportunities:**
1. Add a dedicated "What is Promptless?" concept page
2. Create a "What you can do" section with concrete use cases
3. Add more visual, numbered "How it works" explanation
4. Implement user-role-based orientation on entry pages

---

## Reference Analysis

### EkLine's Docs Agent Page Strengths

EkLine's entry page (docs.ekline.io/agent/) demonstrates several effective patterns:

| Element | How EkLine Does It | Current Promptless Approach |
|---------|-------------------|----------------------------|
| **Headline** | Clear, simple: "AI-powered assistant that generates, updates, and reviews your technical documentation" | More abstract: "Your Docs on Autopilot" |
| **Video demo** | Prominently placed at top with clear CTA | Video exists but in announcement page, not landing |
| **"What you can do"** | 5 concrete capabilities (Generate, Update from tickets, Review, Pull from integrations, Trigger from GitHub) | Benefits are described but more abstractly |
| **"How it works"** | Simple 4 numbered steps | Diagram exists but less scannable |
| **"What you can create"** | Concrete deliverables list (README, API refs, How-to guides, Release notes, etc.) | Not explicitly listed |
| **Next steps** | Two clear CTAs with time estimate ("Create your first document in 5 minutes") | Multiple cards, less focused |

### Good Docs Project Template Guidance

The Good Docs templates emphasize:

1. **Inverted pyramid structure** - Start with high-level overview, then details
2. **Clear definitions** - Define the concept before explaining features
3. **Use cases with StoryBrand** - Frame users as protagonists facing problems
4. **Visual aids** - Diagrams near the top to orient readers
5. **Scope clarity** - Explicitly state what's covered and what's not

---

## Recommended Improvements

### 1. Create a Dedicated "What is Promptless?" Concept Page

**Why:** Following Good Docs concept template guidance, newcomers need foundational context before diving into features. This page would answer "What is this?" and "Why should I care?" before "How do I use it?"

**Content structure:**
```
1. One-sentence definition
2. The problem Promptless solves (documentation drift)
3. How Promptless works (3 simple steps)
4. What you can create with Promptless (concrete deliverables)
5. Who uses Promptless (with use case scenarios)
6. Comparison to alternatives/manual approaches
```

**Good Docs guidance:** "A concept document provides the necessary context and foundational understanding... acts as a primer for users who are not yet ready to dive into concrete operations."

### 2. Add "What You Can Do" Section to Welcome Page

**Why:** EkLine's approach of listing 5-6 concrete capabilities is immediately scannable and helps users understand practical value.

**Suggested content:**
- **Generate docs from code changes** - PRs and commits automatically trigger documentation suggestions
- **Turn support conversations into docs** - Slack threads and tickets become documentation updates
- **Keep screenshots in sync** - UI screenshots auto-update when features change
- **Update docs from @mentions** - Tag @Promptless anywhere to request doc updates
- **Draft from any source** - Pull context from Jira, Linear, Confluence, and more

### 3. Simplify "How It Works" Explanation

**Current:** The welcome page has a diagram and cards, but the flow isn't as immediately scannable as EkLine's numbered steps.

**Recommendation:** Add a simpler numbered progression:

```
1. Connect your repos and tools (10-minute setup)
2. Promptless monitors for documentation triggers
3. When changes happen, Promptless drafts updates
4. Review and approve—docs stay current automatically
```

### 4. Add "What You Can Create" Section

**Why:** EkLine explicitly lists deliverables, making it concrete what documentation outputs users can expect.

**Suggested list:**
- Feature documentation and release notes
- API references and SDK guides
- Getting started guides and tutorials
- Updated screenshots and UI documentation
- Internal knowledge base articles
- Changelog entries

### 5. Add User-Role Entry Points

**Current:** The welcome page has "For Development Teams" and "For Technical Writers" cards, but they don't lead to role-specific journeys.

**Recommendation:** Create role-based "Getting Started" paths:
- **For Engineers:** Focus on PR triggers, @mentions, and hands-off automation
- **For Technical Writers:** Focus on review workflow, feedback mechanisms, style learning
- **For Product Teams:** Focus on Slack triggers, knowledge capture, cross-team visibility

### 6. Add Video Demo to Landing Page

**Why:** The Promptless 1.0 announcement video effectively demonstrates the product, but it's buried in an announcement page rather than the docs entry point.

**Recommendation:** Embed the demo video (or a shorter version) prominently on the welcome page, similar to EkLine's placement.

---

## Implementation Priority

| Priority | Improvement | Effort | Impact |
|----------|------------|--------|--------|
| **High** | Create "What is Promptless?" concept page | Medium | High - foundational understanding |
| **High** | Add "What You Can Do" section to welcome | Low | High - immediate clarity |
| **Medium** | Simplify "How It Works" to numbered steps | Low | Medium - scannability |
| **Medium** | Add "What You Can Create" deliverables list | Low | Medium - concrete expectations |
| **Medium** | Add demo video to welcome page | Low | Medium - engagement |
| **Lower** | Create role-based getting started paths | High | Medium - personalized journeys |

---

## Specific Good Docs Templates to Apply

Based on the analysis, these templates from `meta/reference/good-docs-project-template-1.5.0/` are most applicable:

1. **`concept/`** - For the "What is Promptless?" page
2. **`quickstart/`** - For improving the setup quickstart flow
3. **`how-to/`** - For task-oriented guides in "How to Use Promptless"
4. **`readme/guide_readme.md`** - For overall information architecture principles

---

## Next Steps

1. Review this analysis and prioritize which improvements to implement
2. Draft the "What is Promptless?" concept page
3. Update the welcome page with "What You Can Do" and "What You Can Create" sections
4. Consider role-based documentation paths for future iteration

---

*Analysis generated based on Good Docs Project templates v1.5.0 and https://docs.ekline.io/agent/*
