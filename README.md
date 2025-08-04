# 🚀 DockerHub CI/CD Pipeline with GitHub Actions

This project demonstrates a simple CI/CD pipeline using **GitHub Actions** to build and push Docker images to **DockerHub**. It automates the process of logging in to DockerHub, building the Docker image, and pushing it to your repository whenever changes are pushed to the main branch.

## 📦 Features

- Automatic DockerHub login using GitHub secrets
- Docker image build and tag
- Push to DockerHub on every commit to `main`
- Easy integration with other deployment platforms

## 🛠️ Setup Instructions

### 1. Clone the Repository

bash
git clone https://github.com/TechnicalGaur/nodejs-demo-app-cicd/
cd nodejs-demo-app-cicd


2. Add GitHub Secrets
Go to your repository → Settings → Secrets and variables → Actions, and add the following secrets:
| Name | Description | 
| DOCKER_USERNAME | Your DockerHub username | 
| DOCKER_PASSWORD | Your DockerHub password or token | 


💡 If you use 2FA on DockerHub, generate a Personal Access Token and use it as your password.


3. Workflow File
Ensure your .github/workflows/docker.yml (or similar) contains the following login step:

- name: Log in to DockerHub
  run: echo "${{ secrets.DOCKER_PASSWORD }}" | docker login -u "${{ secrets.DOCKER_USERNAME }}" --password-stdin

4. Customize Docker Image
    Edit your Dockerfile to how your app should be build

5. Push Changes
git add .
git commit -m "Initial commit with DockerHub CI/CD"
git push origin main

6. 📤 Image Deployment
Once pushed, your Docker image will be available at:

docker pull your-username/your-image-name:latest



7. Resouce

 Absolutely, Prashant! Based on the debug logs you shared, it looks like your project involves a GitHub Actions workflow that logs into DockerHub—likely to build and push Docker images. Here's a sample README.md tailored for a project like that. You can customize it further based on your app's purpose and tech stack:

# 🚀 DockerHub CI/CD Pipeline with GitHub Actions

This project demonstrates a simple CI/CD pipeline using **GitHub Actions** to build and push Docker images to **DockerHub**. It automates the process of logging in to DockerHub, building the Docker image, and pushing it to your repository whenever changes are pushed to the main branch.

## 📦 Features

- Automatic DockerHub login using GitHub secrets
- Docker image build and tag
- Push to DockerHub on every commit to `main`
- Easy integration with other deployment platforms

## 🛠️ Setup Instructions

### 1. Clone the Repository

bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name


2. Add GitHub Secrets
Go to your repository → Settings → Secrets and variables → Actions, and add the following secrets:
| Name | Description | 
| DOCKER_USERNAME | Your DockerHub username | 
| DOCKER_PASSWORD | Your DockerHub password or token | 


💡 If you use 2FA on DockerHub, generate a Personal Access Token and use it as your password.

3. Workflow File
Ensure your .github/workflows/docker.yml (or similar) contains the following login step:
- name: Log in to DockerHub
  run: echo "${{ secrets.DOCKER_PASSWORD }}" | docker login -u "${{ secrets.DOCKER_USERNAME }}" --password-stdin


4. Customize Docker Image
Edit your Dockerfile to define how your app should be built.
5. Push Changes
git add .
git commit -m "Initial commit with DockerHub CI/CD"
git push origin main


📤 Image Deployment
Once pushed, your Docker image will be available at:
docker pull your-username/your-image-name:latest


📚 Resources
- GitHub Actions Documentation
- DockerHub
- Dockerfile Reference

8. 💬 Contributing
Feel free to fork the repo, open issues, or submit pull requests. Contributions are welcome!


9. SCREENSHOT

     <img width="1341" height="587" alt="Screenshot 2025-08-04 133119" src="https://github.com/user-attachments/assets/08070133-5f8c-4fee-b9cb-2ad8e37f0b28" />


    <img width="912" height="687" alt="Screenshot 2025-08-04 133239" src="https://github.com/user-attachments/assets/ac5e1462-ca73-457c-bb0b-4582287358d0" />


    <img width="1337" height="612" alt="Screenshot 2025-08-04 133312" src="https://github.com/user-attachments/assets/e5c31e6c-4240-4ae5-aa82-80bbbbc00e8d" />



     

   



  


