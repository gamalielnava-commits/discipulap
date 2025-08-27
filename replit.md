# Overview

This is a comprehensive church discipleship management system built for Iglesia Casa de Dios in Aurora, Colorado. The application provides a complete solution for managing church groups, members, attendance tracking, resources, and announcements in Spanish. It features role-based access control with three user levels (admin, leader, member) and includes reporting capabilities with PDF and CSV export functionality.

## Discipleship System Features
- **CREA Methodology**: Complete discipleship learning system using Conocer, Reflexionar, Examinar, Aplicar methodology
- **Bloque 2: Vida en Santidad**: 4 lessons on holiness (Santidad de Dios, Integridad, Humildad, Misericordia)
- **Módulo 2: Vida en Santidad - Segunda Parte**: 3 additional lessons (Sansón, Zaqueo, Sinaí)
- **Progress Tracking**: Individual lesson and module progress monitoring
- **AI Image Generation**: Dynamic lesson imagery creation capability
- **Minister Access Control**: Role-based content management and student progress oversight

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **React + TypeScript**: Modern component-based architecture using functional components with hooks
- **Vite**: Fast build tool and development server for optimal development experience
- **Tailwind CSS**: Utility-first CSS framework for consistent styling and responsive design
- **Shadcn/ui**: Pre-built component library built on Radix UI primitives for accessible, customizable components
- **Wouter**: Lightweight client-side routing library for single-page application navigation
- **React Query (@tanstack/react-query)**: Server state management with caching, synchronization, and error handling
- **React Hook Form + Zod**: Form handling with robust validation using TypeScript-first schema validation

## Backend Architecture
- **Express.js**: RESTful API server with middleware for request processing and authentication
- **TypeScript**: Type-safe server-side development with shared types between frontend and backend
- **Drizzle ORM**: Type-safe database operations with PostgreSQL dialect
- **Replit Authentication**: OAuth-based authentication system integrated with Replit's identity provider
- **Session Management**: Secure session storage using PostgreSQL with express-session

## Database Design
- **PostgreSQL**: Primary database using Neon serverless PostgreSQL
- **Schema Structure**: 
  - Users table for authentication and role management
  - Groups table for discipleship group organization
  - Members table for church member information with group associations
  - Attendance table for tracking weekly group meetings
  - Resources table for digital content management
  - Announcements table for church communications
  - Group leaders junction table for leader-group relationships
  - Discipleship system tables (modules, lessons, questions, progress) for CREA methodology
  - Message system for hierarchical church communication
- **Drizzle Kit**: Database migration management and schema synchronization

## Authentication & Authorization
- **Replit OAuth**: Integrated authentication using Replit's OpenID Connect provider
- **Role-Based Access Control**: Three-tier permission system (admin, leader, member)
- **Session Security**: Secure HTTP-only cookies with PostgreSQL session storage
- **Route Protection**: Server-side middleware for API endpoint protection

## State Management
- **React Query**: Server state caching and synchronization
- **React Hook Form**: Form state management with validation
- **Local Component State**: React hooks for UI state management

## File Structure
- `/client`: Frontend React application with TypeScript
- `/server`: Express.js backend API with authentication and database layers
- `/shared`: Shared TypeScript schemas and types between frontend and backend
- Component organization follows feature-based structure with reusable UI components

# External Dependencies

## Database Services
- **Neon Database**: Serverless PostgreSQL hosting with connection pooling
- **@neondatabase/serverless**: PostgreSQL client optimized for serverless environments

## Authentication Services
- **Replit Authentication**: OAuth 2.0 / OpenID Connect integration for user authentication
- **Session Storage**: PostgreSQL-based session management using connect-pg-simple

## UI Libraries
- **Radix UI**: Headless component primitives for accessibility and customization
- **Tailwind CSS**: Utility-first CSS framework for styling
- **Lucide React**: Icon library for consistent iconography
- **Font Awesome**: Additional icon set for church-specific icons

## Chart & Export Libraries
- **Chart.js**: Client-side charting for attendance analytics and dashboard visualizations
- **jsPDF**: PDF generation for reports and member data exports
- **CSV Export**: Browser-based CSV generation with UTF-8 BOM encoding

## Development Tools
- **Vite**: Build tool and development server with hot module replacement
- **TypeScript**: Type checking and development experience enhancement
- **ESBuild**: Fast JavaScript bundler for production builds
- **PostCSS**: CSS processing with Tailwind CSS integration