# MAG-9 Audit: Magic Kimonos Shopify Store and Theme Readiness

## Current state

Verified from local machine at start of heartbeat:
- No usable Shopify Admin access token or credentials were found in the inspected local env/files.
- Shopify CLI is not installed locally.
- No local GitHub theme repository for the live store was detected.

Because real Shopify state cannot be verified without credentials, this report should be treated as:
- a structured audit framework based on the Magic Kimonos pack guidance
- a gap checklist that can be filled in once access is available

## Storefront audit structure

### Homepage
Verify:
- Hero supports emotional, editorial, luxury feel.
- Core line is visible: WEAR ART. MOVE ENERGY.
- Editorial typography and generous whitespace are used.
- No fake urgency, countdowns, or aggressive discount banners.
- Images load responsively and support movement/nature/architecture theme.

### Header
Verify:
- Logo and brand feel is consistent.
- Navigation is minimal and intentional.
- Search is visible but not dominant.
- No dropshipping-style badges or clutter.

### Footer
Verify:
- Newsletter presence is clean and calm.
- Policies, contact, social, and legal links are present.
- No excessive link spam.

### Mobile
Verify:
- Hero, typography, and CTAs scale well.
- Product cards and menus remain usable.
- No horizontal scroll or layout breaks.
- Checkout handoff remains smooth.

### Search and cart
Verify:
- Search results surface relevant products and collections.
- Cart shows product story, variant, and price clearly.
- No cart popup spam.

## Content audit

### Products
For each product, verify:
- title reflects the garment/artwork, not generic “silk robe”
- story and artist context where applicable
- fabric composition matches actual materials:
  - viscose/rayon
  - linen
  - silk only if true
  - bamboo/chiffon only where confirmed
- price is accurate and VAT-inclusive where intended
- variants and inventory accuracy
- shipping weight
- product category
- vendor/artist
- SKU/barcode if available
- high-quality media
- SEO title/description
- image alt text
- care instructions
- origin
- returns eligibility

### Collections
Verify:
- collections are curated, not artificially bloated
- naming and organization match editorial vision
- featured collection logic exists for homepage

### Pages
Expected pages from project brief:
- Home
- Shop / Collections
- Product
- About
- Artists
- Path of Light
- Wholesale
- Contact
- Journal future
- Magic Glasses future

Confirm current existence and state of each page.

### Blogs
Verify:
- whether a Journal/blog exists
- whether posts are editorial and aligned with voice
- no empty or placeholder drafts left public

### Menus
Verify:
- main navigation matches intended page structure
- footer navigation is complete
- mobile menu is clean

### Files and media
Verify:
- hero and product imagery are editorial quality
- no low-res placeholders
- files map matches asset manifest

### Metafields
Verify presence and accuracy of:
- artist
- artwork_story
- fabric_composition
- care
- origin
- edition_size
- edition_number
- mood
- collection_story

### Metaobjects
Verify whether these exist and are populated:
- Artist
- Artwork
- Experience
- Lookbook
- Event
- Stockist

## Operations audit

### Inventory
Verify:
- current stock levels against intended 100+ incoming units and 144 references
- Magic Glasses stock if present
- no unexpected overselling risk

### Locations
Verify:
- Amsterdam inbound stock location exists or is planned
- any additional fulfillment locations

### Shipping
Verify:
- shipping rules are calm and premium
- no free-shipping hooks that undermine perceived value unless intentional
- EU delivery options are clear

### Returns
Verify:
- returns policy is available and coherent
- returns eligibility is set per product where needed

### Taxes
Verify:
- Netherlands VAT setup is correct
- EU tax handling is correct
- taxes are not misleading to customers

### Markets
Verify:
- primary market and EUR pricing
- languages and domains
- international subfolders or domains if used
- duties handling

### Payments
Verify:
- payment providers are set and visible
- no unapproved provider changes
- payout details are owner-controlled

### Notifications
Verify:
- order confirmation and fulfillment flows are branded
- no broken notification templates

### Policies
Verify:
- privacy, returns, terms of service are present
- links are accessible from footer/checkout

## Technical audit

### Published theme
Verify:
- current published theme name
- whether it is Dawn or another theme
- whether it matches expected archive/backup state

### Duplicate theme
Verify:
- whether a safe duplicate already exists
- whether download backup exists

### GitHub
Verify:
- whether theme repo exists
- branch model alignment:
  - main stable production mirror
  - development integration
  - feature branches
- whether GitHub connection is intact

### Apps
Verify:
- current app list
- impact on speed, checkout, and data
- whether any app should be removed or reviewed

### Analytics and pixels
Verify:
- analytics are present but not noisy
- tracking pixels are intended and documented

### Domains
Verify:
- connected domain is correct
- no accidental disconnect risk

### Redirects and broken links
Verify:
- no broken nav or policy links
- no unnecessary redirect chains

### Console errors
Verify:
- storefront has no obvious JS console errors
- no broken Liquid in preview

## Gaps vs Magic Kimonos pack vision

### Confirmed likely gaps to verify after access is granted
- Whether WEAR ART. MOVE ENERGY is clearly present on the homepage.
- Whether editorial homepage architecture is implemented or still default Dawn.
- Whether Path of Light page exists with intended standalone presentation.
- Whether artist/artwork metaobject system is live or missing.
- Whether fabric composition and story fields are populated.
- Whether any public product is mislabeled as silk.
- Whether pricing aligns with intended tiers and VAT expectations.
- Whether a safe published-theme duplicate/backup exists.
- Whether local theme repository is connected to GitHub.

### Hard-rule risk flags
- Any sustainability claim without evidence should be removed before publish.
- Any silk label on non-silk product is a hard stop for publishing.
- Any fake urgency or dropshipping-style banner should be removed.

## Safe theme backup/duplication checklist

Repeatable checklist:
1. Open Shopify Admin → Online Store → Themes.
2. Identify the currently published theme.
3. Duplicate the published theme.
4. Rename the duplicate with date and purpose, for example:
   - `Magic Kimonos - Backup - YYYY-MM-DD`
   - `Magic Kimonos - Dev - MAG-9`
5. Download a theme ZIP of the duplicate.
6. Store the ZIP in a safe local folder with the date in the filename.
7. Work only on the non-published duplicate.
8. Preview desktop and mobile.
9. Test product, cart, checkout, navigation, footer, forms, search, policy links.
10. Obtain explicit owner approval.
11. Publish.
12. Retain prior published theme as rollback.

## Risks

- Without credentials, this audit is structural, not definitive.
- Editing without a verified backup/duplicate is a high-risk operation.
- Missing or wrong fabric claims can create compliance or returns risk.
- Changing shipping/tax/market settings without owner confirmation can break checkout.
- Theme edits on a live published theme can break customer experience immediately.

## Reversal steps

- Keep prior published theme until new theme is verified in preview.
- Revert to previous theme via Shopify Admin if checkout or storefront breaks.
- Restore product CSV from export before bulk edits.
- Roll back Git branch if GitHub-connected theme push causes errors.
- Document every change in changelog format before publishing.

## Next step

To continue, owner must provide:
1. Shopify Admin access with least-privilege permissions:
   - Products and collections
   - Content, files, menus, pages, metaobjects
   - Online Store themes
   - Apps, markets, domains as needed
2. Confirmation of whether a local developer theme repo should be initialized or connected.

After access is granted, continue with:
- live theme snapshot
- product CSV export
- page and collection inventory
- metaobject/metafield review
- safe duplicate/backup execution
