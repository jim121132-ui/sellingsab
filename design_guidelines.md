# Design Guidelines: Brainrot Marketplace

## Design Approach
Reference-based approach inspired by **sellsab.com** - a modern gaming marketplace with vibrant gradients, clean stats displays, and trust-building elements. We'll adapt this aesthetic for a TikTok brainrot selling platform with Discord integration.

## Core Design Elements

### Typography
- **Primary Font**: Inter or DM Sans (Google Fonts)
- **Headings**: Bold (700), sizes: text-4xl to text-6xl for hero, text-2xl to text-3xl for sections
- **Body**: Regular (400), text-base to text-lg
- **Stats/Numbers**: Bold (700), text-3xl to text-5xl
- **Buttons**: Semibold (600), text-base

### Layout System
- **Container**: max-w-7xl mx-auto px-4 to px-8
- **Spacing Scale**: Tailwind units 4, 6, 8, 12, 16, 20, 24 (e.g., py-20, gap-8, mb-12)
- **Section Padding**: py-16 on mobile, py-24 on desktop
- **Grid Systems**: grid-cols-1 md:grid-cols-2 lg:grid-cols-4 for stats, lg:grid-cols-3 for reviews

### Component Library

**Hero Section**
- Full-width gradient background (purple to blue to pink gradient)
- Centered content with h-screen or min-h-[600px]
- Main heading: "Sell Your Brainrots Safely In Steal A Brainrot"
- Subheading: "The #1 Marketplace To Sell Your Brainrots."
- Primary CTA: Large blue Discord button with bot emoji (bg-[#5865F2])
- Top-right badge: "Trusted By Many Users" with pill-shaped background

**Stats Dashboard**
- 4-column grid (stacks on mobile): Happy Customers (263), Money Paid Out ($29,860), Sales Today (10), Total Paid Today ($600)
- Card-based design with gradient borders or subtle shadows
- Large numbers with small labels beneath
- Optional: Subtle animations or counters

**Form Section**
- Multi-step form flow with smooth transitions
- Step 1: Large "Sell Your Brainrots" button (prominent, gradient or solid blue)
- Step 2: Input field "Type your brainrot name" with example text "Los Combinasiones"
- Step 3: Input field "Paste your TikTok user"
- Step 4: Input field "Price" with currency symbol
- Submit button: Gradient or blue, sends to Discord webhook
- Form container: Centered, max-w-md to max-w-lg, with card styling

**Reviews Section**
- 3-column grid on desktop (stacks on mobile)
- 5 review cards total with testimonials:
  - "legit"
  - "nice, fast service!"
  - "I 100% Reccomend"
  - "great service"
  - "Ill Be Using Again!"
- Each card: User avatar (generated initial), username, 5 gold star rating, testimonial text
- Card styling: Subtle background, rounded corners, padding p-6

**Discord Button**
- Blue background (#5865F2 - Discord brand color)
- Discord bot emoji icon before text
- Text: "Join The Discord"
- Rounded-full or rounded-lg
- Links to: https://discord.gg/G23869hSpV
- Hover state: Slightly darker blue

### Visual Style
- **Gradients**: Purple-blue-pink for hero, subtle gradients for cards
- **Shadows**: Soft drop shadows (shadow-lg, shadow-xl) on cards
- **Borders**: Rounded corners (rounded-xl, rounded-2xl)
- **Glass Effects**: Optional backdrop-blur on certain elements
- **Accent Colors**: Discord blue (#5865F2) for primary actions

### Navigation
- Clean, minimal top navigation
- Logo/site name on left
- Discord button on right
- No login/get started buttons

### Animations
- Minimal and purposeful only:
  - Smooth form step transitions (fade or slide)
  - Hover states on buttons (scale or brightness change)
  - Optional: Stat counter animations on load

## Images
- **Hero Background**: Abstract gradient or geometric pattern, can use CSS gradients instead of image
- **User Avatars**: Generated initials in colored circles for review section
- **Icons**: Discord bot emoji (can use Unicode: 🤖 or emoji library)

This design creates a trustworthy, modern marketplace that balances sellsab.com's clean aesthetic with the playful "brainrot" theme while maintaining professional credibility through stats, reviews, and clear CTAs.