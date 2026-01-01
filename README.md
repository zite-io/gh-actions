# gh-actions

A tiny toolbox of GitHub composite actions.

## What’s inside

- **`.github/actions/ecr-build-push-action`**  
  Build a Docker image and push it to **AWS ECR**.
  Docs: see the action’s own `README.md`.

- **`.github/actions/deploy_to_ecs`**  
  Deploy recently pushed image to respective **AWS ECS**. 
  Docs: see the action’s own `README.md`.

## Usage

```yaml
- uses: zite-io/gh-actions/.github/actions/action-name@v1.0.0
  with:
    AWS_REGION: ap-south-1
    AWS_ROLE_ARN: arn:aws:iam::123456789012:role/GitHubOidcEcrPushRole
    ECR_REPOSITORY: my-service
    IMAGE_TAG: latest
    DOMAIN: app.zite.io
## Other inputs as needed
```

## Tip
Always use a tag (`@v1.0.0`) instead of `@main`
