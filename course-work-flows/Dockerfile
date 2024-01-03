# Stage 1: Build the Node.js application
FROM node:18 AS build
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci --also=dev && npm run build



# Stage 2: Serve the application with Nginx
FROM nginx:latest
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
