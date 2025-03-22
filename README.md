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
