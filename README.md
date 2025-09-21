# pipeline-runner

`pipeline-runner` is a Docker image designed for use in CI/CD pipelines. It provides a containerized environment with essential tools for infrastructure automation and deployment, including Terraform and Helm.

## Features

- Pre-installed [Terraform](https://www.terraform.io/) for infrastructure provisioning
- Pre-installed [Helm](https://helm.sh/) for Kubernetes package management
- Suitable for integration with popular CI/CD platforms

## Usage

Pull the image from Docker Hub:

```sh
docker pull yelluc/pipeline-runner:latest
```

Run the container:

```sh
docker run --rm -it yelluc/pipeline-runner:latest
```

Build the container:

```sh
docker build --build-arg TF_VERSION=1.13.3 --build-arg HELM_VERSION=3.19.0 -t yelluc/pipeline-builder:develop
```

## Included Tools

- Terraform
- Helm

## Customization

You can extend the image by creating your own Dockerfile:

```Dockerfile
FROM your-dockerhub-username/pipeline-runner:latest
# Add custom tools or scripts here
```

## License

MIT

## Contributing

Contributions are welcome! Please open issues or submit pull requests.
