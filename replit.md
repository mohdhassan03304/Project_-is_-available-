# Overview

This is a full-stack web application built with React frontend and Express backend, featuring a todo list application. The project uses TypeScript throughout and follows a modern development stack with Vite for frontend bundling, Drizzle ORM for database operations, and shadcn/ui for the component library. The application currently implements local storage for task persistence but is configured to support PostgreSQL database integration.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized production builds
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: React hooks with local storage persistence via custom useLocalStorage hook
- **UI Components**: shadcn/ui component library built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming support
- **Data Fetching**: TanStack Query (React Query) for server state management

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Development**: tsx for TypeScript execution during development
- **Build Process**: esbuild for production bundling
- **Storage Interface**: Abstracted storage layer with in-memory implementation (MemStorage class)
- **Middleware**: Custom logging middleware for API requests

## Data Storage
- **Current**: Local storage in browser for task persistence
- **Configured**: Drizzle ORM with PostgreSQL support via Neon Database
- **Schema**: Shared TypeScript schemas using Zod for validation
- **Migration**: Drizzle Kit for database schema management

## Development & Build Setup
- **Monorepo Structure**: Client and server code in separate directories with shared schemas
- **Path Aliases**: TypeScript path mapping for clean imports (@/, @shared/, @assets/)
- **Development Server**: Vite dev server with HMR and Express API proxy
- **Production**: Static file serving from Express with client-side routing support

## Key Design Decisions

### Modular Architecture
The application separates concerns with a clear client/server/shared structure. Shared schemas ensure type safety between frontend and backend, while the storage interface allows easy switching between storage implementations.

### UI Component Strategy
Uses shadcn/ui for consistent, accessible components built on Radix UI. This provides a solid foundation with customizable styling via Tailwind CSS and CSS variables for theming.

### State Management Approach
Combines React Query for server state with local storage for client-side persistence. This hybrid approach provides offline capability while preparing for server-side data synchronization.

### Development Experience
Prioritizes fast feedback loops with Vite's HMR, TypeScript for type safety, and a unified build process that handles both frontend and backend code.

# External Dependencies

## Database & ORM
- **Neon Database**: PostgreSQL-compatible serverless database (@neondatabase/serverless)
- **Drizzle ORM**: Type-safe database toolkit with PostgreSQL dialect
- **Drizzle Kit**: Schema management and migration tool

## UI & Styling
- **Radix UI**: Comprehensive collection of accessible UI primitives
- **Tailwind CSS**: Utility-first CSS framework with PostCSS processing
- **Lucide React**: Modern icon library for React applications
- **Class Variance Authority**: Utility for creating component variants

## Development Tools
- **Vite**: Fast build tool with React plugin and runtime error overlay
- **TypeScript**: Static type checking across the entire application
- **ESBuild**: Fast JavaScript bundler for production builds
- **tsx**: TypeScript execution for development server

## Data & Validation
- **Zod**: Schema validation library for runtime type checking
- **date-fns**: Modern date utility library for formatting and manipulation
- **TanStack Query**: Powerful data synchronization for React applications

## Routing & Navigation
- **Wouter**: Minimalist routing library for React applications
- **React Hook Form**: Performant forms library with validation support

## Replit Integration
- **Replit Plugins**: Cartographer and runtime error modal for enhanced development experience
- **Development Banner**: Replit development environment indicator