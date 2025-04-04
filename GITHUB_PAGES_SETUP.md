# Setting Up GitHub Pages

We've completely revised the GitHub Pages deployment approach:

1. The `gh-pages` branch is now the default branch for the repository
2. All content is directly stored in this branch
3. A GitHub Actions workflow automatically deploys changes to GitHub Pages

## Enable GitHub Pages in Repository Settings

Follow these steps to ensure GitHub Pages is properly enabled:

1. Go to your GitHub repository: https://github.com/underwood-enterprises/total-fucking-bullshit
2. Click on the "Settings" tab (near the top right)
3. Scroll down to the "GitHub Pages" section (or click on "Pages" in the left sidebar)
4. Under "Source", select "GitHub Actions" as the build and deployment source
5. Click "Save"

## Verify Workflow Permissions

1. While still in the repository settings, click on "Actions" in the left sidebar, then "General"
2. Ensure that "Read and write permissions" is selected under "Workflow permissions"
3. Make sure "Allow GitHub Actions to create and approve pull requests" is checked
4. Click "Save"

## Check Workflow Status

1. Go to the "Actions" tab in your repository
2. Look for the most recent "Deploy to GitHub Pages" workflow run
3. Click on it to see the detailed logs and identify any specific errors

## Common Issues and Solutions

### Issue: "Error: The process '/usr/bin/git' failed with exit code 128"
- Solution: Check that the workflow has proper permissions to access the repository.

### Issue: "Error: The deploy step encountered an error"
- Solution: This could be due to various reasons. Check the detailed logs for more information.

## Making Changes

Since `gh-pages` is now the default branch, you should:

1. Always pull the latest changes before making edits: `git pull origin gh-pages`
2. Make your changes directly to the files
3. Commit and push to the `gh-pages` branch: `git push origin gh-pages`
4. The GitHub Actions workflow will automatically deploy your changes

Your blog should be available at: https://underwood-enterprises.github.io/total-fucking-bullshit/ once the deployment is successful.
