# Use the official Node.js image from the Docker Hub
FROM node:14

ARG DEFAULT_PORT

# Create and change to the app directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

ENV PORT $DEFAULT_PORT

# Expose port 80
EXPOSE $PORT

# Command to run the application
CMD ["npm", "start"]