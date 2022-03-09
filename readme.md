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
      slack_webhook_url: <snip>
      aws_role: arn:aws:iam::688865856606:role/apps-master-a4e1ebd
      aws_region: us-east-1
      task_definition_family: bff-template
      ecr_repository: bff-50e8673
      ecs_cluster: naro-bff-7b5b24b
      ecs_service: bff-8c13d47
      dockerfile_path: ./bff/dockerfile # Optional; defaults to dockerfile
```
