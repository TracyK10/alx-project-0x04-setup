# Splash App - AI-Powered Platform

![Splash App Homepage](/alx-project-0x03/public/assets/images/home.png)

Splash App is a modern, responsive web application built with Next.js, TypeScript, and Tailwind CSS. It serves as a platform for AI-powered tools and features, providing users with an intuitive interface to interact with various AI capabilities.

## ✨ Features

- **Modern UI/UX**: Clean, responsive design built with Tailwind CSS
- **Type Safety**: Full TypeScript support for better developer experience
- **Component-Based Architecture**: Reusable UI components for maintainability
- **Responsive Layout**: Works seamlessly on all device sizes
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
