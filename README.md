# WordPress Site

- [Docker Setup Reference](https://github.com/imranhsayed/nextjs-headless-wordpress/tree/feature/youtube-tutorial)

### [Set up new WordPress Website](https://docs.docker.com/compose/wordpress/)

- Create directory for site
- Create `docker-compose.yml` containing the following:
- Install the following plugins into the WordPress site:
  - WP GraphQL
  - WP Gatsby
  - Advanced Custom Fields

### To Run the Site

- Run `docker-compose up -d` (detached mode...won't show requests & responses in your Terminal) or `docker-compose up`

- Navigate to `localhost:8020` || whatever port you set up in `docker-compose.yml`
