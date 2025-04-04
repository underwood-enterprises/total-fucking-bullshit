# Setting Up GitHub Pages

We've updated the GitHub Pages deployment to use a more reliable approach. The new workflow will:

1. Create a `gh-pages` branch (if it doesn't exist)
2. Deploy the contents of the repository to that branch
3. Configure GitHub Pages to serve from that branch

## Enable GitHub Pages in Repository Settings

After the workflow runs successfully, follow these steps to ensure GitHub Pages is properly enabled:

1. Go to your GitHub repository: https://github.com/underwood-enterprises/total-fucking-bullshit
2. Click on the "Settings" tab (near the top right)
3. Scroll down to the "GitHub Pages" section (or click on "Pages" in the left sidebar)
4. Under "Source", select "Deploy from a branch"
5. In the "Branch" dropdown, select "gh-pages" and "/ (root)"
6. Click "Save"

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

### Issue: "Repository not found" or authentication errors
- Solution: Make sure the workflow has the correct permissions (contents: write) in the workflow file.

## After Fixing Issues

Once you've made the necessary changes, you can manually trigger the workflow:

1. Go to the "Actions" tab
2. Click on "Deploy to GitHub Pages" in the left sidebar
3. Click "Run workflow" dropdown
4. Select the branch (usually "master") and click "Run workflow"

Your blog should be available at: https://underwood-enterprises.github.io/total-fucking-bullshit/ once the deployment is successful and you've configured GitHub Pages to serve from the gh-pages branch.
