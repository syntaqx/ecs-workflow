# Docker ECS Workflow

## Manual Steps

1. Create ECS Cluster and update `env.ECS_CLUSTER`
2. Create a task definition that matches your needs and update `.aws/task-definition.json`
3. Create a service for the task definition to land on that matches your needs
4. In a lot of cases the service name is using `${{ github.event.repository.name }}` - This might not be your case.
