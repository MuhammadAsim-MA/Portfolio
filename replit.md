# Muhammad Asim Portfolio - Full Stack Application

## Overview

This is a modern full-stack portfolio application built for Muhammad Asim, a Data Analyst & ML Engineer. The application showcases professional experience, skills, projects, and provides a contact form for potential clients and employers. The portfolio has been redesigned using the Parallelism template with a yellow and grey color scheme and includes comprehensive experience and qualification sections.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **UI Framework**: Shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **State Management**: React Query (@tanstack/react-query) for server state
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (@neondatabase/serverless)
- **Session Management**: Connect-pg-simple for PostgreSQL session storage
- **Development**: Hot module replacement via Vite integration

### Component Structure (Parallelism Design)
- **Hero Section**: Centered profile with photo, introduction, and contact details
- **Experience Section**: Professional timeline with detailed achievements and responsibilities
- **Education Section**: Academic qualifications with MS AI and BE Electronics degrees
- **Skills Section**: Technical capabilities organized by category with visual icons
- **Projects Section**: Featured work displayed in masonry grid layout with modal popups
- **Footer**: Contact information and social links

## Key Components

### Database Schema
- **Users Table**: Basic user authentication structure with id, username, and password
- **Schema Location**: `/shared/schema.ts` using Drizzle ORM with PostgreSQL dialect
- **Migrations**: Managed through Drizzle Kit with migrations stored in `/migrations`

### API Routes
- **Contact Endpoint**: `/api/contact` - Handles contact form submissions
- **User Management**: Basic CRUD operations for users (authentication ready)

### UI Components
- **Design System**: Shadcn/ui components with consistent styling
- **Responsive Design**: Mobile-first approach with Tailwind breakpoints
- **Accessibility**: ARIA labels and keyboard navigation support
- **Toast Notifications**: User feedback system for form submissions

## Data Flow

1. **Client Requests**: Browser requests handled by Vite dev server or static files in production
2. **API Calls**: Frontend makes requests to Express server at `/api/*` endpoints
3. **Database Operations**: Server uses Drizzle ORM to interact with PostgreSQL
4. **Response Handling**: Data returned to client and managed by React Query
5. **State Updates**: UI updates automatically based on server state changes

## External Dependencies

### Frontend Dependencies
- **UI Components**: Radix UI primitives for accessible components
- **Icons**: Lucide React for consistent iconography
- **Date Handling**: date-fns for date formatting
- **Animation**: CSS transitions and Tailwind animations
- **Form Validation**: Zod for schema validation

### Backend Dependencies
- **Database**: Neon PostgreSQL serverless database
- **ORM**: Drizzle ORM with Zod integration
- **Development Tools**: tsx for TypeScript execution, esbuild for production builds

### Development Tools
- **Replit Integration**: Vite plugins for Replit environment
- **Error Handling**: Runtime error modal in development
- **Code Mapping**: Cartographer for better debugging

## Deployment Strategy

### Development
- **Command**: `npm run dev` - Starts development server with hot reloading
- **Environment**: NODE_ENV=development with Vite dev server integration
- **Database**: Uses DATABASE_URL environment variable for connection

### Production Build
- **Frontend**: `vite build` - Optimized static assets in `/dist/public`
- **Backend**: `esbuild` - Bundled server code in `/dist/index.js`
- **Database**: `npm run db:push` - Applies schema changes to production database

### Environment Configuration
- **Database URL**: Required environment variable for PostgreSQL connection
- **Static Files**: Served from `/dist/public` in production
- **Server**: Express server serves both API and static files

### Key Features
- **Responsive Design**: Works on all device sizes
- **SEO Friendly**: Proper meta tags and semantic HTML
- **Performance Optimized**: Code splitting and lazy loading
- **Contact Form**: Functional contact form with validation
- **Professional Portfolio**: Comprehensive showcase of skills and experience

The application follows modern web development practices with a clean separation of concerns, type safety throughout the stack, and a focus on user experience and performance.