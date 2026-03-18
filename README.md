
#  $${\color{lightlightblue} \textbf{Docker 🐳}}$$

<img width="1262" height="657" alt="image" src="https://github.com/user-attachments/assets/7fb03208-1d32-4a77-b84c-b50fb166245e" />



# Diff Monolithic vs Microservises Architecture
<img width="1281" height="601" alt="image" src="https://github.com/user-attachments/assets/b6704028-f9e4-4331-a65c-aff79077393a" />

##  ${\color{lightblue} \textbf{ Monolithic \ vs \ Microservises}}$
| Feature        | VM 🖥️              | Container 📦              |
|----------------|--------------------|---------------------------|
| OS             | Full OS per VM     | No OS (shared)            |
| Size           | Heavy (GBs)        | Light (MBs)               |
| Startup        | Slow               | Very fast                 |
| Performance    | Lower              | Near native               |
| Isolation      | Strong             | Moderate                  |
| Resource Usage | High (more CPU/RAM)| Low (efficient sharing)   |
| Portability    | Less portable      | Highly portable (runs anywhere with container runtime) |





${\color{Green} \textbf{1. \ Developement \ Team:}}$ Responsible for writing code

${\color{Orange} \textbf{2. \ Testing \ Team:}}$ Responsible for Testing code

${\color{Red} \textbf{3. \ Operations \ Team:}}$ Responsible for providing infrastructure setup
   
- So all the code is stored or integrated inside github
- We cant deliver code to client directly
  Wwe need to test this code
- So developers will test the code on machine/server where we need to install dependencies like
    - angular-frontend
    - java -backend
    - database server
    - tomcat for app
  so this set up we called as environment

- There are multliple environments present in a project such as
  
  ${\color{Green} \textbf{1. Dev}}$ : Where developers write and test code.
  
  ${\color{Orange} \textbf{2. Test}}$ : Where testers ensure the code works correctly
  
  ${\color{Yellow} \textbf{3. UAT (User Acceptance Testing)}}$ : Where customer will test the product
  
  ${\color{Red} \textbf{4. Prod}}$ : Where the final product runs for end-users.

- Installation of dependencies and particular version of software is a very difficult task
- To avoid these kind of environmental issues we are using docker
- Whatever the softwares we required is install using docker
  
##  ${\color{lightblue} \textbf{ Que. \ What \ is \ Docker \?}}$
${\color{lightblue}  \textbf{Docker}}$ 
- is an open source platform for developing, shipping and running applications in containers.
- containers are lightweight, isolated environments that package application and their dependencies together.
  
  **Benefits**
  - portability
  - scalability
  - consistency
  - resource efficiency







##  ${\color{lightblue} \textbf{Virtual Machines (VMs) \ vs. \  Containers)}}$

| Feature                   | Virtual Machines (VMs)                               | Containers                                     |
|---------------------------|------------------------------------------------------|------------------------------------------------|
| **Architecture**          | Includes the entire OS, virtual hardware, and application | Shares the host OS kernel, includes only the application and its dependencies |
| **Size**                  | Typically large, includes full OS                   | Lightweight, usually in MBs                    |
| **Startup Time**          | Slower, can take minutes                            | Fast, usually in seconds                       |
| **Performance**           | Potential overhead due to full OS virtualization    | Near-native performance, minimal overhead      |
| **Isolation**             | Strong isolation, each VM has its own OS            | Process-level isolation, shares OS kernel      |
| **Resource Efficiency**   | Less efficient, more resources required per VM      | Highly efficient, better resource utilization  |
| **Portability**           | Portable across different environments, but larger in size | Highly portable, easy to move and replicate   |
| **Management**            | Requires hypervisor (e.g., VMware, Hyper-V)         | Requires container runtime (e.g., Docker)      |
| **Deployment Speed**      | Slower deployment due to full OS boot               | Rapid deployment                               |
| **Scalability**           | Scalable, but with more overhead and complexity     | Highly scalable with orchestration tools (e.g., Kubernetes) |
| **Security**              | Strong isolation with separate OS instances         | Shared kernel can pose security risks, but improving |
| **Use Cases**             | Running multiple OS environments, legacy application support | Microservices, agile development, continuous integration/continuous deployment (CI/CD) |
| **Storage**               | Each VM has its own storage                         | Containers can share storage volumes           |
| **Networking**            | Requires network bridging or virtual netwo






<img width="1175" height="678" alt="image" src="https://github.com/user-attachments/assets/537434ed-6c7b-4d71-a247-bb61cfff4279" />
<img width="1285" height="575" alt="image" src="https://github.com/user-attachments/assets/6f20b98e-64a5-4ec5-a680-0740ee1b395e" />
<img width="1365" height="547" alt="image" src="https://github.com/user-attachments/assets/52c25be2-c2e0-4806-a3cb-b54636237476" />
<img width="1542" height="593" alt="image" src="https://github.com/user-attachments/assets/02800600-5a46-4ca0-9b17-8b6e76bbb625" 
##  ${\color{lightblue} \textbf{docker \ architecture}}$ 

<img width="801" height="401" alt="image" src="https://github.com/user-attachments/assets/044a0c54-6aaf-40b8-bdb7-256f626d7b4a" />


##  ${\color{lightblue} \textbf{Installation-Steps  \ (Amazon-Linux)}}$ 


````
sudo yum update -y
sudo yum install -y docker
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker ec2-user
newgrp docker
sudo chmod 777 /var/run/docker.sock
````
````
docker --version
````

##  ${\color{lightblue} \textbf{Installation-Steps  \ (Ubuntu)}}$ 


````
sudo apt update -y
sudo apt install  docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker ubuntu
newgrp docker
sudo chmod 777 /var/run/docker.sock
````
````
docker --version
````



