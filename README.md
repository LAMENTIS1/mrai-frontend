# Accusaga AI Frontend

Next-generation AI-powered data analysis and insights platform built with React, Vite, and TypeScript.

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- npm, yarn, or bun

### Local Development
```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

## 🐳 Docker Deployment

### For Hugging Face Spaces

This project is configured for deployment on Hugging Face Spaces with Docker.

#### Files Included:
- `Dockerfile` - Multi-stage build optimized for production
- `nginx.conf` - Nginx configuration for serving the React app
- `.dockerignore` - Excludes unnecessary files from Docker build
- `env.template` - Template for environment variables

#### Deployment Steps:

1. **Prepare Environment Variables:**
   ```bash
   # Copy the template and configure your variables
   cp env.template .env
   # Edit .env with your actual values
   ```

2. **Build and Test Locally:**
   ```bash
   # Build the Docker image
   docker build -t accusaga-ai .

   # Run the container
   docker run -p 7860:7860 accusaga-ai
   ```

3. **Deploy to Hugging Face Spaces:**
   - Push your code to a Git repository
   - Create a new Space on Hugging Face
   - Select "Docker" as the SDK
   - Configure your environment variables in the Space settings
   - The Space will automatically build and deploy your app

#### Environment Variables for Hugging Face Spaces:
Set these in your Space settings:
- `VITE_API_BASE_URL` - Your API endpoint
- `VITE_APP_NAME` - Application name
- Any other variables from `env.template`

### Docker Features:
- **Multi-stage build** for optimized image size
- **Nginx** for efficient static file serving
- **Port 7860** configured for Hugging Face Spaces
- **Client-side routing** support
- **Gzip compression** enabled
- **Security headers** included
- **Static asset caching** optimized

## 📁 Project Structure

```
src/
├── components/     # Reusable UI components
├── pages/         # Page components
├── hooks/         # Custom React hooks
├── services/      # API services
├── stores/        # State management
├── types/         # TypeScript type definitions
└── utils/         # Utility functions
```

## 🛠️ Tech Stack

- **React 18** - UI framework
- **Vite** - Build tool and dev server
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Radix UI** - Accessible components
- **React Query** - Data fetching
- **Zustand** - State management
- **React Router** - Navigation

## 📝 License

© 2024 Accusaga Information Technologies
