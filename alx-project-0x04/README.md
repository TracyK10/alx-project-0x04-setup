# ALX Project 0x04: Introduction to Next.js

This project serves as an introduction to Next.js, a React framework for building server-rendered applications. It's part of the ALX Software Engineering program and focuses on the fundamentals of Next.js, including routing, API routes, and static site generation.

## ✨ Features

- **Server-Side Rendering (SSR)**: Improved SEO and performance
- **File-based Routing**: Intuitive page-based routing system
- **API Routes**: Build API endpoints within your Next.js application
- **Static Site Generation (SSG)**: Pre-render pages at build time
- **TypeScript Support**: Type-safe development experience
- **Responsive Design**: Built with Tailwind CSS for mobile-first development

## 🛠️ Tech Stack

- **Framework**: Next.js 13+
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Linting/Formatting**: ESLint, Prettier
- **Build Tool**: Turbopack (Next.js default)

## 🚀 Getting Started

### Prerequisites

- Node.js 16.8 or later
- npm or yarn package manager

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/TracyK10/alx-project-0x04-setup.git
   cd alx-project-0x04-setup/alx-project-0x04
   ```

2. Install dependencies:

   ```bash
   npm install
   # or
   yarn install
   ```

### Development

Start the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the result.

## 📁 Project Structure

```text
alx-project-0x04/
├── components/         # Reusable UI components
│   ├── common/        # Common components (Button, Card, etc.)
│   └── layouts/       # Layout components (Header, Footer, etc.)
├── pages/             # Application pages and API routes
│   ├── api/           # API routes
│   ├── _app.tsx       # Custom App component
│   ├── _document.tsx  # Custom Document component
│   └── index.tsx      # Home page
├── public/            # Static assets
├── styles/            # Global styles
└── README.md          # Project documentation
```

## 🌟 Next.js Features

This project demonstrates key Next.js features:

### File-based Routing

Next.js has a file-system based router built on the concept of pages. When a file is added to the `pages` directory, it's automatically available as a route.

```typescript
// pages/about.tsx
const About = () => {
  return <div>About Page</div>;
};

export default About;
```

### API Routes

API routes let you create API endpoints inside a Next.js app. They can be deployed as Serverless Functions.

```typescript
// pages/api/hello.ts
export default function handler(req, res) {
  res.status(200).json({ name: 'John Doe' });
}
```

### Data Fetching

Next.js provides multiple methods for data fetching:

1. **getStaticProps**: Fetch data at build time
2. **getServerSideProps**: Fetch data on each request
3. **getStaticPaths**: Specify dynamic routes to pre-render

```typescript
// Example of getStaticProps
export async function getStaticProps() {
  const res = await fetch('https://api.example.com/data');
  const data = await res.json();

  return {
    props: {
      data,
    },
  };
}
```

## 🎨 Styling

This project uses Tailwind CSS for styling:

- **Utility-First**: Rapid UI development with utility classes
- **Responsive Design**: Built-in responsive modifiers
- **Dark Mode**: Support for dark mode with `dark:` variant
- **Customization**: Extend the default theme in `tailwind.config.js`

## 🧪 Testing

Run tests with:

```bash
npm test
# or
yarn test
```

## 📝 License

This project is part of the ALX Software Engineering program.

## 📧 Contact

Project Link: [https://github.com/TracyK10/alx-project-0x04-setup](https://github.com/TracyK10/alx-project-0x04-setup)
Author: Tracy K
