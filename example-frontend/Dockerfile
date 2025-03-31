FROM node:16

WORKDIR /usr/src/app

# Copy package files first for better caching
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application
COPY . .

# Build the static files
RUN npm run build

# Install serve for production serving
RUN npm install -g serve

# Expose the port that serve will use
EXPOSE 5000

# Start the server
CMD ["serve", "-s", "-l", "5000", "build"]
