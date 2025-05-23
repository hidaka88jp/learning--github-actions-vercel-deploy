# Exploring Vercel Deployments with GitHub Actions

<div align="center">
  <p>
    <a href="#overview">Overview</a> •
    <a href="#what-i-learned">What I Learned</a> •
    <a href="#tech-stack">Tech Stack</a> •
    <a href="#installation">Installation</a> •
    <a href="#license">License</a>
  </p>
</div>

## Overview
While working through a Next.js tutorial, I previously deployed a project to Vercel by connecting my GitHub repository through the dashboard. It was simple and almost felt like magic—just pushing to GitHub triggered the deployment.

Later, in my previous portfolio project, I used Firebase Hosting with GitHub Actions and added custom workflow steps to run type checks and tests during deployment. That experience made me realize how valuable it is to have control over the CI process.

Although I’m currently only doing basic deployments with Vercel, I started wondering if I could achieve the same level of flexibility by integrating Vercel with GitHub Actions. Using GitHub Actions gives me more control over the deployment flow, especially if more complex CI steps are needed in the future. So I created a spike project to experiment with deploying to Vercel via its CLI and GitHub Actions.

## What I Learned
- Basic usage and behavior of the **Vercel CLI**:
    - `vercel build` generates a `.vercel/output` directory
    - `vercel deploy --prebuilt` skips Vercel’s internal build and deploys the local output
- How to write **GitHub Actions workflows** for both `production` and `preview` environments
- The full process of **linking Vercel with GitHub Actions**:
    - Generating and using a Vercel Access Token
    - Adding secrets to GitHub for secure authentication
    - Running deploy commands via the CLI
- Setting up a modern development environment for Next.js with:
  - ESLint and Prettier for code quality
  - Husky for pre-commit hooks

## Tech Stack

<table>
  <tr>
    <th>Frontend</th>
    <td>
      <img src="https://img.shields.io/badge/Next.js-2A2833.svg?logo=nextdotjs">
      <img src="https://img.shields.io/badge/Tailwind CSS-4C5359.svg?logo=tailwindcss">
    </td>
  </tr>
  <tr>
    <th>Deployment</th>
    <td>
      <img src="https://img.shields.io/badge/Vercel-2A2833.svg?logo=vercel">
      <img src="https://img.shields.io/badge/GitHub Actions-4C5259.svg?logo=githubactions">
    </td>
  </tr>
  <tr>
    <th>Dev Tools</th>
    <td>
      <img src="https://img.shields.io/badge/VS Code-4C5259.svg?">
      <img src="https://img.shields.io/badge/ESLint-2A2833.svg?logo=eslint">
      <img src="https://img.shields.io/badge/Prettier-59554C.svg?logo=prettier">
      <img src="https://img.shields.io/badge/Husky-4C4D59.svg">
    </td>
  </tr>
</table>

## Installation

If you want to run this project locally, clone the repository and install the dependencies:

```bash
git clone https://github.com/hidaka88jp/learning--github-actions-vercel-deploy.git
cd learning--github-actions-vercel-deploy
npm install
npm run dev
```

## License

This project was created for educational and portfolio use.  
Licensed under the [MIT License](./LICENSE). 