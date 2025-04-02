# Use the official Node.js image
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json (or yarn.lock)
COPY server/package*.json ./

# Install dependencies
RUN npm install --production

# Copy the rest of the application
COPY server/ .

# Expose the port the app will run on
EXPOSE 3000

# Command to run the app
CMD ["node", "src/index.js"]
