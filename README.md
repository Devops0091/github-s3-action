<h2 align="center">
  Deploy to S3 and CloudFront for Node.js App
</h2>

<div align="center">
  <img alt="AWS Logo" src="https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg" width="100" />
</div>

<br/>

<center>

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/your-username/your-repo-name/Deploy%20to%20S3%20and%20CloudFront?style=for-the-badge)

</center>

## Overview

This GitHub Action automates the deployment of your Node.js application to Amazon S3 and CloudFront on each push to the main branch.

## Workflow Details

The workflow is triggered on every push to the `main` branch. Here's an overview of the workflow steps:

1. **Checkout repository:** This step checks out the repository code for the workflow to run on.

2. **Set up AWS CLI:** Configures AWS CLI with the provided access keys and region using GitHub Secrets.

3. **Set up Node.js:** Sets up the desired Node.js version for the workflow.

4. **Install dependencies:** Installs necessary global dependencies using npm.

5. **Install Build Dependencies:** Installs project-specific dependencies using yarn.

6. **Build:** Builds the Node.js application. Uncomment the `export CI=false` line if treating warnings as errors needs to be temporarily disabled.

7. **Deploy to S3:** Syncs the build artifacts with the specified S3 bucket.

## Usage

To use this GitHub Action in your repository, create a YAML file (e.g., `.github/workflows/deploy-to-s3.yaml`) and copy the provided workflow code into it. Make sure to set up the required secrets in your GitHub repository settings.
