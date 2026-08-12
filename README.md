# Aura Apparel 🛍️

A modern, high-performance e-commerce storefront and administration dashboard built with **Next.js 16 (App Router)**, **React 19**, **Tailwind CSS v4**, and **GSAP** animations.

---

## 🌟 Key Features

### 🛒 Storefront
* **Dynamic Home & Collection Showcase**: Featured collections, best-selling apparel, and interactive hero sections driven by smooth GSAP animations.
* **Product Catalog & Filtering**: Browse products by collection with live client & server-side filtering, search integration, and pagination.
* **Interactive Product Details**: Multi-angle image galleries, variant picker (sizes, colors, stock), and real-time inventory updates.
* **Seamless Cart Experience**: Slide-over shopping cart with instant quantity adjustments, price calculation, and local storage state sync.
* **Checkout Workflow**: Streamlined multi-step checkout form with dynamic validation and order placement.
* **Brand Story & Contact Pages**: Dedicated landing sections for brand storytelling (`/ourstory`) and customer inquiries (`/contactus`).

### ⚙️ Admin Dashboard
* **Secure Admin Portal**: Dedicated admin layout with authentication (`/admin/signin`).
* **Product Management**: Full CRUD interface for products, variants, price tracking, and media uploads.
* **Media Uploader**: Integrated image upload workflows powered by **Uploadcare**.
* **Order Management**: Monitor customer orders, track fulfillment status, and handle deletion or status updates (`/admin/orders`).

---

## 🛠️ Tech Stack

* **Framework**: [Next.js 16 (App Router)](https://nextjs.org/) & [React 19](https://react.dev/)
* **Styling**: [Tailwind CSS v4](https://tailwindcss.com/)
* **Animations**: [GSAP](https://gsap.com/) (`gsap` & `@gsap/react`)
* **Forms & Validation**: [React Hook Form](https://react-hook-form.com/) & [Zod](https://zod.dev/)
* **Media Uploads**: [Uploadcare](https://uploadcare.com/) (`@uploadcare/react-uploader`)
* **Notifications**: [Sonner](https://sonner.emilkowal.si/)
* **Language**: [TypeScript](https://www.typescriptlang.org/)
* **Package Manager**: [pnpm](https://pnpm.io/)

---

## 📁 Directory Structure

```text
aura_frontend/
├── app/
│   ├── (adminLayout)/       # Admin dashboard & login routes (/admin, /admin/orders, /admin/products)
│   ├── (checkoutLayout)/    # Checkout workflow routes (/checkout)
│   ├── (sharedLayout)/      # Main storefront pages (/collections, /ourstory, /contactus, etc.)
│   ├── action.ts            # Next.js Server Actions for cart, products, orders & admin logic
│   ├── globals.css          # Global styles & Tailwind v4 setup
│   └── layout.tsx           # Root layout component
├── components/
│   ├── app/                 # Domain-specific UI components (Cart, Forms, Filters, Admin UI, etc.)
│   ├── buttons/             # Reusable button elements
│   ├── input/               # Custom form inputs
│   └── svg/                 # SVG icon assets
├── lib/
│   ├── cache-tags.ts        # Next.js revalidation tag constants
│   ├── revalidate.ts        # Server revalidation utilities
│   ├── schemas.ts           # Zod validation schemas (products, orders, addresses)
│   └── utils.ts             # Utility functions
└── public/                  # Static assets & images
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed on your machine:
* [Node.js](https://nodejs.org/) (v18.17 or higher recommended)
* [pnpm](https://pnpm.io/) (v8 or higher)

### 1. Installation

Clone the repository and install dependencies using `pnpm`:

```bash
git clone <repository-url>
cd aura_frontend
pnpm install
```

### 2. Environment Setup

Create a `.env` file in the root directory and configure the required environment variables:

```env
NEXT_PUBLIC_BACKEND_URL=https://your-backend-api.com/
NEXT_PUBLIC_UPLOADCARE_PUBLIC_KEY=your_uploadcare_public_key
UPLOADCARE_SECRET_KEY=your_uploadcare_secret_key
```

### 3. Running Development Server

Launch the development server:

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to view the application.

---

## 📜 Available Scripts

In the project directory, you can run:

| Command | Description |
| :--- | :--- |
| `pnpm dev` | Starts the development server with Hot Module Replacement |
| `pnpm build` | Compiles and optimizes the app for production |
| `pnpm start` | Runs the production build server |
| `pnpm lint` | Runs ESLint to check for code formatting and syntax errors |

---

## 📄 License

This project is private. All rights reserved.
