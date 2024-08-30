# notify-workflow-error-action

GitHub Action to notify the failure of GitHub Actions Workflow to a GitHub Issue.

It posts a comment and re-open the issue if the workflow fails.

![re-open](https://github.com/user-attachments/assets/2ba93003-c1b6-43ba-ac3b-5cbbc39e3c21)

And it closes the issue if the workflow succeeds.

![close](https://github.com/user-attachments/assets/6036e3ed-760b-46c4-87a0-1f07be01d01a)

## Motivation

If you run a workflow periodically by schedule event, you need to notice when the workflow has something wrong.
This action posts a comment to an issue, then you can receive the notification quickly via email or somehow.

## Example

```yaml
- uses: suzuki-shunsuke/notify-workflow-error-action@main
  if: always()
  with:
    issue_number: "225"
    status: ${{ job.status }}
```

## Inputs

### Required Inputs

- `issue_number`: GitHub Issue Number
- `status`: The status of the current job or workflow
  - If the value is `success`, the action closes the issue
  - If the value is `failure`, the action re-open the issue
  - Otherwise, the action does nothing. So if the value is `cancelled` or `skipped`, the action does nothing

### Optional Inputs

Nothing.

## Outputs

Nothing.

## LICENSE

[MIT](LICENSE)
