# notify-workflow-error-action

Action to notify the failure of GitHub Actions Workflow to a GitHub Issue.

Using this action, you can notice the failure of your schedule workflow quickly.
This action uses a GitHub Issue for notification.
If the workflow fails, this action posts a comment to the issue and re-open the issue if the issue is close.
If the workflow succeeds and the issue is open, this action closes the issue.
Otherwise, this action does nothing.

## Example

```yaml

```

## Inputs

### Required Inputs

- issue_number: GitHub Issue Number

### Optional Inputs

Nothing.

## Outputs

Nothing.

## LICENSE

[MIT](LICENSE)
