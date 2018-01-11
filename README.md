# Web Engineering 2017-2018 / Microservices
## Report

The followings pictures show that both microservices are running and registered

![WebServer Microservice](/Screenshots/WebServer.png)
*Webserver microservice log*

![Account Microservice](/Screenshots/Accounts2222.png)
*Account Microservice which runs on 2222 port log*

The following picture proves that the registration service has registered the services

![Registration Service](/Screenshots/Eureka.png)
*Registered services*

The following picture shows the last microservice running on 4444 port. The previous picture proves that it has been registered
[!Account Microservice 2](/Screenshots/Accounts4444.png)
*Account Microservice which runs on 4444 port log*

If the microservice running on the 2222 port is killed, the Web Server will show some failed request as long as Eureka isn't aware that the microservice isn't online. That's because the eureka service will provide one of both microservices to the web server service upon request, so if the killed microservice is provided, the petition will fail. After Eureka takes notice of this, all petitions will be redirect to the online service running on the 4444 port and therefore there will be no more failed requests.
