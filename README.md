## n8n Docker Compose

This repository contains a `docker-compose.yml` file for setting up an **n8n** instance with PostgreSQL.

### Prerequisites

- Docker
- Docker Compose

### Setup Instructions

1. Clone the repository:

   ```sh
   git clone https://github.com/strider73/n8n-docker-compose.git
   cd n8n-docker-compose
   ```

2. Create the PostgreSQL user and database:

   ```sql
   CREATE USER n8n WITH PASSWORD '5785Ch00';
   CREATE DATABASE n8n_db OWNER n8n;
   GRANT ALL PRIVILEGES ON DATABASE n8n_db TO n8n;
   ALTER ROLE n8n WITH LOGIN;
   ```

3. Start the services using Docker Compose:

   ```sh
   docker-compose up -d
   ```

4. Access the n8n instance at:

   ```
   http://localhost:5678
   ```

### Configuration

- You can modify environment variables in the `.env` file.
- Ensure PostgreSQL is accessible by n8n.

### License

This project is open-source and available under the MIT License.
