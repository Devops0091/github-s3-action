<h1 align="center">
  🚀 Deploy to S3 and CloudFront for Node.js App
</h1>

<div align="center">
  <img alt="AWS Logo" src="https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg" width="100" />
</div>

<br/>

<p align="center">
  <img alt="GitHub Workflow Status" src="https://img.shields.io/github/workflow/status/your-username/your-repo-name/Deploy%20to%20S3%20and%20CloudFront?style=for-the-badge">
</p>

## Overview

Automate the deployment of your Node.js application to Amazon S3 and CloudFront with this GitHub Action on each push to the main branch.

## Workflow Details

The workflow is triggered on every push to the `main` branch. Here's an overview of the workflow steps:

1. **Checkout repository:** This step checks out the repository code for the workflow to run on.

2. **Set up AWS CLI:** Configure AWS CLI with the provided access keys and region using GitHub Secrets.

3. **Set up Node.js:** Set up the desired Node.js version for the workflow.

4. **Install dependencies:** Install necessary global dependencies using npm.

5. **Install Build Dependencies:** Install project-specific dependencies using yarn.

6. **Build:** Build the Node.js application. Uncomment the `export CI=false` line if treating warnings as errors needs to be temporarily disabled.

7. **Deploy to S3:** Sync the build artifacts with the specified S3 bucket.

## Usage

To use this GitHub Action in your repository, create a YAML file (e.g., `.github/workflows/deploy-to-s3.yaml`) and copy the provided workflow code into it. Make sure to set up the required secrets in your GitHub repository settings.

