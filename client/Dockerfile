# Use the official Node.js image
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and install dependencies
COPY client/package*.json ./

# Install all dependencies, including dev dependencies
RUN npm install

# Copy the rest of the application
COPY client/ .

# Build the app for production
RUN npm run build

# Install a simple web server to serve the build
RUN npm install -g serve

# Expose port 3001 (or any other port you want to serve the React app on)
EXPOSE 3001

# Command to start serving the app
CMD ["serve", "-s", "dist", "-l", "3001"]
