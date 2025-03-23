# DockerProject
- **Project Overview**
- **Project Structure**
- **Steps**



📌 **Project Overview** 
We target to dockerize BOTH apps - the Python and the Node app and apply below actions:

1) Create appropriate images for both apps (two separate images).

2) Launch a container for each created image, and making sure that the app inside the container works correctly and is usable.

3) Re-create both containers and assign names to both containers. Use these names to stop and restart both containers.

4) Clean up (remove) all stopped (and running) containers,clean up all created images.

5) Re-build the images - this time with names and tags assigned to them.

6) Run new containers based on the re-built images, ensuring that the containers are removed automatically when stopped.
   

📂 **Project Structure**

  │── dockerLearning/  
  
    ├── Docker_Project 
     ├── node-app                        # Node Application folder
      ├── dockerfile                     # Docker configuration
      ├── package.json                   # Application dependency
      ├── server.js                      # Application source code 
      ├── images                         # images for output
     ├── python app                      # Python Application folder  
      ├── dockerfile                     # Docker configuration 
      ├── bmi.py                         # Application source code  
     ├── instruction.txt                 # Requirments
    ├── README.md                        # Project details


 🎯 **Steps**

| Questions   | First image                  | Second image  |
|------------|-------------------------------|------------|
| Q1         |cd node-app/ <br>docker build .    | cd python-app/ <br>docker build .   |
| Q2         | docker images<br>docker run -p 8000:3000 image_ID     | docker images<br>docker run -it image_ID     |
| Q3         | docker run  -p 8000:3000 --name containerName image_ID<br>docker stop containerName<br>docker start containerName    | docker run -it --name containerName image_ID<br>docker stop containerName<br>docker start containerName     |
| Q4         | clean containers: <br> docker ps -a<br> docker rm container_name1 container_name2<br>clean images:<br>docker images<br>docker rmi image_name1 image_name2<br>docker image prune    |     |
| Q5         |cd node-app/<br> docker build -t node-demo:latest .   | cd python-app/<br>docker build -t python-demo:1 .     |
| Q6         | docker run -p 8000:3000  -d -—name nodeapp -—rm node-demo     | docker run -it -—name pythonnode -—rm python-demo:1     |



