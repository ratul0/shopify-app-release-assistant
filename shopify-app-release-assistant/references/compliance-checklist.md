# Compliance Pre-Flight Checklist

Use this to generate the Deliverable #14 checklist, customized for the specific app.

## Technical Compliance

- [ ] OAuth flow works correctly on install, uninstall, and reinstall
- [ ] Only necessary API scopes are requested (principle of least privilege)
- [ ] GDPR webhooks implemented:
  - [ ] `customers/data_request` — returns or exports customer data
  - [ ] `customers/redact` — deletes customer data
  - [ ] `shop/redact` — deletes shop data after uninstall
- [ ] Shopify Billing API or Managed Pricing used for all charges
- [ ] Security headers set (X-Frame-Options or CSP frame-ancestors for clickjacking protection)
- [ ] No third-party cookies used (use session tokens instead)
- [ ] GraphQL Admin API used (REST Admin API is legacy since Oct 2024; required for new apps since April 2025)
- [ ] Latest Shopify App Bridge version used
- [ ] Lighthouse performance impact measured: must be < 10 points degradation (ratio > 0.9)
- [ ] No pop-up windows for OAuth or billing flows
- [ ] Theme modifications use Theme App Extensions (not direct theme file edits)
- [ ] Theme App Extensions clean up on uninstall (no orphaned code)

## Listing Compliance

- [ ] App name ≤ 30 characters
- [ ] App name starts with brand name
- [ ] App name matches between TOML file and App Submission form
- [ ] App icon is 1200×1200px, JPEG or PNG
- [ ] App icon has no text, no Shopify trademarks, no transparent background
- [ ] App introduction ≤ 100 characters, benefit-focused
- [ ] App details between 100–2,800 characters, Markdown only
- [ ] App details contain no links, bold, italics, or strikethrough
- [ ] No statistics, data claims, or superlatives ("the best" / "the first" / "the only")
- [ ] No Shopify logo in any graphics
- [ ] No myshopify.com URLs in screenshots or video
- [ ] Minimum 3 desktop screenshots at 1600×900px
- [ ] All images have alt text (max 64 characters each)
- [ ] Key features listed (each ≤ 80 characters)
- [ ] Up to 6 integrations listed (Shopify itself is not an integration)
- [ ] Up to 5 search terms (complete words, one idea per term)
- [ ] Pricing plans described
- [ ] Privacy policy link provided
- [ ] Support email provided
- [ ] Languages listed only if the app is fully translated in those languages
- [ ] Online Store requirement indicated if applicable
- [ ] Review instructions include Lighthouse performance scores (before and after install)

## Legal Compliance

- [ ] Complies with Shopify Partner Program Agreement
- [ ] Complies with Shopify Acceptable Use Policy
- [ ] Complies with Shopify API License and Terms of Use
- [ ] Privacy policy covers all collected, stored, and processed data
- [ ] GDPR compliance (data portability, right to erasure, consent)
- [ ] CCPA compliance if serving California residents
- [ ] App is not a prohibited app type (check Shopify's prohibited list)
- [ ] No payments processed outside Shopify checkout
- [ ] Theme modifications use Theme App Extensions (not ScriptTag or direct edits)
