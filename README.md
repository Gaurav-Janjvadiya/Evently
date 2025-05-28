# Event Platform

A full-stack event management platform built with Next.js 14, TypeScript, and Stripe integration.

## Features

- **User Authentication** - Secure authentication with Clerk
- **Event Management** - Create, read, update, and delete events
- **Payment Processing** - Stripe integration for ticket purchases
- **Search & Filter** - Find events by name and category
- **Responsive Design** - Works on all devices
- **Order Management** - Track event purchases and attendance

## Tech Stack

- **Frontend**: Next.js 14, TypeScript, TailwindCSS
- **Backend**: Node.js, MongoDB
- **Authentication**: Clerk
- **Payments**: Stripe
- **File Upload**: UploadThing
- **Form Validation**: React Hook Form + Zod
- **UI Components**: Shadcn/ui

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- MongoDB database
- Stripe account
- Clerk account
- UploadThing account

### Installation

1. Clone the repository
```bash
git clone https://github.com/Gaurav-Janjvadiya/Evently.git
cd event-platform
```

2. Install dependencies
```bash
npm install
```

3. Set up environment variables

Create a `.env` file in the root directory:

```env
# Next.js
NEXT_PUBLIC_SERVER_URL=http://localhost:3000

# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
NEXT_CLERK_WEBHOOK_SECRET=your_clerk_webhook_secret

NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/

# Database
MONGODB_URI=your_mongodb_connection_string

# File Upload
UPLOADTHING_SECRET=your_uploadthing_secret
UPLOADTHING_APP_ID=your_uploadthing_app_id

# Stripe
STRIPE_SECRET_KEY=your_stripe_secret_key
STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key
```

4. Run the development server
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the application.

## Project Structure

```
event-platform/
├── app/                    # Next.js app directory
├── components/            # Reusable UI components
├── lib/                   # Utility functions and database
├── types/                 # TypeScript type definitions
├── public/               # Static assets
└── styles/               # Global styles
```

## Key Features Explained

### Event Management
- Users can create events with details like title, description, date, location, and price
- Events can be categorized for better organization
- Event organizers can update or delete their events

### Payment Integration
- Stripe checkout for secure payment processing
- Support for both free and paid events
- Order tracking and management

### User Authentication
- Clerk handles user registration, login, and profile management
- Secure webhook integration for user data synchronization

### Search and Filtering
- Real-time search functionality
- Filter events by category
- Pagination for large event lists
