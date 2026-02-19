# Shopify App Release Assistant

An AI agent skill that acts as your expert Shopify App Store release consultant — guiding you interactively through every deliverable needed to submit and list your app.

Stop guessing what Shopify will reject. This skill knows every rule, character limit, and common rejection reason, and walks you through all 14 deliverables in sequence.

## Install

```bash
npx skills add ratul0/shopify-app-release-assistant
```

## What It Does

Guides you through all **14 required deliverables** for a Shopify App Store submission:

| # | Deliverable | What You Get |
|---|-------------|-------------|
| 1 | **App Name** | 3 options with character counts, brand-first naming |
| 2 | **Subtitle** | 3 benefit-focused options under 100 chars |
| 3 | **Introduction** | 2-3 variations tied to business outcomes |
| 4 | **App Description** | Full Markdown copy (100-2,800 chars), benefit-first writing |
| 5 | **Key Features** | 4-6 scannable feature lines under 80 chars each |
| 6 | **Search Terms** | 5 optimized terms with rationale |
| 7 | **App Icon Brief** | Creative brief for your designer with specs |
| 8 | **Screenshots** | Shot list with descriptions and alt text |
| 9 | **Promo Video** | Video brief with structure and talking points |
| 10 | **Pricing Plans** | Formatted pricing descriptions for the listing |
| 11 | **Privacy & Data** | GDPR checklist, privacy policy outline, webhook list |
| 12 | **Support Info** | Formatted support section content |
| 13 | **Review Instructions** | Complete testing doc for Shopify's review team |
| 14 | **Compliance Checklist** | Technical, listing, and legal pre-flight checks |

## How It Works

1. Run the skill from your app's root directory — it automatically reads your code, configs, and project structure to understand what your app does
2. The skill asks a few targeted questions to fill gaps it can't infer from code (pricing, target audience, brand voice)
3. It works through each deliverable in order, generating output based on what it learned
4. You approve or request revisions before moving on
5. At the end, get a compiled reference document with everything

## Use When

- Preparing a Shopify app for App Store submission
- Writing your app listing (title, description, features)
- Planning screenshots or promotional assets
- Setting up privacy policy and GDPR compliance
- Writing testing instructions for Shopify reviewers
- Running a pre-submission compliance check
- Wondering why your app got rejected

## What Makes This Different

- **Cites specific Shopify rules** behind every constraint — not generic advice
- **Proactively warns** about the most common rejection reasons
- **Handles special categories** — Online Store, Checkout, Payments, Subscriptions, Ads, POS, and Post-Purchase apps each have extra requirements that this skill flags automatically
- **Character-counted output** — every option shows its count against the limit
- **Conversion-focused copy** — listing text is written to convert merchants, not just pass review

## Example

```
You: I need help submitting my Shopify app to the App Store.

Skill: I've analyzed your project. Here's what I found:
       - React-based app using Polaris components
       - Adds a product reviews widget to storefronts
       - Uses App Proxy for storefront endpoints
       - Handles customer data (review author names, emails)

       A few questions before we start:
       1. What's your brand name for this app?
       2. Who's your target merchant — niche or all stores?
       3. Do you have a pricing model in mind?

You: Brand is "Starfish", targeting small-to-mid stores, freemium.

Skill: Let's start with your App Name (max 30 characters).

       | # | Name                           | Chars |
       |---|--------------------------------|-------|
       | 1 | Starfish ‑ Product Reviews     | 28    |
       | 2 | Starfish Reviews               | 18    |
       | 3 | Starfish ‑ Reviews & Ratings   | 30    |

       Rule: Names must start with your brand name, not a generic
       descriptor. All three comply. Which works, or want revisions?
```

## Skill Structure

```
shopify-app-release-assistant/
├── SKILL.md                        # Main skill instructions (214 lines)
└── references/
    ├── description-rules.md        # Full rules for app description copy
    ├── compliance-checklist.md     # Technical, listing, and legal checks
    └── special-categories.md      # Extra rules for specific app types
```

## Compatibility

Works with any AI coding agent that supports skills:
- Claude Code
- Cursor
- Windsurf
- GitHub Copilot
- Any agent supporting SKILL.md format

## License

MIT
