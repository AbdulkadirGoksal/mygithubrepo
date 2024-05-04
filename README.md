# Phonebook Microservice Web Application

The Phonebook Microservice Web Application is designed to provide students with a practical understanding of Microservice architecture by implementing a web application with MySQL Database using Docker and Kubernetes. The project encompasses frontend and backend services interacting with a database service, each managed by Kubernetes deployments. The backend service acts as a gateway, facilitating create, delete, and update operations, while the frontend service enables read operations through a search page. To ensure data persistence, concepts such as persistent volume and persistent volume claim are employed.

## Project Structure

```
Kubernetes-Microservice-Phonebook/
│
├── Initial files/
│   ├── README.md
│   ├── Image_for_web_server/
│   │   ├── app.py      
│   │   ├── requirements.txt              
│   │   └── templates/
│   │       ├── index.html
│   │       ├── add-update.html
│   │       └── delete.html
│   └── image_for_result_server/
│       ├── app.py           
│       ├── requirements.txt              
│       └── templates/
│           └── index.html
│
├── ADD_DELETE_UPDATE/
│   ├── Dockerfile
│   ├── web_server_deployment.yml
│   └── web_server_service.yaml
│
├── SEARCH/
│   ├── Dockerfile
│   ├── result_server_deployment.yml
│   └── result_server_service.yaml
│
├── DATABASE/
│   ├── mysql_deployement.yml
│   ├── mysql_service.yaml
│   ├── persistent_volume.yaml
│   └── persistent_volume_claim.yaml
│
└── SECRETS_CONFIGMAP/
    ├── mysql-secret.yaml
    ├── database_configmap.yaml
    └── servers_configmap.yaml
```

## Kubernetes Objects

### ADD/DELETE/UPDATE Deployment and Service
- **Dockerfile:** Docker configuration for the backend service.
- **web_server_deployment.yml:** Deployment configuration for the backend service.
- **web_server_service.yaml:** Service configuration for the backend service.

### SEARCH Deployment and Service
- **Dockerfile:** Docker configuration for the frontend service.
- **result_server_deployment.yml:** Deployment configuration for the frontend service.
- **result_server_service.yaml:** Service configuration for the frontend service.

### DATABASE Deployment and Service
- **mysql_deployement.yml:** Deployment configuration for the MySQL database.
- **mysql_service.yaml:** Service configuration for the MySQL database.
- **persistent_volume.yaml:** Definition for persistent volume to ensure data persistence.
- **persistent_volume_claim.yaml:** Configuration for persistent volume claim.

### Secrets and ConfigMap
- **mysql-secret.yaml:** Definition for MySQL database credentials.
- **database_configmap.yaml:** Configuration for database settings.
- **servers_configmap.yaml:** Configuration for server settings.

### Horizontal Pod Autoscale
Horizontal pod autoscale for both web server and result server is implemented.

Please feel free to adjust and expand upon this README as needed for your project documentation.
