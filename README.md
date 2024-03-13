# A Mock Landing Page for Nutrition Snap

## Overview

NutritionSnap is an innovative app designed to simplify the process of tracking your dietary intake and making informed nutritional choices. By leveraging advanced image recognition technology, NutritionSnap allows users to quickly and accurately determine the calorie count and macronutrient breakdown of any meal, just by taking a photo with their smartphone.

## Key Features

- **Instant Meal Analysis**: Snap a photo of your meal and receive instant calorie and macronutrient breakdown.
- **Macronutrient Breakdown**: Discover the protein, carbohydrates, and fats in your meal for effective diet balancing.
- **Meal History and Graphs**: Save your meal analyses and track your dietary habits over time with intuitive graphs.
- **Customizable Meal Details**: Input serving sizes and ingredients to enhance analysis accuracy.
- **Multi-Device Sync**: Seamlessly sync data across multiple devices for easy access anywhere.
- **Personalized Recommendations**: Receive tailored recommendations based on dietary goals and restrictions.

## GitHub Actions Workflow

A GitHub Actions workflow is designed to automate the process of building and deploying a Hugo-based static website to GitHub Pages. It is triggered by pushes to the main branch of the repository.

The workflow consists of a single job named deploy, which runs on an Ubuntu 22.04 runner provided by GitHub Actions.

The job includes the following steps:

- Check Out Source Repository: This step checks out the repository's source code, including any submodules (such as Hugo themes) and fetches the entire commit history.
- Initialize Hugo Environment: This step sets up the Hugo environment by installing the specified version of Hugo (0.123.4) with the extended mode enabled.
- Compile Hugo Static Files: In this step, the hugo command is executed to compile the static website files from the source code. The compiled files include draft content, and the output is minified for better performance.
- Publish to GitHub Pages: This final step publishes the compiled website files to the gh-pages branch, which is used by GitHub Pages to host the website. The commit author information is set, and the deployment is authenticated using the GitHub token provided by GitHub Actions. There's also an option to specify a custom domain for the GitHub Pages site, which is currently commented out.
