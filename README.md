
# Project Title
Kubernetes-based Book Shop Application Deployment with Istio, Canary Deployment, and mTLS for Enhanced Security and Observability using Kiali

## Description:

This project demonstrates the deployment of a **book shop application** on a Kubernetes cluster running on **Docker Desktop.** The deployment incorporates **Istio** for service mesh management, enabling advanced networking features like **canary deployments** and **mTLS (mutual TLS)** for secure communication between services. Additionally, **Kiali** is used to monitor and observe the mesh network, providing real-time insights into traffic flows, service health, and security policies.

## Tools and Technologies Used
- Docker Desktop
- Kubernetes
- Docker
- Istio
- Canary Deployment
- mTLS (Mutual TLS)
- Kiali
- Admission controller

## Flow Diagram

![P06](https://github.com/user-attachments/assets/158fe90c-2e80-4f16-b62b-6b2cf160cd90)


# Key Components and Tools

## Docker Desktop Kubernetes
The Kubernetes cluster is set up locally using Docker Desktop to provide a development environment for deploying and managing the application and service mesh.

Kubernetes is responsible for orchestrating the book shop microservices and managing the lifecycle of containers.

## Book Shop Application
A simple book shop application composed of multiple microservices (e.g., catalog, orders, payments).

Each service is containerized using Docker and deployed in the Kubernetes cluster.

NodePort or Ingress is used to expose the application for external access.

## Istio Service Mesh
Istio is installed to manage the network traffic between microservices, enabling advanced networking features such as traffic management, security, and observability.

Istio provides features like load balancing, service discovery, and traffic splitting.

## Canary Deployment
The canary deployment strategy is used to gradually roll out a new version of the book shop application.

In a canary deployment, a small percentage of traffic is initially routed to the new version, allowing real-time monitoring of performance and errors before fully deploying it.

If the new version performs as expected, Istio will gradually route more traffic to it until the old version is replaced.

## Mutual TLS (mTLS)
mTLS is implemented using Istio to ensure encrypted communication between microservices.

This secures internal traffic within the cluster, as both the client and server must authenticate each other during the handshake.

mTLS provides strong security measures, preventing eavesdropping and man-in-the-middle attacks within the service mesh.

## Observability with Kiali
Kiali is an observability tool integrated with Istio to visualize service mesh architecture and traffic flow.

It provides insights into the health of microservices, showing metrics like success rates, error rates, and latencies.

Kiali offers a real-time graphical representation of how traffic flows through the mesh and highlights any security policies (e.g., mTLS) being enforced.

# Project Workflow
## Kubernetes Cluster Setup with Docker Desktop
Docker Desktop is used to set up a local Kubernetes environment, providing a platform for deploying and managing the book shop application and Istio service mesh.

## Book Shop Application Deployment
The book shop application is deployed as multiple microservices, each responsible for a distinct function (e.g., book catalog, user management, and payment processing).

Docker images for the microservices are created and deployed in the Kubernetes cluster.

The application is exposed externally using NodePort or Ingress, depending on the configuration.

## Istio Installation
Istio is installed in the Kubernetes cluster to manage and secure inter-service communication.

Istio components such as the pilot, mixer, and proxy sidecars are injected into the book shop application’s microservices to handle traffic routing and security policies.

## Canary Deployment
When a new version of the book shop application is ready, it is deployed alongside the current version.

Istio is configured to split traffic between the current version and the new version using a canary deployment strategy.

Traffic is gradually shifted from the old version to the new version based on performance metrics and user feedback.

## Mutual TLS (mTLS) Configuration
Istio is configured to enforce mTLS between the microservices, ensuring secure communication.

This prevents unauthorized access to internal services and ensures that all communications are encrypted.

## Monitoring and Observability with Kiali
Kiali is deployed to provide a detailed view of the service mesh, including traffic flows, security policies, and service health.

Kiali's dashboard offers real-time insights into how traffic is distributed across microservices, especially useful during the canary deployment process.

Any mTLS issues or traffic anomalies are immediately visible, allowing quick identification of potential problems.

# OUTPUT
## Docker Desktop Kubernetes
![Screenshot (298)](https://github.com/user-attachments/assets/87f14f54-b7ec-481c-84e2-65fd5046a8e1)

## Istio Installation
![Screenshot (300)](https://github.com/user-attachments/assets/60af6b63-2399-4192-8c2c-65f7473b589f)
![Screenshot (301)](https://github.com/user-attachments/assets/3bd51cd9-9ed0-422d-84dd-57ab9a0a6240)
![Screenshot (302)](https://github.com/user-attachments/assets/949fc66c-ff1e-4c3b-861b-37b1957e7e6b)
![Screenshot (305)](https://github.com/user-attachments/assets/d3970910-22ec-4cf9-adb7-cf26a38bad88)


## Book Shop Application Development
![Screenshot (306)](https://github.com/user-attachments/assets/78d05134-b023-42ba-a955-429000659a14)
![Screenshot (307)](https://github.com/user-attachments/assets/484a3e5d-553a-4061-9d57-04324dc07d64)
![Screenshot (308)](https://github.com/user-attachments/assets/8d7f9a84-db59-410b-b2b2-abcd09e297cb)
## Sidecar Container
![Screenshot (309)](https://github.com/user-attachments/assets/f2198f5e-9119-4a91-941e-7a217490281b)
![Screenshot (310)](https://github.com/user-attachments/assets/64beef37-f84c-4548-bade-084451fe8f2e)
![Screenshot (311)](https://github.com/user-attachments/assets/4eb79565-299f-40d8-bd35-ade49666ebec)

## Gateway Installation
![Screenshot (312)](https://github.com/user-attachments/assets/b9fd5605-0ace-490b-817d-f869fd6c30fa)

## Application OUTPUT
![Screenshot (313)](https://github.com/user-attachments/assets/f955a000-938b-4055-93ae-717590114081)
![Screenshot (314)](https://github.com/user-attachments/assets/c88fc0cc-159c-4bb5-ae83-2bde250e0c2e)

## Application Version updates Deployment
![Screenshot (321)](https://github.com/user-attachments/assets/d64e3acd-9d9d-4ce3-9789-b85506270d16)

# Mutual TLS (mTLS) Configuration

## without mTLS
![Screenshot (322)](https://github.com/user-attachments/assets/9ecfa424-5837-48ce-9029-8d3fb1106e05)
![Screenshot (323)](https://github.com/user-attachments/assets/a27380f1-f36e-461d-a381-c4277bf7f2af)

## mTLS configuration
![Screenshot (330)](https://github.com/user-attachments/assets/2976402d-e9cf-40b9-bb3c-80d2a194bb36)
![Screenshot (328)](https://github.com/user-attachments/assets/9acbf354-3289-4c81-a54e-cebf8166d853)
![Screenshot (329)](https://github.com/user-attachments/assets/a98096c5-5996-482e-a622-c175baf15958)

# Canary Release Deployment
## Varchuval Service
![Screenshot (337)](https://github.com/user-attachments/assets/329483a4-12f8-49db-990c-22c363ab5a90)

## Traffic Shifting
![Screenshot (338)](https://github.com/user-attachments/assets/450dc264-e093-4c50-bde2-a9c5466eed1a)

## destination Rule
![Screenshot (339)](https://github.com/user-attachments/assets/e3da25bd-7cab-4dae-ab7c-6c0ddf6fbc7c)

## Application Review Version 50 old-50 new %
![Screenshot (340)](https://github.com/user-attachments/assets/e08e9713-ffe2-4a00-b98b-4331bb1d22df)
![Screenshot (344)](https://github.com/user-attachments/assets/c7c835a6-2d96-485b-af93-8a69b9f1a34b)
![Screenshot (344)](https://github.com/user-attachments/assets/d438d806-fe7b-44c5-8782-1cf44ece7d19)
![Screenshot (345)](https://github.com/user-attachments/assets/4b4b374b-2d8e-4f9a-9061-fc9e881b215b)
![Screenshot (346)](https://github.com/user-attachments/assets/4c63e5da-194d-44a0-8e98-81455566de3e)

## Observability Kiali Configuration
![Screenshot (350)](https://github.com/user-attachments/assets/f4d03899-5d85-4932-9cd4-56db2e17403f)
![Screenshot (352)](https://github.com/user-attachments/assets/449592ad-4e88-4d4e-a895-2c891bc59ba7)
![Screenshot (353)](https://github.com/user-attachments/assets/55937f0b-cdba-49e8-b0e4-119bfaf59044)
![Screenshot (354)](https://github.com/user-attachments/assets/4ce969fc-d2ca-4d8a-ab02-e0fa492538c1)
![Screenshot (355)](https://github.com/user-attachments/assets/733fa2c8-0f2b-43c7-b836-51fdb31b48be)
![Screenshot (358)](https://github.com/user-attachments/assets/a6b03efe-a735-4cd3-8b6f-baa604dafe53)
![Screenshot (359)](https://github.com/user-attachments/assets/fb953852-d6c9-43d4-92b6-f8270ec5238e)
![Screenshot (360)](https://github.com/user-attachments/assets/2a2f0f9e-8fbb-453f-b451-124925842402)
![Screenshot (363)](https://github.com/user-attachments/assets/1b691db6-7fe0-4b8f-abca-2700af45b7f3)





**This project demonstrates the deployment of a book shop application on a Kubernetes cluster managed by Docker Desktop. Using Istio, the project implements canary deployments, ensuring safe and gradual application updates, and enforces mTLS for secure communication between microservices. Observability is enhanced with Kiali, providing a comprehensive view of the service mesh architecture, traffic flows, and security policies. This setup is ideal for testing microservice-based applications with advanced networking and security features locally before moving to production.**


# **Thank you.......**
