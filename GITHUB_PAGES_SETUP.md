# Setting Up GitHub Pages

If you're experiencing issues with the GitHub Pages deployment, follow these steps to ensure GitHub Pages is properly enabled for your repository:

## Enable GitHub Pages in Repository Settings

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

### Issue: "Error: Unable to find the GitHub Pages source branch"
- Solution: Make sure you've selected "GitHub Actions" as the source in the GitHub Pages settings.

### Issue: "Error: The process '/usr/bin/git' failed with exit code 128"
- Solution: Check that the workflow has proper permissions to access the repository.

### Issue: "Error: The deploy step encountered an error: Error: Failed to deploy to GitHub Pages"
- Solution: This could be due to various reasons. Check the detailed logs for more information.

## After Fixing Issues

Once you've made the necessary changes, you can manually trigger the workflow:

1. Go to the "Actions" tab
2. Click on "Deploy to GitHub Pages" in the left sidebar
3. Click "Run workflow" dropdown
4. Select the branch (usually "master") and click "Run workflow"

Your blog should be available at: https://underwood-enterprises.github.io/total-fucking-bullshit/ once the deployment is successful.
