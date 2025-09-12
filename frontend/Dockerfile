FROM node:18

# Set working directory before copying files
WORKDIR /app

# Copy package files first for better caching
COPY package.json yarn.lock ./

# Install dependencies including react-scripts
RUN yarn install

# Copy rest of the app source code
COPY . .

# Expose ports
EXPOSE 3000

# Runtime command to start dev server
CMD ["yarn", "start"]
