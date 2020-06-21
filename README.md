# k8s-jenkins

Hello World!

In my previous articles we have seen many examples of deployment integrating docker and jenkins. We felt using this and building this kind of setup is very cool! But we are not keeping in mind the industrial use case and true meaning of deployment. Deployment means there is no human intervention from developer who builds the application to deploy application. If we encounter any intervention it is classified as delivery.

Now, docker is a container service provider that means it helps us with building, distributing and running container. Some of the use case in which we face problem is 

✅Auto Scaling: What if the clients exponentially increase and we have to scale or increase the number of container where our application is running? Manually going and launching container is not a good practice even we can have one monitoring software to look for the traffic and accordingly scale out and scale in. This will again add pain to our head. So we need one unified tool to handle this.
✅Load Balancing: Let's say after scaling if our program is not so intelligent to distribute the traffic to other containers auto scaling is of no use then, hence we need a software which also look for load balancing.
✅Service Discovery: Let's say we scaled out some container for our new clients and we even have load balancing for some existing containers, now how will the load balance program will come to know the IP of the newly created container? In this dynamic world even our IP is not constant, so we even need a program to have capability for service discovery.
✅Reverse Proxy: Let's say we have auto scaled, we have balanced the load, we have service discovery but we cannot give too many IP address to client to connect to our application, no one does that, it's a very bad practice. So, we need a program which takes all the IP of the containers and give us one unique IP.
✅Fault Tolerance: Here fault tolerance means once the container with our application is launched, we don't want our clients to face any down time. Hence we need any system which can have a fault tolerance capability. So, this program have to continuously monitor the container running and if it fails it should automatically launch the new container.

So, I have used Kubernetes integrating it with Jenkins to make our build pipeline more robust. What new you will get in here is:
🔰To download the files from the GitHub
🔰To Classify according to the language of the code
🔰 To deploy it in testing environment and test it
🔰If the test is successful deploy it in production environment
🔰We will additionally create Deployment which will do all the above mentioned industrial use cases. We will also make the storage permanent or persistent so that our clients doesn't loose any data. We will also automatically create the .yaml config file for production. After deploying it in the production environment we will automatically launch it in our browser.

🎫Write-up: https://tinyurl.com/y76qkvoe
