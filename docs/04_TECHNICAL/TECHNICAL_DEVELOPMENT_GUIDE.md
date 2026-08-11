# TECHNICAL DEVELOPMENT GUIDE

## Theme
Known theme: Dawn. Verify the current published theme before starting.

## Theme architecture
Shopify themes use:
- `layout/`
- `templates/`
- `sections/`
- `blocks/`
- `snippets/`
- `assets/`
- `config/`
- `locales/`

Official:
https://shopify.dev/docs/storefronts/themes/architecture
https://shopify.dev/docs/storefronts/themes/architecture/templates/json-templates
https://shopify.dev/docs/api/liquid

## Development tools
- Shopify CLI
- Git
- GitHub
- Theme Check
- Browser developer tools
- Lighthouse
- Shopify theme editor

Official:
https://shopify.dev/docs/storefronts/themes/tools
https://shopify.dev/docs/storefronts/themes/tools/cli
https://shopify.dev/docs/storefronts/themes/tools/github
https://shopify.dev/docs/storefronts/themes/best-practices/version-control
https://github.com/Shopify/dawn

## Recommended Git branches
- `main`: stable production mirror
- `development`: integration
- `feature/homepage`
- `feature/path-of-light`
- `feature/product-page`

## Change rule
One purposeful change per commit. Use clear messages:
- `feat: add artist spotlight section`
- `fix: correct mobile hero spacing`
- `content: update founding collection copy`
- `chore: export theme backup`

## Suggested repository files
- `README.md`
- `CHANGELOG.md`
- `docs/brand.md`
- `docs/content-map.md`
- `docs/release-checklist.md`
- `.shopifyignore`
- theme source folders

## Shopify CLI starter commands
```bash
npm install -g @shopify/cli@latest
shopify version
shopify theme dev --store YOUR-STORE.myshopify.com
shopify theme pull --store YOUR-STORE.myshopify.com
shopify theme push --unpublished --store YOUR-STORE.myshopify.com
shopify theme check
```

Never put an Admin API access token into Git.

## GitHub integration
The Shopify GitHub integration can synchronize a theme branch with Shopify. Verify the exact store and branch before connecting.

Official:
https://shopify.dev/docs/storefronts/themes/tools/github

## APIs
Only build an app/API integration when theme and native Shopify features are insufficient.

- Admin GraphQL API: back-office data and operations
- Storefront API: headless customer-facing experiences
- Webhooks: event notifications

Official:
https://shopify.dev/docs/api
https://shopify.dev/docs/storefronts/headless/building-with-the-storefront-api/getting-started
https://shopify.dev/docs/api/usage/authentication

## Custom data
Recommended metafields:
- product.artist
- product.artwork_story
- product.fabric_composition
- product.care
- product.origin
- product.edition_size
- product.edition_number
- product.mood
- product.collection_story

Recommended metaobjects:
- Artist
- Artwork
- Experience
- Lookbook
- Event
- Stockist

Official:
https://shopify.dev/docs/apps/build/custom-data/metafields
https://shopify.dev/docs/apps/build/custom-data/metaobjects

## Performance
- Use responsive Shopify image URLs.
- Avoid oversized video.
- Lazy-load below-the-fold media.
- Keep app scripts minimal.
- Avoid duplicate font files.
- Test mobile first.
- Preserve accessibility and keyboard navigation.

Official:
https://shopify.dev/docs/storefronts/themes/best-practices/performance

## Release checklist
- Theme duplicated
- Backup downloaded
- Git commit created
- Desktop checked
- Mobile checked
- Product variants checked
- Add to cart checked
- Cart checked
- Checkout handoff checked
- Navigation checked
- Footer checked
- Forms checked
- Search checked
- Legal pages checked
- Analytics preserved
- No console errors
- Owner approval received
