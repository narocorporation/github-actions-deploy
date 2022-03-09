# Github Actions

One convenient shopping mall.

#### Using these

In the `uses:` clause use a link as such:

```
narocorporation/github-actions/<some yml file>@master
```

## Service Deploy

Deploys an ECS service.

#### Usage:

```yaml
jobs:
  deploy:
    uses: narocorporation/github-actions/.github/workflows/service-deploy.yml@master
    with:
      # Example values
      aws_region: us-east-1
      task_definition: bff-template
      ecr_repository: bff-50e8673
      ecs_cluster: naro-bff-7b5b24b
      ecs_service: bff-8c13d47
      dockerfile_path: ./bff/dockerfile # Optional; defaults to dockerfile
```

## Typescript Lint

Lints Typescript within a repo, so long as that repo has a `package.json` with a `lint` command.

#### Usage:

```yaml
jobs:
  lint:
    uses: narocorporation/github-actions/.github/workflows/typescript-lint.yml@master
```

## Jest Test

Runs Jest tests on a nodejs repo.

#### Usage

```yaml
jobs:
  test:
    uses: narocorporation/github-actions/.github/workflows/jest-test.yml@master
```
