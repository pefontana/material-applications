FROM node:16

WORKDIR /app

ENV REACT_APP_BACKEND_URL=http://localhost:8080

# Expose the port that serve will use
EXPOSE 5000

COPY . .

# Install dependencies
RUN npm install

# Build
RUN npm run build

RUN npm install -g serve


# Start the server
CMD ["serve", "-s", "-l", "5000", "build"]
