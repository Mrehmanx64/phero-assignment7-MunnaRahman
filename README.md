<div align="center">
  <img src="./public/logo-icon.png" alt="BazarDor Logo" width="120" height="120">
  
  # 🛒 বাজার দর (BazarDor)
  
  ### প্রয়োজনীয় পণ্যের দাম এক নজরে
  
  [![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen?style=for-the-badge)](https://phero-assignment7-munna-rahman.vercel.app)
  [![Next.js](https://img.shields.io/badge/Next.js-16.4.0-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
  [![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
  [![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

  <p align="center">
    A comprehensive web application for tracking and displaying daily market prices of essential commodities in Bangladesh.
  </p>
</div>

---

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [Project Structure](#project-structure)
- [Screenshots](#screenshots)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 About

**বাজার দর (BazarDor)** is designed to help users track daily price fluctuations of essential goods like rice, fish, vegetables, and more. It provides market insights with real-time data, enabling users to make informed purchasing decisions based on up-to-date price trends.

### Why BazarDor?

- 📊 **Real-time Updates**: Track daily price changes with visual indicators
- 🔐 **Secure Authentication**: Multiple sign-in options for user convenience
- 📱 **Responsive Design**: Works seamlessly on all devices
- 🎨 **Intuitive UI**: Clean and user-friendly interface
- 🚀 **Fast Performance**: Built with Next.js for optimal speed

---

## ✨ Features

### 🎯 Core Features

1. **Real-time Price Ticker**
   - Infinite scrolling marquee displaying current market prices
   - Visual indicators (▲/▼) for price changes
   - Bengali numerals support

2. **Comprehensive Product Tracking**
   - Top 6 price risers section
   - Top 6 price fallers section
   - Complete product catalog with responsive grid layout

3. **Advanced Product Details** 🔒
   - Protected routes requiring authentication
   - Detailed market summaries
   - Price trends analysis
   - Market-wise price breakdown

4. **Category-based Browsing**
   - Filter products by category (চাল, ডাল, তেল, মাছ, মাংস, সবজি, মসলা)
   - Sort options: Default, Price (Low to High), Price (High to Low)
   - Smart Bengali numeral sorting

5. **Secure Authentication & User Profile**
   - Email/Password authentication
   - Google OAuth integration
   - GitHub OAuth integration
   - Profile management with name and avatar updates
   - Protected routes with session persistence

### 🎨 UI/UX Features

- Skeleton loading states for better UX
- Toast notifications for user feedback
- 404 page for invalid routes
- Mobile-first responsive design
- Smooth animations and transitions

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **Next.js 16.4.0** | React framework with App Router |
| **TypeScript** | Type-safe development |
| **Tailwind CSS** | Utility-first CSS framework |
| **HeroUI** | Modern UI component library |
| **BetterAuth** | Authentication solution |
| **MongoDB** | Database for user data |
| **React Icons** | Icon library |
| **React Toastify** | Toast notifications |
| **Vercel** | Deployment platform |

---

## 🚀 Getting Started

### Prerequisites

- Node.js 20.x or higher
- npm or yarn
- MongoDB Atlas account
- Google OAuth credentials
- GitHub OAuth credentials

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Mrehmanx64/phero-assignment7-MunnaRahman.git
   cd phero-assignment7-MunnaRahman
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   BETTER_AUTH_DB_URL=your_mongodb_connection_string
   BETTER_AUTH_SECRET=your_secret_key
   BETTER_AUTH_GOOGLE_CLIENT_ID=your_google_client_id
   BETTER_AUTH_GOOGLE_CLIENT_SECRET=your_google_client_secret
   BETTER_AUTH_GITHUB_CLIENT_ID=your_github_client_id
   BETTER_AUTH_GITHUB_CLIENT_SECRET=your_github_client_secret
   NEXT_PUBLIC_BETTER_AUTH_URL=http://localhost:3000
   ```

4. **Run the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

---

## 🔐 Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `BETTER_AUTH_DB_URL` | MongoDB connection string | ✅ |
| `BETTER_AUTH_SECRET` | Secret key for session encryption | ✅ |
| `BETTER_AUTH_GOOGLE_CLIENT_ID` | Google OAuth Client ID | ✅ |
| `BETTER_AUTH_GOOGLE_CLIENT_SECRET` | Google OAuth Client Secret | ✅ |
| `BETTER_AUTH_GITHUB_CLIENT_ID` | GitHub OAuth Client ID | ✅ |
| `BETTER_AUTH_GITHUB_CLIENT_SECRET` | GitHub OAuth Client Secret | ✅ |
| `NEXT_PUBLIC_BETTER_AUTH_URL` | Base URL for authentication | ✅ |

---

## 📁 Project Structure

```
├── public/
│   ├── logo-icon.png
│   └── bazar-hero.png
├── src/
│   ├── app/
│   │   ├── (auth)/
│   │   │   ├── profile/
│   │   │   ├── sign-in/
│   │   │   └── sign-up/
│   │   ├── api/
│   │   │   └── auth/
│   │   ├── category/
│   │   │   └── [categoryId]/
│   │   ├── product/
│   │   │   └── [slug]/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── not-found.tsx
│   ├── components/
│   │   ├── AllProducts.tsx
│   │   ├── AuthControls.tsx
│   │   ├── Banner.tsx
│   │   ├── Footer.tsx
│   │   ├── Header.tsx
│   │   ├── Marquee.tsx
│   │   ├── NavLinks.tsx
│   │   ├── PriceIncrease.tsx
│   │   └── PriceDecrease.tsx
│   └── lib/
│       ├── auth.ts
│       └── auth-client.ts
├── .env
├── .gitignore
├── next.config.ts
├── package.json
├── tailwind.config.ts
└── tsconfig.json
```

---

## 📸 Screenshots

### Home Page
Display of price risers, fallers, and all products with real-time price updates.

### Product Details (Protected)
Detailed market analysis and price trends for authenticated users.

### Category Page
Filtered product listing with advanced sorting capabilities.

### Authentication
Secure sign-in/sign-up with multiple OAuth providers.

---

## 🚢 Deployment

### Deploy to Vercel

1. **Push your code to GitHub**
   ```bash
   git add .
   git commit -m "Ready for deployment"
   git push origin main
   ```

2. **Import to Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Click "Import Project"
   - Select your repository

3. **Configure Environment Variables**
   - Add all environment variables from `.env`
   - Update `NEXT_PUBLIC_BETTER_AUTH_URL` to your Vercel domain

4. **Deploy**
   - Click "Deploy"
   - Wait for the build to complete

5. **Update OAuth Redirect URIs**
   - Google: `https://your-domain.vercel.app/api/auth/callback/google`
   - GitHub: `https://your-domain.vercel.app/api/auth/callback/github`

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Munna Rahman**

- GitHub: [@Mrehmanx64](https://github.com/Mrehmanx64)
- Project Link: [https://github.com/Mrehmanx64/phero-assignment7-MunnaRahman](https://github.com/Mrehmanx64/phero-assignment7-MunnaRahman)

---

## 🙏 Acknowledgments

- [Programming Hero](https://www.programming-hero.com/) for the assignment
- API Provider: [OpenAPI Programming Hero](https://openapi.programming-hero.com/api/bazardor)
- Icons from [React Icons](https://react-icons.github.io/react-icons/)

---

<div align="center">
  Made with ❤️ by Munna Rahman
  
  ⭐ Star this repository if you found it helpful!
</div>
