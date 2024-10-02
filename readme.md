# **README**

## 1. Theme Development

### Overview:
The CMS-tc theme is a custom child theme built on top of the Astra parent theme. The child theme introduces styling and functionality modifications to fit the U3A Townsville website's design needs. This child theme allows for custom changes while maintaining the integrity of the Astra parent theme, making future updates to Astra seamless without losing customizations.

### Features of the Child Theme:
- **Custom Styling**: The child theme overrides Astra’s default styles with custom CSS to reflect the branding of U3A Townsville.
- **Enhanced Header and Footer**: Customizations have been made to the header and footer for a more unique design that fits the overall theme.
- **Typography Adjustments**: Modified fonts and font sizes for better readability and aesthetic appeal.
- **Button Styles**: Customized button styles and hover effects to make the UI more interactive and visually appealing.

### Key Files:
- `style.css`: Contains all the custom CSS for the child theme. This is where any new style changes should be added.
- `functions.php`: This file is responsible for enqueueing the parent theme styles and adding additional functionality if needed.

### How to Make Changes:
1. **Editing the Styles**:
   - To change the theme’s appearance, modify the `style.css` file in the child theme directory. Add or update CSS rules to adjust the site’s look and feel.
   - Example CSS snippet to change header color:
     ```css
     .site-header {
       background-color: #004ea2 !important;
     }
     ```
   
2. **Adding PHP Functionality**:
   - If you need to add custom functionality (e.g., enqueueing new scripts or adding custom functions), update the functions.php file as needed.

### Local Development:
1. Set up a local WordPress development environment (Vagrant or Docker).
2. Clone the project repository to your local machine
3. Make changes to the theme as needed and test them locally by refreshing the site in your browser.


## 2. Deployment

### Overview:
This project uses a Continuous Deployment (CD) workflow using GitHub Actions and Azure App Service. Every time changes are pushed to the main branch on GitHub, the updated theme is automatically deployed to the live site hosted on Azure.

### Deployment Workflow:
Prerequisites:
Azure App Service: Ensure the Azure App Service is set up for hosting WordPress site.
GitHub Repository: All theme code is stored and managed in a GitHub repository.

Automated Deployment with GitHub Actions:
The repository is configured to automatically deploy changes to Azure using GitHub Actions. The deployment pipeline is triggered on every push to the main branch.

### Steps for Deployment:
1. Pushing Changes to GitHub:
	- After making changes to the theme (updating style.css or functions.php), commit and push your changes to the main branch
2. GitHub Actions Workflow:
	- The push to the main branch will automatically trigger the GitHub Actions workflow, which builds and deploys the theme to the Azure App Service.
3. Monitoring the Deployment:
	- You can monitor the progress of the deployment by checking the Actions tab in your GitHub repository.
	- The deployment logs will show whether the build was successful or if there were any issues during deployment.

### GitHub Actions Workflow
The deployment is handled by a GitHub Actions YAML file located at .github/workflows/main_troy-wp.yml in the repository. This file is configured to:
1. Trigger: On any push to the main branch.
2. Build: Pulls the latest changes from GitHub, installs dependencies, and prepares the theme for deployment.
3. Deploy: Uses the Azure Web App Deploy action to push the theme to Azure.
