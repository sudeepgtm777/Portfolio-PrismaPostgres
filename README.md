# Portfolio with Prisma & PostgreSQL

A modern portfolio website built with Next.js, featuring a blog system and comment functionality powered by Prisma ORM and PostgreSQL.

## Screenshots

### Home Page

![Home Page](./public/img/HomePage.png)

### Blog Page

![Blog Page](./public/img/BlogPage.png)

### Comments Page

![Comments Page](./public/img/CommentsPage.png)

## Features

- **Personal Portfolio**: Showcase your skills and experience
- **Blog System**: Create and manage blog posts with markdown support
- **Comment System**: GitHub OAuth authentication for user comments
- **Responsive Design**: Built with Tailwind CSS and Radix UI components
- **Database**: PostgreSQL with Prisma ORM for type-safe database operations

## Tech Stack

- **Framework**: Next.js 16 with App Router
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: Better Auth with GitHub OAuth
- **Styling**: Tailwind CSS v4
- **UI Components**: Radix UI primitives
- **Markdown**: React Markdown with GitHub Flavored Markdown

## Getting Started

1. **Clone the repository**

```bash
git clone <your-repo-url>
cd portfolio
```

2. **Install dependencies**

```bash
npm install
```

3. **Set up environment variables**
   Create a `.env` file with:

```env
DATABASE_URL="postgresql://username:password@localhost:5432/portfolio"
BETTER_AUTH_SECRET="your-secret-key"
GITHUB_CLIENT_ID="your-github-client-id"
GITHUB_CLIENT_SECRET="your-github-client-secret"
```

4. **Set up the database**

```bash
npx prisma generate
npx prisma db push
```

5. **Run the development server**

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the portfolio.

## Project Structure

```
├── app/                 # Next.js app directory
│   ├── api/            # API routes
│   ├── blog/           # Blog pages
│   └── comments/       # Comments page
├── components/         # Reusable UI components
├── lib/               # Utilities and database config
├── prisma/            # Database schema and migrations
└── public/            # Static assets
```

## Database Schema

- **User**: GitHub OAuth user data
- **BlogPost**: Blog posts with slug-based routing
- **Comment**: User comments with relations
- **Session/Account**: Authentication data

## Deployment

Deploy on Vercel with PostgreSQL database:

1. Connect your GitHub repository to Vercel
2. Add environment variables in Vercel dashboard
3. Deploy automatically on push to main branch
