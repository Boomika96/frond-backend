# Base Image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package files first (for caching layer)
COPY package*.json ./

# Install only production dependencies
RUN npm install

# Copy all backend source code
COPY . .

# Expose backend port (change if yours uses something else)
EXPOSE 3500

# Start backend
CMD ["node", "server.js"]
