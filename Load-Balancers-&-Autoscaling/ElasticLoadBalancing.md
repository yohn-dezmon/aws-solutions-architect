Application Load Balancer is a type of ELB.  

Types of Elastic Load Balancers:
- Application Load Balancer
- Network Load Balancer 
- Gateway Load Balancer

HTTP - port 80  
HTTPS - port 443

Health Checks:
- defined at LB level 
- `/health` -- you ping the application and have an expected response (e.g. status_code=200)

Application Load Balancer:
- HTTP, HTTPS, HTTP2, WebSocket
- can redirect (HTTP -> HTTPS)
- Used to balance load for specific applications 
- an "application" is determined by a target group

Target Group:
- can be a single container, various EC2 instances, IP addresses, ECS services, Lambda functions, etc. 

Listener Rules:
- can have a priority 
- 1 is highest 50,000 is lowest
- default just forwards data from a source to an output port 
- determines flow of traffic across a load balancer
- this is where hostname, path, status code, etc. come into play 

Security Groups:
- firewalls that allow given ports on the LB to receive traffic
- you can set the source for a listener to be a security group as opposed to another application 

IP Addresses & Target Groups:
- target groups don't know the IP address of the client
- this can be retrieved via the HTTP Header "X-Forwarded-For"


