# Development Dockerfile (Dockerfile.dev)
FROM node:20-alpine

WORKDIR /app

# Add necessary development tools
RUN apk add --no-cache python3 make g++

# Copy package files
COPY ../../package*.json ./

# Install dependencies
RUN npm install

# Copy source code
COPY ../../ .

# Expose port
EXPOSE 3000
EXPOSE 9229

# Start development server
CMD ["npm", "run", "start:dev"]