# SVR.JS with Docker

This repository demonstrates how to set up and run [SVR.JS](https://svrjs.org/) using Docker Compose. SVR.JS is a lightweight static file server, and this guide simplifies the deployment process by eliminating installation dependencies.

## Project Structure

```
svrjs-with-docker
├── README.md
├── docker-compose.yml
├── svrjs-config.json
└── www
    ├── index.html
    └── style.css
```

- **`docker-compose.yml`**: Defines the Docker services and configurations.
- **`svrjs-config.json`**: Configuration file for SVR.JS.
- **`www`**: Directory for static files (e.g., HTML, CSS).
- **`README.md`**: This file.

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/) installed on your system.
- Basic understanding of Docker Compose.

### Steps to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/andyj/svrjs-with-docker.git
   cd svrjs-with-docker
   ```

2. Start the Docker container:

   ```bash
   docker-compose up
   ```

3. Open your browser and navigate to:

   ```
   http://localhost:8383
   ```

   You should see the sample `index.html` page served by SVR.JS.

### Configuration

The `svrjs-config.json` file contains key configurations:

```json
{
  "port": 80,
  "wwwroot": "/var/www/svrjs",
  "logging": {
    "enabled": true,
    "level": "info"
  }
}
```


## Customisation

To serve your own static files:

1. Replace the contents of the `www` directory with your own files.
2. Restart the Docker container:

   ```bash
   docker-compose down && docker-compose up
   ```

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

If you encounter any issues or have questions, feel free to open an issue, submit a pull request or ping me on [bsky.app/profile/andyjarrett.com](https://bsky.app/profile/andyjarrett.com)
