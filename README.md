# Job Info Action

Quick example demonstrating how to get information about a job run from an action.

## Action

The code for the action is in `.github/actions/job_url`. Currently it just prints the HTML URL of the running action,
but that is to demonstrate how to get job-run specific information using the GitHub API.

## Workflow

The calling workflow is in `github/workflows/test.yml`. It calls the action which does job-run specific things. 
The calling workflow must do two critical things:

1. Specify the `actions: read` permission for the GitHub Token
2. Specify the `GH_TOKEN` with the permissions as an env var for the action
