# SUS TEXTILES EST. 25

A responsive textile catalogue and WhatsApp ordering website based on the supplied SUS TEXTILES logos.

## Included

- Professional customer storefront for phone, tablet and laptop
- Large SUS TEXTILES branding
- Product catalogue with image/video support
- Product price, discount price, description, origin and item code
- Search by product, collection or item code
- Collections such as Getzner
- Add-to-cart and quantity controls
- Automatic checkout total
- Required customer name, phone, address, state and country/LGA
- WhatsApp order message sent to 08134616304
- Coming-soon, sold-out and hidden product states
- Administrator login
- Administrator product upload with image/video
- Hide/show and permanent product deletion
- New collection creation
- Editable WhatsApp/social accounts
- Free-delivery option or delivery discussion on WhatsApp
- Health endpoint at /api/health
- Supplied SUS TEXTILES logo images included in /public/assets

## Run locally

1. Install Node.js 20 or newer.
2. Open this folder in a terminal.
3. Run `npm install`.
4. Set environment variables:
   - ADMIN_USERNAME
   - ADMIN_PASSWORD
5. Run `npm start`.
6. Open http://localhost:10000

## Deploy to Render

Create a Web Service from this folder/repository.

- Runtime: Node
- Build command: `npm install`
- Start command: `npm start`
- Node: 20+
- Add `ADMIN_USERNAME` and `ADMIN_PASSWORD` as Render environment variables.

### Important production note

This starter stores catalogue data in `data/store.json` and uploaded media in `public/uploads`. On a normal free Render service, local files are not a reliable permanent database/storage layer. For a production store with many products, orders and media, connect the administrator system to PostgreSQL and object storage (Cloudinary, S3-compatible storage, etc.).

The WhatsApp order is intentionally a customer-to-admin handoff: the customer reviews the cart and checkout details, then WhatsApp opens with the order information pre-filled. Delivery cost can be confirmed with the administrator.

## Logo files

The two supplied logo images are preserved as:
- `public/assets/sus-textiles-wordmark.jpg`
- `public/assets/sus-round-logo.jpg`
