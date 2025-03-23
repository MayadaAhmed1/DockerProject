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
  
    ├── nodejs-app-starting-setup 
     ├── dockerfile                        # Docker configuration
     ├── public/                  
       ├── styles.css/                     # Application web format
     ├── package.json                      # Dependencies
     ├── server.js                         # Application source code  
     ├── images                            # Readme images 
    ├── README.md                          # Project details


 🎯 **Steps**

| Questions   | First image                  | Second image  |
|------------|-------------------------------|------------|
| Q1         |cd node-app/ docker build .    | cd python-app/ docker build .   |
| Q2         | Data 5     | Data 6     |
| Q3         | Data 5     | Data 6     |
| Q4         | Data 5     | Data 6     |
| Q5         | Data 5     | Data 6     |
| Q6         | Data 5     | Data 6     |



 |  | First image | Second image  |
| --- | --- | --- |
| Q1 | `cd node-app`/
`docker build .` | `cd python-app/`
`docker build .` |
| Q2 | `docker images`
`docker run -p 8000:3000 image_ID` | `docker images
docker run -it image_ID` |
| Q3 | `docker run  -p 8000:3000 --name containerName image_ID

docker stop containerName
docker start containerName` | `docker run -it --name containerName image_ID

docker stop containerName
docker start containerName` |
| Q4 | **clean containers :** 
docker ps -a
docker rm container_name1 container_name2

**clean images:**
docker images
docker rmi image_name1 image_name2

docker image prune |  |
| Q5 | `cd node-app`/
`docker build -t node-demo:latest .` | `cd python-app/`
`docker build -t python-demo:1 .` |
| Q6 | `docker run -p 8000:3000  -d -—name nodeapp -—rm node-demo` | `docker run -it -—name pythonnode -—rm python-demo:1` |
