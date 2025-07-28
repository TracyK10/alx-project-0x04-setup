# ALX Project 0x06: Advanced State Management with Redux

This project demonstrates advanced state management in a Next.js application using Redux Toolkit. It's part of the ALX Software Engineering program and focuses on implementing predictable state management with TypeScript support.

## ✨ Features

- **Redux Toolkit**: Predictable state management solution
- **Type Safety**: Full TypeScript integration with Redux
- **Redux DevTools**: Built-in debugging capabilities
- **Modern UI**: Responsive design with Tailwind CSS
- **Context API Integration**: Combined with Redux for global UI state

## 🛠️ Tech Stack

- **Framework**: Next.js 13+
- **Language**: TypeScript
- **State Management**: Redux Toolkit, React Context
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
   cd alx-project-0x04-setup/alx-project-0x06
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
alx-project-0x06/
├── components/         # Reusable UI components
│   ├── common/        # Common components (Button, etc.)
│   └── layouts/       # Layout components (Header, etc.)
├── context/           # React Context providers
├── interfaces/        # TypeScript interfaces/types
├── pages/             # Application pages
├── public/            # Static assets
├── store/             # Redux store and slices
├── styles/            # Global styles
└── README.md          # Project documentation
```

## 🔧 State Management

This project uses Redux Toolkit for state management with the following features:

- **Slices**: Organized state logic using `createSlice`
- **Type Safety**: Full TypeScript support for actions and state
- **Middleware**: Custom middleware for side effects
- **Redux DevTools**: Built-in debugging capabilities

### Example: Counter Slice

```typescript
// store/slices/counterSlice.ts
import { createSlice, PayloadAction } from '@reduxjs/toolkit';

interface CounterState {
  value: number;
}

const initialState: CounterState = {
  value: 0,
};

export const counterSlice = createSlice({
  name: 'counter',
  initialState,
  reducers: {
    increment: (state) => {
      state.value += 1;
    },
    decrement: (state) => {
      state.value = Math.max(0, state.value - 1);
    },
  },
});

export const { increment, decrement } = counterSlice.actions;
export default counterSlice.reducer;
```

## 🎨 Styling

- **Tailwind CSS** for utility-first styling
- Responsive design with mobile-first approach
- Custom components in `components/common/`

## 📝 License

This project is part of the ALX Software Engineering program.

## 📧 Contact

Project Link: [https://github.com/TracyK10/alx-project-0x04-setup](https://github.com/TracyK10/alx-project-0x04-setup)
- **Custom 404 Page**: Beautiful error page with helpful navigation
- **Performance Optimized**: Built with Next.js for optimal performance

## 📱 Screenshots

### Homepage
![Splash App Homepage](/alx-project-0x03/public/assets/images/home.png)

### 404 Error Page
![404 Error Page](/alx-project-0x03/public/assets/images/error.png)

## 🚀 Getting Started

### Prerequisites

- Node.js 18.0 or later
- npm or yarn

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/TracyK10/alx-project-0x03-setup.git
   cd alx-project-0x03
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Start the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser to see the result.

## 🛠️ Project Structure

```
alx-project-0x03/
├── components/
│   ├── common/           # Reusable UI components
│   │   └── Button.tsx    # Custom button component
│   └── layouts/          # Layout components
│       ├── Footer.tsx    # Footer component
│       ├── Header.tsx    # Header component
│       └── Layout.tsx    # Main layout wrapper
├── interface/            # TypeScript interfaces
│   └── index.tsx         # Centralized type definitions
├── pages/
│   ├── _app.tsx          # Main App component
│   ├── _document.tsx     # Custom Document
│   ├── index.tsx         # Home page
│   └── 404.tsx           # Custom 404 page
├── public/               # Static files
│   └── assets/
│       └── images/       # Image assets
├── styles/               # Global styles
│   └── globals.css       # Global CSS with Tailwind
└── package.json          # Project dependencies
```

## 🎨 Styling

This project uses:
- **Tailwind CSS** for utility-first styling
- **React Icons** for iconography
- Custom CSS in `globals.css` for global styles

## 🔍 Code Organization

- **Components**: Reusable UI components are organized by feature
- **Interfaces**: TypeScript interfaces are centralized in the `interface` directory
- **Pages**: Each route has its own file in the `pages` directory
- **Styles**: Global styles and Tailwind configuration

## 🛠 Built With

- [Next.js](https://nextjs.org/) - The React Framework for Production
- [TypeScript](https://www.typescriptlang.org/) - TypeScript is a typed superset of JavaScript
- [Tailwind CSS](https://tailwindcss.com/) - A utility-first CSS framework
- [React Icons](https://react-icons.github.io/react-icons/) - Popular icons for React projects

## 🙏 Acknowledgments

- [Next.js Documentation](https://nextjs.org/docs)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [React Icons](https://react-icons.github.io/react-icons/)
