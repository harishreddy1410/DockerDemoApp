# DockerDemoApp
This is the sample webapi application to demonstrate building docker image and running it in a container on a windows machine. 
Pre-requisites : 
    1) VSCode IDE 
    2) Docker desktop for windows and should be running in your machine
Steps involved are as follows     
dotnet new webapi
dotnet build
dotnet run 
Test you application and hit Ctrl+C
dotnet new gitignore
dotnet publish

//Here your sample webapi is running successfully and dll's are ready 
//Follow the below commands to create the image and run your image in a container 

Include the Docker file in the root directory 
Copy paste the Dockerfile and .dockerignore files from my repo to your solution

docker build -t vscodeprojects .  #repo name should in lower case
docker run -d -p 8080:80 --name myapp vscodeprojects
docker ps -a
docker stop myapp
docker rm myapp