# Special Category Requirements

If the app falls into any of these categories, flag the additional requirements during the compliance checklist (Deliverable #14).

## Online Store Apps
Apps that modify or extend the storefront:
- Must work in the Shopify theme editor
- Must use Theme App Extensions (not ScriptTag or direct theme file edits)
- Extensions must clean up fully on uninstall
- Must not break the merchant's theme

## Embedded Apps
Apps that run inside the Shopify admin:
- Must use Shopify App Bridge (latest version)
- Must provide a 16×16px SVG navigation icon
- Must not use pop-up windows for OAuth or billing
- Must use session tokens (not third-party cookies)

## Checkout Apps
Apps that modify the checkout flow:
- Additional UI restrictions apply (Shopify controls checkout UX tightly)
- Must use Checkout UI Extensions
- Cannot redirect away from checkout
- Must comply with Shopify's checkout extensibility guidelines

## Product Sourcing Apps
Apps that connect merchants with suppliers:
- Must populate the Cost field on products
- Must comply with PCI requirements if handling payment data
- Must not source high-risk or prohibited product categories
- Must clearly disclose supplier relationships

## Subscription Apps
Apps that enable recurring purchases:
- Must use the correct Shopify purchase option categories
- Must integrate with Shopify's subscription APIs
- Must allow customers to manage subscriptions without contacting the merchant

## Ads & Marketing Apps
Apps that place ads or track marketing:
- Must use Web Pixel extensions for tracking (not ScriptTag)
- Script tags are not allowed for new apps
- Must comply with data privacy regulations for ad tracking

## Payments Apps
Apps that process payments:
- Must use the Payments Apps API
- Must be authorized through Shopify's payments partner program
- Additional security and compliance review required
- Cannot process payments outside of Shopify checkout

## Post-Purchase Apps
Apps that show content after checkout:
- Maximum 2 consecutive post-purchase requests to the customer
- Must redirect to order confirmation after post-purchase flow
- Must not block or delay order confirmation
