# Use Node.js LTS as the base image
FROM node:18-slim

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install --production

# Copy the rest of the application code
COPY . .

# Expose the port (Cloud Run uses the PORT environment variable)
EXPOSE 7860

# Start the server
CMD [ "npm", "start" ]
