# **PROJECT REPORT**

## **Project Overview**
This project involved developing and deploying a custom WordPress website using a Docker-based local environment and Azure Cloud for production. The goal was to create a functional, easily modifiable website that implements continuous integration and continuous deployment (CI/CD) practices, ensuring every push to the repository automatically updates the live production site.

The site was built using a child theme of the Astra WordPress theme. My contributions focused on enhancing the child theme’s functionality and styling while ensuring a seamless deployment process.


## **Technologies and Tools Used**
- **WordPress**: Theme development through child themes, enabling site customization without altering the core theme. Managed plugin integration to extend the site's functionality.
- **CSS, PHP**: Used for customizing the layout and design of the theme.
- **Docker**: Set up a local development environment using `docker-compose.yml`.
- **Azure Cloud**:  Used for hosting and production deployment. I configured and deployed the WordPress site using Azure App Service. I also set up continuous integration and deployment (CI/CD) using GitHub Actions integrated with Azure for an automated workflow.
- **Azure CI/CD Integration**: Utilized Azure's built-in CI/CD tools to automatically trigger a build and deployment to the live site on every push to the GitHub repository. This workflow minimized manual intervention, ensured a smooth and error-free deployment process, and greatly improved efficiency.
- **GitHub Actions (CI/CD)**: Ensured that each code update in the local environment was automatically deployed to the live website. GitHub Actions provided automated testing, building, and deployment processes.
- **Git & GitHub**: Managed version control and collaboration throughout the project using Git and GitHub.

## **Skills Developed**

### 1. **Full-Stack WordPress Development**
- Gained valuable hands-on experience working on both the front end (WordPress theme customization) and back end (server setup and database management), which provided insight into the broader architecture of modern web applications.

### 2. **Docker**
- Successfully set up local development environments using Docker.

### 3. **Cloud Deployment & Server Management**
- Deployed the website to Azure App Services and configured the web server, gaining experience in cloud deployment. Understanding how to handle the deployment process, monitor performance, and manage environments was an essential takeaway. Initially, I tried to create a virtual machine and set up WordPress manually via SSH. However, after encountering issues with the Ubuntu Default Page, despite several troubleshooting attempts, I opted to use Azure’s WordPress App Service, which streamlined the process and resolved the deployment challenges.

### 4. **CI/CD Practices**
- Implementing a continuous integration/continuous deployment pipeline significantly deepened my understanding of CI/CD practices. These practices are critical in modern web development, as they allow for fast, iterative improvements without downtime or manual intervention. I initially attempted to set up the CI/CD pipeline manually using a custom YAML file, but encountered errors. While searching for the SSH key for GitHub secrets, I discovered that Azure offered a built-in CI/CD setup, which I utilized for seamless automation.

## **Key Challenges and Lessons Learned**

### 1. **Deployment on Azure Virtual Machine**
- The initial approach involved creating a WordPress site manually on an Azure Virtual Machine (VM). Despite correctly configuring the VM and connecting via SSH, the default Apache2 Ubuntu Default Page appeared instead of the WordPress site. I attempted multiple solutions, such as adjusting configuration files, restarting services, and modifying permissions, but the issue persisted.

- Solution: After considerable troubleshooting with no success, I opted to use Azure App Service for WordPress. This provided a quicker, more reliable way to host the WordPress site without manual setup, significantly reducing deployment complexity.

### 2. **CI/CD Pipeline Configuration**
- Setting up the CI/CD pipeline was another challenge, particularly in writing a custom GitHub Actions workflow from scratch. While trying to configure the yaml file, I encountered several errors related to incorrect syntax, file paths, and deployment issues. At first, I attempted to configure the pipeline manually but was met with errors.

- Solution: After struggling with the manual setup of the pipeline, I discovered Azure’s built-in CI/CD Integration in the Azure App Service. By leveraging this tool, I was able to automatically trigger deployments on every push to GitHub without the need for a complex custom script. This greatly simplified the process and ensured a stable deployment pipeline.

  
## **Conclusion**
This project provided extensive experience in modern web development practices, including local development with Docker, cloud deployment with Azure, and automation with CI/CD pipelines. I have gained a deeper understanding of how web development projects are managed, deployed, and maintained across environments.