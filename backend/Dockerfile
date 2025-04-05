# backend/Dockerfile

# Base image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy source code
COPY . .

# Generate Prisma client
RUN npx prisma generate

# Build TypeScript code
RUN npm run build

# Expose API port (ví dụ: 5000)
EXPOSE 5000

# Start the backend (after build)
CMD ["npm", "start"]
