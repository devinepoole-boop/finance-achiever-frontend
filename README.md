# Finance Achiever Frontend

React TypeScript frontend application for the Finance Achiever social media fintech platform.

## Features

- **Modern React Architecture**: React 18 with TypeScript and Vite
- **UI Components**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom themes and animations
- **State Management**: TanStack Query for server state
- **Routing**: Wouter for lightweight routing
- **Payment Integration**: Stripe Elements for secure payments
- **Charts & Visualization**: Chart.js and Recharts for financial data
- **Mobile Responsive**: Optimized for all device sizes

## Tech Stack

- **Framework**: React 18.3.1 with TypeScript 5.6.3
- **Build Tool**: Vite 6.3.5 with hot reload
- **UI Library**: Radix UI primitives + shadcn/ui
- **Styling**: Tailwind CSS 3.4.17 with animations
- **HTTP Client**: Axios with TanStack Query
- **Forms**: React Hook Form with Zod validation
- **Icons**: Lucide React + React Icons

## Getting Started

### Prerequisites
- Node.js 18+ and npm 8+
- Backend API running (see backend README)

### Installation
```bash
npm install
```

### Environment Setup
```bash
cp .env.example .env
```

Configure your environment variables:
- `VITE_API_URL`: Backend API URL (http://localhost:5000 for local development)
- `VITE_STRIPE_PUBLISHABLE_KEY`: Stripe publishable key

### Development
```bash
npm run dev
```
Runs on http://localhost:3000 with hot reload

### Production Build
```bash
npm run build
npm run preview
```

## Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── ui/             # shadcn/ui components
│   └── ...             # Custom components
├── hooks/              # Custom React hooks
├── lib/               # Utilities and configurations
│   ├── queryClient.ts # API client setup
│   ├── stripe.ts      # Stripe configuration
│   └── utils.ts       # Helper functions
├── pages/             # Page components
└── utils/             # Utility functions
```

## Key Components

### Authentication
- Replit OIDC integration
- Local email/password authentication
- Session-based authentication with httpOnly cookies

### Course Management
- 37 expert-led video courses
- Progress tracking and completion
- Interactive learning experiences

### Social Features
- Community creation and management
- Post creation with multimedia support
- Like/comment functionality
- User profiles and interactions

### Financial Tools
- Account tracking and transaction management
- Budget creation and monitoring
- Goal setting and progress tracking
- Interactive charts and analytics

### Payment Processing
- Stripe integration for subscriptions
- Secure payment handling
- Multiple subscription tiers

## Deployment Options

### Vercel (Recommended)
```bash
npm install -g vercel
vercel deploy
```

### Netlify
```bash
npm run build
# Drag dist folder to Netlify dashboard
```

### Static Hosting
```bash
npm run build
# Upload dist/ folder to any static host
```

## Environment Variables

### Development
```env
VITE_API_URL=http://localhost:5000
VITE_STRIPE_PUBLISHABLE_KEY=pk_test_...
```

### Production
```env
VITE_API_URL=https://your-backend-api.com
VITE_STRIPE_PUBLISHABLE_KEY=pk_live_...
```

## Performance Optimizations

- **Code Splitting**: Automatic chunking for vendors
- **Tree Shaking**: Unused code elimination
- **Asset Optimization**: Image compression and lazy loading
- **Caching**: Service worker for offline support
- **Bundle Analysis**: Optimized dependency loading

## API Integration

The frontend communicates with the backend via REST API:
- **Authentication**: `/api/auth/*`
- **Courses**: `/api/courses/*`
- **Social**: `/api/posts/*`, `/api/communities/*`
- **Financial**: `/api/financial/*`
- **AI Tutoring**: `/api/ai/*`
- **Payments**: `/api/stripe/*`

## Build Configuration

Configured for optimal production deployment:
- Modern browser targets
- CSS purging and minification
- Asset optimization
- Environment variable injection
- Source map generation (development only)

## Contributing

1. Follow React/TypeScript best practices
2. Use provided UI components from shadcn/ui
3. Maintain consistent styling with Tailwind
4. Add proper TypeScript types
5. Test all payment flows thoroughly

## License

MIT License - see LICENSE file for details