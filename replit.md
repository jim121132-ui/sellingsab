# Brainrot Marketplace

## Overview

A TikTok brainrot content marketplace web application inspired by sellsab.com. Users can submit their brainrot content for sale through a multi-step form that sends submissions to a Discord webhook. The application features a modern gaming marketplace aesthetic with vibrant gradients, stats displays, and customer reviews to build trust.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter (lightweight client-side routing)
- **State Management**: TanStack React Query for server state
- **Styling**: Tailwind CSS with shadcn/ui component library (New York style)
- **Form Handling**: React Hook Form with Zod validation
- **Build Tool**: Vite with path aliases (@/, @shared/, @assets/)

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **API Pattern**: RESTful endpoints under /api prefix
- **Server Structure**: 
  - `server/index.ts` - Entry point, middleware setup
  - `server/routes.ts` - API route definitions
  - `server/storage.ts` - In-memory data storage interface
  - `server/vite.ts` - Development server with HMR
  - `server/static.ts` - Production static file serving

### Data Layer
- **ORM**: Drizzle ORM with PostgreSQL dialect
- **Schema Validation**: drizzle-zod for type-safe schemas
- **Schema Location**: `shared/schema.ts` (shared between client/server)
- **Current Storage**: In-memory (MemStorage class) with interface for future database integration
- **Database Config**: drizzle.config.ts configured for PostgreSQL when DATABASE_URL is available

### Build System
- **Development**: Vite dev server with HMR through custom server integration
- **Production**: 
  - Client: Vite build to `dist/public`
  - Server: esbuild bundling to `dist/index.cjs`
  - Selective dependency bundling for faster cold starts

## External Dependencies

### Third-Party Services
- **Discord Webhook**: Receives brainrot submissions via DISCORD_WEBHOOK_URL environment variable
- **Google Fonts**: DM Sans and Inter font families loaded via CDN

### Database
- **PostgreSQL**: Configured via DATABASE_URL environment variable (optional, currently using in-memory storage)

### Key NPM Packages
- **UI Components**: Full shadcn/ui component suite with Radix UI primitives
- **Icons**: Lucide React, react-icons (for Discord icon)
- **Utilities**: clsx, tailwind-merge, class-variance-authority, date-fns
- **Replit Plugins**: Runtime error overlay, cartographer, dev banner (development only)