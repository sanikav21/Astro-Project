# AstroShop 🔮

An e-commerce platform for spiritual and astrological products — gemstones, rudraksh, bracelets, malas, and yantras. Built with React and powered by a Spring Boot REST API.

---

## Tech Stack

- **Frontend:** React 19, React Router DOM 7, Axios, React Icons
- **Backend:** Spring Boot REST API (`localhost:8080`)
- **Payments:** Razorpay
- **Styling:** CSS3 with custom properties (dark/light theme)

---

## Features

### Shopping
- Browse 5 product categories: Gemstones, Rudraksh, Bracelets, Malas, Yantras
- Filter by zodiac sign, material, purpose, or face count
- Sort by price (low-high / high-low) or carat weight
- Gemstone variants (different carats and shapes)
- Add to cart or wishlist from any product page

### Cart & Checkout
- Quantity management, item removal, order total
- Address form with Razorpay payment integration
- Order confirmation page on successful payment

### Authentication
- Register with strong password validation (8+ chars, uppercase, lowercase, number, special char)
- Login with 3-attempt lockout (30-second cooldown)
- Role-based redirect: `ADMIN` → `/admin`, `USER` → `/`

### User Dashboard
- View order history and track status (PENDING, CONFIRMED, SHIPPED, DELIVERED, CANCELLED)
- Cancel pending orders
- Manage wishlist

### Admin Panel
- Dashboard stats (total users, products, orders, pending/confirmed counts)
- Full CRUD on all 5 product categories
- User management — block/unblock with reason
- Order management — filter by product type, sort by date/price, update order status

### UX
- Dark/light theme toggle (persisted to localStorage)
- Auto-scrolling hero slider with manual controls
- Responsive design

---

## Project Structure

```
astro/
├── public/
└── src/
    ├── Components/
    │   ├── Header.js        # Nav, theme toggle, cart/wishlist icons
    │   └── Footer.jsx       # Links, newsletter, social icons
    ├── contexts/
    │   └── ThemeContext.js  # Global dark/light theme state
    ├── Pages/
    │   ├── Home.jsx
    │   ├── Gemstone.jsx / GemstoneDetails.jsx
    │   ├── Bracelet.jsx / Rudraksh.jsx / Mala.jsx / Yantra.jsx
    │   ├── Cart.jsx / Checkout.jsx / OrderSuccess.jsx
    │   ├── Wishlist.jsx / WishlistButton.jsx
    │   ├── OrderHistory.jsx
    │   ├── Login.jsx / Register.jsx
    │   ├── UserDashboard.jsx
    │   └── AdminDashboard.jsx
    ├── styles/
    │   └── themes.css       # CSS custom properties for theming
    ├── App.js               # Route definitions
    └── index.js             # Entry point
```

---

## Routes

| Path | Page |
|------|------|
| `/` | Home |
| `/login` | Login |
| `/register` | Register |
| `/user` | User Dashboard |
| `/admin` | Admin Dashboard |
| `/gemstone` | Gemstone Catalog |
| `/gemstone/:name` | Gemstone Details |
| `/bracelet` | Bracelets |
| `/rudraksh` | Rudraksh |
| `/mala` | Malas |
| `/yantra` | Yantras |
| `/cart` | Cart |
| `/checkout` | Checkout |
| `/order-success` | Order Confirmation |
| `/orders` | Order History |
| `/wishlist` | Wishlist |

---

## Getting Started

### Prerequisites
- Node.js 18+
- Spring Boot backend running on `http://localhost:8080`
- Razorpay account (for payment integration)

### Installation

```bash
cd astro
npm install
npm start
```

App runs at `http://localhost:3000`.

---

## API Base URL

All API calls point to `http://localhost:8080`. Update this in each page file if your backend runs on a different port.

---

## Session & Storage

User session is stored in `localStorage` under the `user` key:

```json
{
  "id": 1,
  "name": "User Name",
  "email": "user@example.com",
  "role": "USER"
}
```

Theme preference is stored under the `theme` key (`dark` / `light`).
