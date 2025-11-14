Daraz-like E-Commerce Store (HTML + CSS + Minimal JavaScript)

What this is
- A fully responsive e-commerce template with product listing, cart, and checkout flow.
- Built with HTML, CSS, and minimal JavaScript for cart/checkout functionality.
- Uses localStorage to persist cart and orders (client-side only, no server required).

Files
- `index.html` — main store homepage with product grid and "Add to Cart" buttons.
- `styles.css` — responsive styling for all pages.
- `cart.html` — shopping cart page showing items, quantities, and totals.
- `checkout.html` — checkout page with delivery address form, payment method, and order review.
- `README.md` — this file.

How to use

1. Open the homepage:
```powershell
cd "c:\Users\acer\OneDrive\Documents\BIT Texas\Project"
Start-Process .\index.html
```

2. Click **Add to Cart** on any product — it will navigate to cart.html and add the item.
3. On cart.html:
   - View all items in your cart with quantities and prices.
   - Adjust quantities or remove items.
   - Click **Proceed to Checkout** to go to checkout.html.

4. On checkout.html:
   - Fill in your delivery address (name, email, phone, address, city).
   - Select a payment method (Cash on Delivery, Card, Bank Transfer, Digital Wallet).
   - Review your order summary.
   - Click **Place Order** to complete the purchase (demo confirmation).

Features

- **Responsive design** — optimized for desktop, tablet, and mobile.
- **Cart persistence** — items stored in browser localStorage; survives page refresh.
- **Order storage** — orders are saved to localStorage for demo purposes.
- **Clean layout** — removed banners, promo sections; focused on products and checkout.
- **CSS-only mini-cart toggle** — click Cart in header to see a side panel (checkbox trick).

Adding images and logos

- **Logo**: Replace "Your Logo" in the `<div class="logo">` tag with an `<img>`:
  ```html
  <img src="assets/logo.png" alt="Logo" style="height:48px">
  ```
- **Product images**: Update product-image divs in index.html with `<img>` tags or background images.
- **Banners**: You can add hero banners back if needed; use CSS background-image or `<img>` tags.

Customizing products

- Edit product titles, prices directly in `index.html`.
- Update the "Add to Cart" link href with id, title, and price parameters:
  ```html
  <a href="cart.html?id=1&title=Your Product&price=1299">Add to Cart</a>
  ```
- Add or remove product cards as needed.

Responsive breakpoints

- **Desktop** (1000px+) — 3-column product grid.
- **Tablet** (768px–999px) — 2-column grid, cart layout adjusts.
- **Mobile** (480px–767px) — 1-column grid, stacked forms.
- **Small mobile** (<480px) — full-width layout, mini-cart adjusted.

Limitations & Notes

- Cart and orders are stored in browser localStorage only.
  - Data does not persist across different browsers or devices.
  - Clearing browser data will erase cart and order history.
- The checkout form is a static HTML form; it does not submit to a server.
  - For production, connect to a backend service or payment gateway.
- Search functionality is not implemented in this version.

Next steps

- Add backend API integration to save orders to a database.
- Connect to a payment gateway (Stripe, PayPal, etc.).
- Add product detail pages.
- Implement user authentication and order history.
- Add more product categories and filtering.
