# Pocketbase Dockerfile

This repository provides a **multi-stage Dockerfile** that builds the latest version of [PocketBase](https://pocketbase.io/) in a lightweight **Alpine Linux** environment.

## Features

- **Lightweight:** Built on a minimal Alpine base image.
- **Multi-Stage Build:** Optimized for small image size and fast builds.
- **Up-to-date:** Automatically fetches the latest version of PocketBase.

## Usage

### Prerequisites

- **Docker**: Ensure Docker is installed (version 23.0.15 or later recommended).

### Building the Image

To build the Docker image, run the following command:

```bash
docker build -t pocketbase .
```

### Running the Container

To start a container using the built image:

```bash
docker run -d -p 8080:8080 --name pocketbase-container pocketbase
```

PocketBase will then be accessible at `http://localhost:8080`.

### Persisting Data

If you want to persist PocketBase data, mount a volume:

```bash
docker run -d -p 8080:8080 -v /path/to/data:/pb_data --name pocketbase-container pocketbase
```

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request if you want to improve or add something.
