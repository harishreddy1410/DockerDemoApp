# DockerDemoApp
This is the sample webapi application to demonstrate building docker image and running it in a container on a windows machine. 
# Pre-requisites : 
    1) VSCode IDE 
    2) Docker desktop for windows and should be running in your machine
# Steps involved are as follows     
    **dotnet new **
    **dotnet build**
    **dotnet run **
    Test you application and hit Ctrl+C
    **dotnet new gitignore**
    **dotnet publish**

//your sample webapi should be running successfully and dll's are ready 
Please follow the below commands to create a docker image and run your image in a container 

Include the Docker file in the root directory 
Copy paste the **Dockerfile** and **.dockerignore** files from my repo to your solution

  **docker build -t dockerdemoapp .**  #please mentione the repo name in lower case, docker is case sensitive 
  **docker run -d -p 8080:80 --name myapp dockerdemoapp**
you can test the api running either from browser or command prompt 
in case of command prompt you should be able to access it from **curl http://localhost:8080/weatherforecast**
in case of browser you should be able to access it from **http://localhost:8080/weatherforecast**

Once you are able to test your changes, you have successfully containerized the dotnet webapi application. 
You can remove the created image and container by using the below commands 
  **docker ps -a**
  **docker stop myapp**
  **docker rm myapp**

you can test the api running either from browser or command prompt 
in case of command prompt you should be able to access it from **curl http://localhost:8080/weatherforecast**
in case of browser you should be able to access it from **http://localhost:8080/weatherforecast**
