FROM node:16-alpine

WORKDIR /app

# ENV REACT_APP_BACKEND_URL=http://localhost:8080
# ENV REACT_APP_BACKEND_URL=http://localhost:80

# Expose the port that serve will use
EXPOSE 5000

COPY . .

# Install dependencies
RUN npm install

# Build
RUN npm run build

RUN npm install -g serve

RUN adduser -D executor
USER executor

# Start the server
CMD ["serve", "-s", "-l", "5000", "build"]
