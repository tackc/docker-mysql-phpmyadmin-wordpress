# WordPress Site

### [Set up new WordPress Website](https://docs.docker.com/compose/wordpress/)

- Create directory for site
- Create `docker-compose.yml` containing the following:

```yml
version: "3.9"

services:
  db:
    image: mysql:8.0.23
    volumes:
      - db_data:/var/lib/mysql
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: somewordpress
      MYSQL_DATABASE: wordpress
      MYSQL_USER: wordpress
      MYSQL_PASSWORD: wordpress

  wordpress:
    depends_on:
      - db
    image: wordpress:latest
    ports:
      - "8000:80"
    restart: always
    environment:
      WORDPRESS_DB_HOST: db:3306
      WORDPRESS_DB_USER: wordpress
      WORDPRESS_DB_PASSWORD: wordpress
      WORDPRESS_DB_NAME: wordpress
volumes:
  db_data: {}
```

- Install the following plugins:
  - WP GraphQL
  - WP Gatsby

### To Run the Site

- Run `docker-compose up -d` (detached mode...won't show requests & responses in your Terminal) or `docker-compose up`

- Navigate to `localhost:8000`
