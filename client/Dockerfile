FROM docker.io/node:latest as BASE
ENV NODE_ENV development
# Add a work directory
WORKDIR /app
# Cache and Install dependencies
COPY package.json .
COPY package-lock.json .
RUN vite build
# Copy app files
COPY . .
# Expose port
EXPOSE 8000
# Start the app
CMD [ "npm", "run", "dev" ]