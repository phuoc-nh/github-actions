## Github actions advantages

- Fully integrated with Github.
- Respond to any Github event.
- Community-powered workflows.
- Support any language, framework, and platform.

## Key functionalities
- Run workflows on Linux, Windows, MacOS, and Docker containers.
- Streaming, searchable logs
- Native secrets management.
- Easy to write and share workflows.


## Events
- Github triggered events: push, pull_request, comments, commit.
- Scheduled events: cron jobs.
- Manual events: workflow_dispatch.

## Workflows
- YAML file that defines a set of actions.
- Located in the .github/workflows directory.
- Actions run in VMs or containers.
## Actions
- Reusable units of code.
- Administrative features allow you to control access to your actions.
- Shareable in the Github marketplace.
- Chainable actions are preferred.

## Troubleshooting
- Action debugging: ACTIONS_STEP_DEBUG & ACTIONS_RUNNER_DEBUG.
- VS Code extension for Github actions.

## Best practices
- Versioning actions.
- Documentation actions: showing needed parameters, what the action does, and how to use it.
- Write unit tests for actions.

## A popular CI Workflow
- Use a reusable action to check out the code.
- Set up language environment by a reusable action (Node.js, Python, etc.).
- Run install dependencies, test in Shell
- Upload artifacts, docker images, etc.
- Use super-linter to check rules.

## A popular CD Workflow in the context of containerized applications
- Use a reusable action to authenticate with the container registry.
- Pull the image from the registry.
- Deploy the image

## Secret management
- Organization level secrets: affect all repositories, not available in free plan.
- Repository level secrets: Scoped to a single repository, can be used to override organization-level secrets. Free plan available.
- Environment level secrets: Scoped to a single environment, can be used to override repository-level secrets.
- Workflow could have up to 100 secrets.
- Secrets are limited to 64KB.
## Environment management
- Logical representation of the deployment environment (dev, staging, prod).
- Environment protection rules: require approval, wait for checks, etc.
- Environment secrets: scoped to a single environment.