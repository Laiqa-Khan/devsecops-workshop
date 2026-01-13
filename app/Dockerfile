# Use Node 18 Alpine image as the base
FROM node:18-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json (or package.json if no lock file) to the working directory
COPY package*.json ./

# Install only the production dependencies
RUN npm install --production

# Copy all other application files into the container
COPY . .

# Expose port 3000 to be accessible from outside the container
EXPOSE 3000

# Start the application using `node index.js`
CMD ["node", "index.js"]
