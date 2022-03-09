# Github Actions - Deploy

Reusable action for Naro's standard deployment to ECS via task
definition template.

#### Using

```yaml
jobs:
  deploy:
    uses: narocorporation/github-actions-deploys@master
    with:
      # Example values
      aws_region: us-east-1
      task_definition: bff-template
      ecr_repository: bff-50e8673
      ecs_cluster: naro-bff-7b5b24b
      ecs_service: bff-8c13d47
      dockerfile_path: ./bff/dockerfile # Optional; defaults to dockerfile
```
