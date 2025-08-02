# replit.md

## Overview

RoAi is a comprehensive AI-powered business assistant platform for e-commerce businesses that leverages OpenAI's GPT-4o to create marketing content including product descriptions, social media ads, and email campaigns. The platform features three pricing tiers (Free, Pro, Diamond) with integrated marketplace functionality, personalized AI assistants (Saad and Hadeel), and comprehensive bilingual support (Arabic/English). The platform includes a dashboard for tracking content generation statistics, business profile management, AI-powered content creation with customizable parameters, plus personalized AI chat assistants for real-time business advice and support.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **Routing**: Wouter for client-side routing
- **UI Components**: Radix UI primitives with shadcn/ui component library
- **Styling**: TailwindCSS with CSS custom properties for theming
- **State Management**: TanStack Query for server state management and caching
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Database ORM**: Drizzle ORM with PostgreSQL dialect
- **API Design**: RESTful API with structured error handling
- **Development Server**: Custom Vite integration for SSR-like development experience
- **Storage Layer**: Abstracted storage interface with in-memory implementation for development

### Data Storage Solutions
- **Primary Database**: PostgreSQL (configured via Drizzle)
- **Connection**: Neon Database serverless PostgreSQL
- **Schema Management**: Drizzle migrations with TypeScript schema definitions
- **Development Storage**: In-memory storage implementation for rapid prototyping

### Database Schema Design
- **Businesses Table**: Core business entity with profile information
- **Content Generated Table**: Tracks all AI-generated content with metadata
- **Activities Table**: Audit trail for user actions and system events
- **Relationships**: Foreign key constraints linking content and activities to businesses

### Authentication and Authorization
- **Session Management**: Express sessions with PostgreSQL session store (connect-pg-simple)
- **Security**: CORS handling and request logging middleware
- **Development**: No authentication barriers for rapid development

### Content Generation Pipeline
- **AI Integration**: OpenAI GPT-4o API with structured JSON responses
- **Prompt Engineering**: Dynamic prompt building based on content type and business context
- **Content Types**: Product descriptions, social media ads, email campaigns
- **Metadata Tracking**: Stores generation parameters and response analytics
- **Personalized AI Assistants**: Saad (professional/direct) and Hadeel (friendly/understanding)

### Pricing Structure and Marketplace
- **Free Plan**: Access to marketplace services with 15% platform fee on purchases
- **Pro Plan ($49/month)**: AI tools + marketplace access + personal AI assistant
- **Diamond Plan ($149/month)**: Unlimited AI tools + advanced features + dedicated support
- **Marketplace Integration**: Agencies, freelancers, and AI tools with revenue sharing model

### API Architecture
- **RESTful Endpoints**: CRUD operations for businesses, content, and activities
- **Error Handling**: Centralized error middleware with structured responses
- **Request/Response Flow**: JSON-based communication with validation
- **Statistics Aggregation**: Real-time dashboard metrics calculation

## External Dependencies

### AI Services
- **OpenAI API**: GPT-4o model for content generation with JSON mode
- **Configuration**: Environment variable-based API key management

### Database Services
- **Neon Database**: Serverless PostgreSQL hosting
- **Connection**: DATABASE_URL environment variable configuration

### Development Tools
- **Replit Integration**: Custom Vite plugin for development environment
- **Error Overlay**: Runtime error modal for development debugging
- **Hot Module Replacement**: Vite HMR with Express middleware integration

### UI Component Libraries
- **Radix UI**: Accessible React primitives for complex UI components
- **Lucide React**: Icon library for consistent iconography
- **Embla Carousel**: Carousel component for content display

### Utility Libraries
- **Zod**: Runtime type validation and schema definition
- **Class Variance Authority**: Type-safe CSS class composition
- **date-fns**: Date manipulation and formatting
- **nanoid**: Unique ID generation for entities

### Session and Storage
- **connect-pg-simple**: PostgreSQL session store for Express sessions
- **Express Session**: Server-side session management

### Build and Development
- **TypeScript**: Static type checking across frontend and backend
- **ESBuild**: Fast JavaScript bundling for production builds
- **PostCSS**: CSS processing with Autoprefixer