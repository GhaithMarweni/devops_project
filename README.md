# DevOps
**DevOps Mini-Project**

### **Project Overview**
This project focused on containerizing and deploying a MERN stack application using Docker, Kubernetes and Jenkins, The goal was to establish a CI/CD pipeline and deploy the application on a Kubernetes cluster.

---

### **1. Docker Implementation**

#### **Dockerfiles Creation**
- **Backend**: A `Dockerfile` was created for the Node.js backend service.
- **Frontend**: A `Dockerfile` was created for the React-based frontend.
- **MongoDB**: A `Dockerfile` was set up for MongoDB.

#### **Docker Compose**
- A `docker-compose.yml` file was written to orchestrate all three services (backend, frontend, and MongoDB).
- The `docker-compose build` command was used to build the images.
- The `docker-compose up` command was used to create a containerized environment running all three services.


---

### **2. CI/CD Pipeline with Jenkins**

#### **Pipeline Setup**
- Installed and configured Jenkins on the local machine.
- Created a Jenkins pipeline that:
  1. Pulled the source code from the Git repository.
  2. Built the Docker images for the backend and frontend.
  3. Pushed the Docker images to DockerHub.

#### **Tools Used**
- Jenkins plugins: Docker, Git, Pipeline.
- DockerHub for image storage.



---

### **3. Kubernetes Deployment**

#### **Manifests Created**
- **ConfigMap**:
  - `app-config.yaml` was created to store environment-specific configurations.
- **Deployment**:
  - Separate deployment files were created for the backend, frontend, and MongoDB.
- **Service**:
  - Service files were created to expose the deployments and manage interconnectivity.


#### **Commands Used**
- Applied manifests:
  ```bash
 kubectl apply -f kubernetes/frontend-service.yaml
 kubectl apply -f kubernetes/backend-service.yaml
 kubectl apply -f kubernetes/mongo-service.yaml
 kubectl apply -f kubernetes/app-config.yaml
 kubectl apply -f kubernetes/backend.yaml
 kubectl apply -f kubernetes/frontend.yaml
  ```
- Verified resources:
  ```bash
  kubectl get pods,services
  ```

---


### **RESULTS**
- Successfully containerized the MERN stack application using Docker.
- Established a CI/CD pipeline with Jenkins to automate image building and pushing.
- Deployed the application on Kubernetes with separate manifests for backend, frontend.


---

### **Key Learnings**
- Docker and Docker Compose streamlined containerization and multi-service management.
- Jenkins pipelines simplified CI/CD processes.
- Kubernetes provided scalability and reliability for application deployment.


---
