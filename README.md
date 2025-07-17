# Atlassian Docker Images

This repository contains Dockerfiles and configurations to build custom Docker images for Atlassian products, specifically Jira and Confluence.

## Features

The Docker images built from this repository include the following additions to the official Atlassian images:

- **MySQL Connector/J:** The [MySQL Connector/J](https://dev.mysql.com/downloads/connector/j/) is included, allowing you to connect your Atlassian product to a MySQL database.
- **Atlassian Agent:** A Java agent is included to be used with the Atlassian products.

## Built Images

The following images are built and pushed to the GitHub Container Registry:

- `ghcr.io/congtran/atlassian/jira:latest`
- `ghcr.io/congtran/atlassian/jira:9-jdk17`
- `ghcr.io/congtran/atlassian/confluence:latest`
- `ghcr.io/congtran/atlassian/confluence:9.2-jdk21`

## Usage

You can use these Docker images as you would use the official Atlassian images. For example, to start a Jira container, you can use the following command:

```bash
docker run -d --name jira -p 8080:8080 ghcr.io/congtran/atlassian/jira:latest
```

## Build

The Docker images are built automatically using a GitHub Actions workflow. The workflow is defined in `.github/workflows/build.yaml`.

The workflow is triggered on:

- Pushes to the `main` branch
- Manual dispatch
- A weekly schedule

The workflow builds and pushes images for both Jira and Confluence to the GitHub Container Registry.
