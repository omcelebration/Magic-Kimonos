# SHOPIFY ADMIN CONTROL GUIDE

## Access and roles
Owner path:
`Shopify Admin → Settings → Users`

Create a dedicated role for the agent or developer. Grant only permissions required for the task. Never share the owner's login.

Recommended developer permissions:
- Products and collections
- Content, files, menus, pages, metaobjects
- Online Store themes
- Domains only when necessary
- Apps only when necessary
- Settings only when necessary
- Reports only when needed
- Never grant billing, payouts, user management, or sensitive customer export access unless essential

Official:
https://help.shopify.com/en/manual/your-account/users/roles
https://help.shopify.com/en/manual/your-account/users/roles/permissions
https://help.shopify.com/en/manual/your-account/users/roles/permissions/store-permissions
https://help.shopify.com/en/manual/your-account/users/manage-users

## Main admin map
- Home: overview and alerts
- Orders: fulfillment, returns, refunds
- Products: products, variants, inventory, collections
- Customers: profiles and segments
- Content: metaobjects, files, menus
- Analytics: reports and performance
- Marketing: campaigns and automations
- Discounts: codes and automatic discounts
- Sales channels → Online Store:
  - Themes
  - Blog posts
  - Pages
  - Preferences
- Settings:
  - Store details
  - Plan
  - Billing
  - Users
  - Payments
  - Checkout
  - Shipping and delivery
  - Taxes and duties
  - Locations
  - Markets
  - Domains
  - Customer events
  - Notifications
  - Custom data
  - Languages
  - Policies
  - Apps and sales channels

## Safe theme workflow
1. Open `Online Store → Themes`.
2. Duplicate the current published theme.
3. Rename it with date and purpose.
4. Download a copy.
5. Edit only the duplicate.
6. Preview on mobile and desktop.
7. Test product, cart, checkout link, menus, forms, search, policy links.
8. Get approval.
9. Publish.
10. Retain the previous published theme as rollback.

Official:
https://help.shopify.com/en/manual/online-store/themes/managing-themes/duplicating-themes
https://help.shopify.com/en/manual/online-store/themes/managing-themes/downloading-themes

Important: A downloaded theme does not include products, collections, pages, menus, blog posts, or files.

## Product backup
Go to `Products → Export → All products → CSV`.

Official:
https://help.shopify.com/en/manual/products/import-export/export-products
https://help.shopify.com/en/manual/products/import-export

## Store backup reality
Shopify does not provide one single native full-store backup file. A complete operational backup requires:
- Theme ZIP
- Product CSV
- Customer CSV where legally appropriate
- Order export where legally appropriate
- Content/page copy
- Menu map
- Metafield/metaobject export or app-based backup
- Files/media inventory
- App list and settings record
- Markets, domains, shipping, tax and policy screenshots/records

Official:
https://help.shopify.com/en/manual/shopify-admin/duplicate-store

## Page-specific template
For Path of Light or any page needing no normal header:
1. Duplicate theme.
2. Create a separate JSON page template, e.g. `page.path-of-light.json`.
3. Assign the template to the page.
4. Use template-aware logic or a dedicated layout/section strategy.
5. Do not remove the global header from every page.

## Products
Each product needs:
- Correct title
- Clear story
- Actual fabric composition
- Price
- Variants
- Inventory
- Shipping weight
- Product category
- Vendor
- SKU/barcode where available
- High-quality media
- SEO title and description
- Image alt text
- Care instructions
- Origin
- Returns eligibility
- Artist information where relevant

## Collections
Use automated collections when rules are stable. Use manual collections for curated editorial stories.

## Markets
Verify:
- Primary market
- EUR pricing
- Netherlands VAT setup
- EU selling
- Languages
- International domains/subfolders
- Duties and shipping
Never assume tax compliance; confirm with the business accountant.

## Domains
Do not transfer or disconnect a domain without owner approval.
Check:
`Settings → Domains`

## Payments
Do not change payment providers, bank payout details, or billing without explicit owner action.

## Apps
Before installing:
- Define the exact problem.
- Check whether Shopify or Dawn already solves it.
- Review permissions.
- Check monthly cost.
- Check impact on speed.
- Get approval.
- Document uninstall procedure.
