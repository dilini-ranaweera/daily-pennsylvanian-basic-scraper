This YAML snippet defines when the GitHub Action should run. Specifically, it says:

on.push.branches: [main]

Run this workflow whenever code is pushed to the main branch.
on.pull_request.branches: [main]

Run this workflow whenever a pull request is opened or updated (e.g., new commits pushed) against the main branch.
*on.schedule - cron: "0 20 * * "

Run this workflow on a schedule defined by the cron expression.
The expression 0 20 * * * means “at minute 0 of hour 20 on every day of the month” — in other words, every day at 20:00 (8 PM) UTC.
In GitHub Actions, scheduled workflows use UTC by default.
In short, the workflow will run:

Any time you push a commit to main,
Any time you create or update a pull request to main,
Once a day at 8 PM UTC.
