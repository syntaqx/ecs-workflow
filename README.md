# Docker ECS Workflow

This workflow is a very simple build out that builds a Docker container,
publishes it to Docker Hub for collaboration sake. This image is then mirrored
to ECR to be closer to deployment, and deployed to ECS (Fargate).

This is the smallest amount of effort to get this functioning, but it works
well, and is very simple to work with.

## Secrets

- `DOCKERHUB_USERNAME`
- `DOCKERHUB_TOKEN`
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`

## Manual Steps

1. Create ECS Cluster and update `env.ECS_CLUSTER` in `release.yml`
2. Create a task definition that matches your needs and update `.aws/task-definition.json`
3. Create a service or update the task definition to match your needs.
4. In a lot of cases the service name is using `${{ github.event.repository.name }}` - This might not be your case.
