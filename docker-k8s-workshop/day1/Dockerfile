FROM node:18-alpine
 
# Set the working directory
WORKDIR /app
 
# Copy package files and install dependencies
COPY package*.json ./
RUN npm install
 
# Copy the rest of the application
COPY . .
 
# Expose port
EXPOSE 8080
 
# Start the app
CMD ["npm", "start"]
