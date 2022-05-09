Configuration includes a VPC with a private subnets. Scenario of a public-facing web application hosted on ECS, while maintaining back-end servers that aren't publicly accessible. Also the database servers in a private subnet. You can set up security and routing so that the web servers can communicate with the database servers. 

Traffic on public subnets, where facing-app Nginx is installed, passes through the Application Load Balancer.

The instances in the private subnet can access the internet by using a network address translation (NAT) gateway that resides in the public subnet. The database servers can connect to the internet for software updates using the NAT gateway, but the internet cannot establish connections to the database servers. 

# tf_ecs_rds
