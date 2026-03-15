# AstroShop 🔮

AstroShop is a full-stack e-commerce platform for spiritual and astrological products such as gemstones, rudraksh, bracelets, malas, and yantras.  
The project is built using a React frontend and a Spring Boot REST API backend.

---

## Tech Stack

### Frontend
- React 19
- React Router DOM 7
- Axios
- React Icons

### Backend
- Java
- Spring Boot REST API
- Maven

### Payments
- Razorpay Integration

### Styling
- CSS3 with custom properties (Dark / Light theme)

---

## Features

### Shopping
- Browse 5 product categories:
  - Gemstones
  - Rudraksh
  - Bracelets
  - Malas
  - Yantras
- Filter by zodiac sign, material, purpose, or face count
- Sort by price (low-high / high-low) or carat weight
- Gemstone variants (different carats and shapes)
- Add products to cart or wishlist

### Cart & Checkout
- Quantity management
- Remove items from cart
- Order total calculation
- Address form during checkout
- Razorpay payment integration
- Order confirmation page

### Authentication
- Register with strong password validation
- Login with 3-attempt lockout (30-second cooldown)
- Role-based redirect:
  - ADMIN → `/admin`
  - USER → `/`

### User Dashboard
- View order history
- Track order status:
  - PENDING
  - CONFIRMED
  - SHIPPED
  - DELIVERED
  - CANCELLED
- Cancel pending orders
- Manage wishlist

### Admin Panel
- Dashboard statistics
- Manage users
- Block / unblock users with reason
- Full CRUD operations for all product categories
- Order management with filtering and sorting
- Update order status

### User Experience
- Dark / Light theme toggle
- Theme preference stored in localStorage
- Auto-scrolling hero slider with manual controls
- Responsive design

---

## Project Structure

```
AstroShop
│
├── frontend
│   ├── public
│   └── src
│       ├── Components
│       ├── contexts
│       ├── Pages
│       ├── styles
│       ├── App.js
│       └── index.js
│
├── backend
│   ├── src/main/java
│   ├── src/main/resources
│   ├── pom.xml
│   ├── mvnw
│   └── mvnw.cmd
│
├── README.md
└── .gitignore
```

---

## Application Routes

| Path | Page |
|-----|-----|
| / | Home |
| /login | Login |
| /register | Register |
| /user | User Dashboard |
| /admin | Admin Dashboard |
| /gemstone | Gemstone Catalog |
| /gemstone/:name | Gemstone Details |
| /bracelet | Bracelets |
| /rudraksh | Rudraksh |
| /mala | Malas |
| /yantra | Yantras |
| /cart | Cart |
| /checkout | Checkout |
| /order-success | Order Confirmation |
| /orders | Order History |
| /wishlist | Wishlist |

---

## Getting Started

### Prerequisites
- Node.js 18+
- Java 17+
- Maven
- Backend running on `http://localhost:8080`
- Razorpay account

---

## Frontend Setup

```
cd frontend
npm install
npm start
```

App runs at:

```
http://localhost:3000
```

---

## Backend Setup

```
cd backend
mvn spring-boot:run
```

Backend runs at:

```
http://localhost:8080
```

---

## API Base URL

All API calls point to:

```
http://localhost:8080
```

Update this if your backend runs on a different port.

---

## Session & Storage

User session is stored in `localStorage` under the `user` key.

Example:

```json
{
  "id": 1,
  "name": "User Name",
  "email": "user@example.com",
  "role": "USER"
}
```

Theme preference is stored in `localStorage` under:

```
theme = dark / light
```

---

## Author

Sanika Vyas  

GitHub: https://github.com/sanikav21
