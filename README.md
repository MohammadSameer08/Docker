# Docker React + Vite Application

A containerized React + Vite development environment using Docker.

## Docker Setup

This project includes a `Dockerfile` configured for development using Node.js Alpine image for a lightweight container.

### Building the Docker Image

```bash
docker build -t docker-test .
```

### Running the Container

```bash
docker run -p 5173:5173 docker-test
```

The application will be available at `http://localhost:5173`

## Docker Configuration

- **Base Image**: `node:22-alpine`
- **Working Directory**: `/app`
- **Exposed Port**: `5173` (Vite dev server)
- **Start Command**: `npm run dev`

## Development Commands

Inside the container or locally:

- `npm run dev` - Start Vite development server
- `npm run build` - Build for production
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build

## Project Structure

- `Dockerfile` - Container configuration
- `src/` - React source files
- `public/` - Static assets
- `package.json` - Project dependencies and scripts
