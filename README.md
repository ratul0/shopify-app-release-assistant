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

1. Describe your app in 2-3 sentences
2. The skill works through each deliverable in order
3. For each one, it asks 2-4 focused questions, then generates output
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
You: I need help submitting my Shopify app. It's a virtual try-on tool
     for clothing stores — shoppers upload a photo and AI shows them
     wearing the product. Aimed at fashion merchants who want to
     reduce returns.

Skill: Let's start with your App Name (max 30 characters).
       A few questions first:
       1. Is "VTon" your established brand name?
       2. In 2-3 words, what's the primary function?
       3. Any competitor app names to differentiate from?

       Here are 3 options:

       | # | Name                        | Chars |
       |---|-----------------------------|-------|
       | 1 | VTon - AI Virtual Try-On    | 25    |
       | 2 | VTon - Virtual Try-On       | 22    |
       | 3 | VTon AI Try-On              | 16    |

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
