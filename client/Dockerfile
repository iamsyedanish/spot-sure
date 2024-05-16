# Use an official Node.js runtime as a parent image
FROM node:latest

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install dependencies
RUN npm install

EXPOSE 3000

# Copy the rest of the application code
COPY . .

# The command to start the app
CMD ["npm", "start"]
