# ---------- Stage 1: Build Angular ----------
FROM node:18-alpine AS build

WORKDIR /app

# Copy package files first (better caching)
COPY package*.json ./

# Clean install (recommended for Docker)
RUN npm ci

# Copy project files
COPY . .

# Build in production mode (default is production in your angular.json)
RUN npm run build

# ---------- Stage 2: Serve with Nginx ----------
FROM nginx:alpine

# Remove default nginx files
RUN rm -rf /usr/share/nginx/html/*

# Copy the Angular build output
COPY --from=build /app/dist/angular-15-crud/ /usr/share/nginx/html/

# Optional: Add custom nginx config for Angular routing
# COPY nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
