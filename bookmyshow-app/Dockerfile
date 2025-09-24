# Use Node.js 18 (LTS)
FROM node:18

# Set working directory
WORKDIR /app

# Copy package files first (for caching layers)
COPY package*.json ./

# Install dependencies (use legacy-peer-deps to avoid conflicts)
RUN npm install --legacy-peer-deps

# Copy the entire project
COPY . .

# Expose app port
EXPOSE 3000

# Environment variables
ENV NODE_OPTIONS=--openssl-legacy-provider
ENV PORT=3000

# Start the application
CMD ["npm", "start"]
