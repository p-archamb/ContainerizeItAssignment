FROM node:18

WORKDIR /app

# Install MySQL client tools
RUN apt-get update && \
    apt-get install -y default-mysql-client && \
    rm -rf /var/lib/apt/lists/*

# Install mysql2 package (which supports the necessary authentication protocol)
RUN npm install mysql2

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy application code
COPY . .

# Use sed to replace the database connection configuration
RUN sed -i 's/host: "localhost"/host: "db"/' index.js


EXPOSE 8800

CMD ["node", "index.js"]