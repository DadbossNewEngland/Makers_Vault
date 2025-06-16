# Maker's Vault 🏛️

A gamified content subscription platform where creators can monetize their content and users collect digital treasures through purchases and engagement.

## ✨ Features

### For Users
- **Treasure Collection System**: Earn digital treasures (coins, gems, artifacts, crowns) through content purchases
- **Loyalty Points**: 10x multiplier system with tier progression (Bronze → Silver → Gold → Platinum → Diamond)
- **Vault Subscriptions**: Monthly, yearly, or lifetime access to creator content libraries
- **Gamified Dashboard**: Track progress, achievements, and treasure collection
- **Real-time Updates**: Live dashboard updates powered by Convex

### For Creators
- **Content Vaults**: Organize content into themed libraries with subscription tiers
- **Multiple Access Levels**: Public, Premium, and Exclusive content tiers
- **Revenue Tracking**: Monitor subscriptions and content performance
- **Verified Creator System**: Build trust with verification badges

### Technical Features
- **Secure Authentication**: Username/password auth with Convex Auth
- **Real-time Database**: Powered by Convex for instant updates
- **Responsive Design**: Beautiful UI with Tailwind CSS and glass morphism
- **Type Safety**: Full TypeScript implementation
- **Scalable Architecture**: Modular component structure

## 🚀 Tech Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS, Vite
- **Backend**: Convex (Database, Auth, Real-time, Functions)
- **Authentication**: Convex Auth
- **Styling**: Tailwind CSS with custom animations
- **State Management**: Convex React hooks
- **Notifications**: Sonner toast library

## 🏗️ Project Structure

```
src/
├── components/
│   ├── features/
│   │   ├── dashboard/     # User dashboard components
│   │   ├── gamification/  # Loyalty and rewards system
│   │   ├── treasure/      # Treasure display and management
│   │   └── vault/         # Vault browsing and subscription
│   └── ui/                # Reusable UI components
├── types/                 # TypeScript type definitions
└── lib/                   # Utility functions

convex/
├── schema.ts             # Database schema
├── auth.ts              # Authentication configuration
├── vaults.ts            # Vault management functions
├── content.ts           # Content and purchase logic
├── creators.ts          # Creator profile management
└── seed.ts              # Sample data seeding
```

## 🎮 Gamification System

### Treasure Types
- **🪙 Coins**: Common treasures from any purchase
- **💎 Gems**: Rare treasures from larger purchases ($50+)
- **🏺 Artifacts**: Epic treasures from premium purchases ($100+)
- **👑 Crowns**: Legendary treasures from special events

### Loyalty Tiers
1. **🥉 Bronze Explorer** (0+ points)
2. **🥈 Silver Adventurer** (1,000+ points)
3. **🥇 Gold Collector** (5,000+ points)
4. **💎 Platinum Master** (15,000+ points)
5. **👑 Diamond Legend** (50,000+ points)

## 🛠️ Setup & Installation

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Convex account

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/makers-vault.git
   cd makers-vault
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up Convex**
   ```bash
   npx convex dev
   ```
   Follow the prompts to create a new Convex project or link to existing one.

4. **Seed sample data** (optional)
   ```bash
   npx convex run seed:seedSampleData
   ```

5. **Start development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   Navigate to `http://localhost:5173`

## 🔧 Environment Variables

Create a `.env.local` file in the root directory:

```env
# Convex
VITE_CONVEX_URL=your_convex_deployment_url

# Optional: Custom API keys
OPENAI_API_KEY=your_openai_key
STRIPE_SECRET_KEY=your_stripe_key
```

## 📊 Database Schema

### Core Tables
- **users**: User authentication and profiles
- **creators**: Creator profiles and verification
- **vaults**: Content subscription containers
- **libraries**: Organized content collections within vaults
- **content**: Individual videos/materials
- **vaultSubscriptions**: User subscription records
- **purchases**: Individual content purchases
- **treasures**: Gamification rewards
- **pointTransactions**: Loyalty point tracking

## 🎯 Key Features Implementation

### Real-time Treasure Collection
```typescript
// Automatic treasure generation on purchase
const generateTreasureRewards = async (userId, purchaseId, amount) => {
  const treasures = [
    { type: "coin", rarity: "common", value: Math.floor(amount) },
    // Bonus treasures based on purchase amount
  ];
  // Cryptographically secure treasure minting
};
```

### Loyalty Point System
```typescript
// 10x multiplier on all purchases
const loyaltyPointsEarned = Math.floor(amount * 10);
```

### Access Control
```typescript
// Secure content access verification
const verifyContentAccess = async (userId, contentId) => {
  // Check direct purchase OR active vault subscription
  return isPurchased || hasActiveSubscription;
};
```

## 🚀 Deployment

### Deploy to Vercel
```bash
npm run build
npx vercel --prod
```

### Deploy Convex Backend
```bash
npx convex deploy
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [Convex](https://convex.dev) for real-time backend
- UI components styled with [Tailwind CSS](https://tailwindcss.com)
- Icons from [Heroicons](https://heroicons.com)
- Treasure-themed design inspired by gaming mechanics

## 📞 Support

If you have any questions or need help with setup, please open an issue or contact the maintainers.

---

**Made with ❤️ for creators and treasure hunters alike!**
