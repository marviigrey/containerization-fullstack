# # Base Image
# FROM node:20-alpine

# # Install a lightweight web server to serve the static files
# RUN npm install -g serve

# # Set Working Directory
# WORKDIR /app

# # Copy package.json and package-lock.json files to the container
# COPY package*.json ./

# # Install the dependencies
# RUN npm install

# # Copy the rest of the frontend files
# COPY . .

# # Build the React application
# RUN npm run build

# # Expose the port the app
# EXPOSE 3000

# # Command to run the app
# CMD ["serve", "-s", "dist", "-l", "3000"]



# Base Image
FROM node:20-alpine

# # Install a lightweight web server to serve the static files
# RUN npm install -g serve

WORKDIR /app

COPY package*.json /app/

RUN npm install

COPY ./ /app/

RUN npm run build

# Use an Nginx container to serve the build
FROM nginx:alpine
COPY --from=0 /app/dist /usr/share/nginx/html

COPY ./nginx.conf /etc/nginx/conf.d/default.conf

# Expose port 80
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]