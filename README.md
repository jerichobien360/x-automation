# x-automation

Docker and n8n checks using GitHub Actions.

## Run the workflow

1. Open the repository's **Actions** tab.
2. Select **Docker and n8n check**.
3. Click **Run workflow**, choose `main`, and confirm the run.
4. Open the run and expand the job steps to see Docker and n8n versions.

The check also runs automatically when `.github/workflows/docker-n8n.yml` changes on `main`.

## What it runs

- Uses GitHub's Ubuntu runner, which includes Docker.
- Runs the official `n8nio/n8n:latest` image with `--version`.
- Removes the container when the command finishes.
- Stops the job after 10 minutes if it has not finished.

This is a container check. It does not provide an n8n editor URL, execute a custom n8n workflow, or host an always-on n8n instance.
