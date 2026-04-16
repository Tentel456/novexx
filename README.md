# NOVEX - Crypto Exchange Platform (Next.js)

Modern crypto exchange platform built with Next.js 14, React, TypeScript, Tailwind CSS, and Supabase.

## ⚡ Quick Start

**New to the project? Start here:** 👉 [QUICK_START.md](QUICK_START.md)

For detailed setup instructions, continue reading below.

## 🚀 Installation Guide

### Prerequisites

- Node.js 18+ installed
- npm or yarn package manager

### Installation

1. **Install dependencies:**
```bash
npm install
# or
yarn install
```

2. **Setup environment variables:**

Create a `.env.local` file in the root directory:

```env
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url_here
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key_here
NEXT_PUBLIC_SITE_URL=http://localhost:3000
```

Get your Supabase credentials from [supabase.com](https://supabase.com)

3. **Run development server:**
```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 📁 Project Structure

```
├── app/                    # Next.js 14 App Router
│   ├── auth/              # Authentication pages
│   │   ├── page.tsx       # Auth page
│   │   └── callback/      # OAuth callback
│   ├── p2p/               # P2P trading platform
│   │   └── page.tsx       # P2P trading page
│   ├── layout.tsx         # Root layout
│   ├── page.tsx           # Home page
│   └── globals.css        # Global styles
├── components/            # React components
│   ├── layout/           # Layout components
│   │   └── Header.tsx    # Main header/navigation
│   ├── home/             # Home page components
│   │   ├── Hero.tsx      # Hero section
│   │   ├── Features.tsx  # Features section
│   │   └── Statistics.tsx # Statistics section
│   ├── auth/             # Auth components
│   │   └── AuthForm.tsx  # Main auth form
│   └── p2p/              # P2P components
│       ├── P2PHeader.tsx # P2P navigation
│       ├── P2PFilters.tsx # Filters & selects
│       └── P2PTradeList.tsx # Trade offers list
├── lib/                   # Utilities
│   └── supabase/         # Supabase clients
│       ├── client.ts     # Client-side
│       └── server.ts     # Server-side
├── public/               # Static assets
│   ├── assets/          # Images, logos
│   ├── first-page/      # Home page images
│   └── p2p-page/        # P2P page images
├── middleware.ts         # Auth middleware
└── package.json         # Dependencies

```

## 🎯 Pages

- **/** - Home page (landing)
- **/auth** - Authentication (login/signup)
- **/p2p** - P2P Trading platform

## 🔑 Features

- ✅ **Modern Stack**: Next.js 14, React 18, TypeScript
- ✅ **Home Page**: 
  - Hero section with CTA
  - Features showcase
  - Live crypto statistics
  - Responsive design
- ✅ **Authentication**: 
  - Email Magic Link (passwordless)
  - Email/Password login
  - Google OAuth
  - Protected routes
- ✅ **P2P Trading**:
  - Buy/Sell cryptocurrency interface
  - Multiple crypto support (USDT, ETH, BTC)
  - Payment method filters
  - Real-time trade offers
  - Mobile-responsive design
- ✅ **Styling**: Tailwind CSS
- ✅ **Type Safety**: Full TypeScript support
- ✅ **Server Components**: Optimized performance
- ✅ **Responsive Design**: Mobile-first approach

## 🛠️ Tech Stack

- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Authentication**: Supabase Auth
- **Database**: Supabase (PostgreSQL)
- **Deployment**: Vercel (recommended)

## 📝 Supabase Setup

1. Create a project at [supabase.com](https://supabase.com)
2. Get your API keys from Settings → API
3. Configure authentication providers:
   - Enable Email provider
   - Setup Google OAuth (optional)
4. Add redirect URLs in Auth settings:
   ```
   http://localhost:3000/auth/callback
   https://yourdomain.com/auth/callback
   ```

Detailed setup guide: `auth-page/SUPABASE_SETUP.md`

## 🚢 Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Import project in [Vercel](https://vercel.com)
3. Add environment variables
4. Deploy!

### Other Platforms

The app can be deployed to any platform that supports Next.js:
- Netlify
- Railway
- AWS Amplify
- Self-hosted

## 📦 Scripts

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run start    # Start production server
npm run lint     # Run ESLint
```

## 🎨 Customization

### Fonts

The project uses Clash Display font. To add it:

1. Download Clash Display font (Variable or Regular)
2. Place `ClashDisplay-Variable.woff2` in the `/fonts/` directory
3. The font is already configured in `app/layout.tsx`

Alternative: Use Gilroy font (already included) by updating the layout configuration.

### Colors

Edit `tailwind.config.ts` to customize colors:

```typescript
colors: {
  primary: "#00BFFF",  // Main brand color
  secondary: "#E8E8E8", // Background color
}
```

### Logo

Replace `/public/assets/logo/novex_logo.png` with your logo.

## 🐛 Troubleshooting

### Supabase Connection Issues

- Check if environment variables are set correctly
- Verify Supabase project is active
- Check redirect URLs in Supabase dashboard

### OAuth Not Working

- Ensure redirect URLs are configured in Supabase
- Check Google OAuth credentials
- Verify site URL in environment variables

### Build Errors

```bash
# Clear cache and reinstall
rm -rf .next node_modules
npm install
npm run dev
```

### Images Not Loading

Make sure all images are in the `/public` directory and paths are correct.

## 📚 Learn More

- [Next.js Documentation](https://nextjs.org/docs)
- [Supabase Documentation](https://supabase.com/docs)
- [Tailwind CSS](https://tailwindcss.com/docs)
- [TypeScript](https://www.typescriptlang.org/docs)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is private and proprietary.
