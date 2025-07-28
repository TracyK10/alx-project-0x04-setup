# ALX Project 0x05: State Management with Context API

This project demonstrates state management in a Next.js application using React's Context API. It's part of the ALX Software Engineering program and focuses on implementing global state management with TypeScript support.

## ✨ Features

- **Context API**: Global state management solution
- **Type Safety**: Full TypeScript integration
- **Custom Hooks**: Reusable logic with custom hooks
- **Modern UI**: Responsive design with Tailwind CSS
- **Theme Toggling**: Light/dark mode implementation

## 🛠️ Tech Stack

- **Framework**: Next.js 13+
- **Language**: TypeScript
- **State Management**: React Context API
- **Styling**: Tailwind CSS
- **Linting/Formatting**: ESLint, Prettier

## 🚀 Getting Started

### Prerequisites

- Node.js 16.8 or later
- npm or yarn package manager

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/TracyK10/alx-project-0x04-setup.git
   cd alx-project-0x04-setup/alx-project-0x05
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
alx-project-0x05/
├── components/         # Reusable UI components
│   ├── common/        # Common components (Button, etc.)
│   └── layouts/       # Layout components (Header, etc.)
├── context/           # React Context providers
│   └── ThemeContext.tsx # Theme context implementation
├── hooks/             # Custom React hooks
├── interfaces/        # TypeScript interfaces/types
├── pages/             # Application pages
├── public/            # Static assets
├── styles/            # Global styles
└── README.md          # Project documentation
```

## 🔧 State Management

This project uses React's Context API for state management with the following features:

- **Theme Context**: Global theme state (light/dark mode)
- **Type Safety**: Full TypeScript support for context values
- **Custom Hooks**: Easy access to context values
- **Performance Optimized**: Memoized context values

### Example: Theme Context Implementation

```typescript
// context/ThemeContext.tsx
'use client';

import React, { createContext, useContext, useState, useEffect, ReactNode } from 'react';

type Theme = 'light' | 'dark';

type ThemeContextType = {
  theme: Theme;
  toggleTheme: () => void;
};

const ThemeContext = createContext<ThemeContextType | undefined>(undefined);

export const ThemeProvider = ({ children }: { children: ReactNode }) => {
  const [theme, setTheme] = useState<Theme>('light');

  // Initialize theme from localStorage or prefer-color-scheme
  useEffect(() => {
    const savedTheme = localStorage.getItem('theme') as Theme | null;
    const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
    
    setTheme(savedTheme || (prefersDark ? 'dark' : 'light'));
  }, []);

  // Update document class and save to localStorage when theme changes
  useEffect(() => {
    document.documentElement.classList.toggle('dark', theme === 'dark');
    localStorage.setItem('theme', theme);
  }, [theme]);

  const toggleTheme = () => {
    setTheme((prevTheme) => (prevTheme === 'light' ? 'dark' : 'light'));
  };

  return (
    <ThemeContext.Provider value={{ theme, toggleTheme }}>
      {children}
    </ThemeContext.Provider>
  );
};

export const useTheme = () => {
  const context = useContext(ThemeContext);
  if (context === undefined) {
    throw new Error('useTheme must be used within a ThemeProvider');
  }
  return context;
};
```

## 🎨 Styling

- **Tailwind CSS** for utility-first styling
- Dark mode support with `dark:` variant
- Responsive design with mobile-first approach
- Custom components in `components/common/`

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