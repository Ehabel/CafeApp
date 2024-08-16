# CafeApp

## Assignment 1

In this exercise, you are asked to create a CloudFormation template to set up an architecture
similar to the one you created in the AWS Academy Cloud Architecting Course Module
5 guided lab. The architecture consists of an EC2 instance running a web server deployed
in a public subnet and an RDS instance running MySQL in a private subnet. The web
server running on the EC2 instance accesses the database hosted on the MySQL instance
to retrieve and update data. \
Assignment 1 Marks: 10/10

### Resources:

-   KeyPair
-   VPC
-   PublicSubnet
-   PrivateSubnet
-   PrivateSubnet2
-   InternetGateway
-   AttachGateway
-   RouteTable
-   PublicRoute
-   PublicSubnetRouteTableAssociation
-   NATGatewayEIP
-   NATGateway
-   PrivateRouteTable
-   NATRoute
-   PrivateSubnetRouteTableAssociation
-   PrivateSubnet2RouteTableAssociation
-   InternalTraffic
-   InternalTrafficRule
-   EC2SecurityGroup
-   RDSInstance
-   DBSubnetGroup
-   EC2Instance

## Assignment 2

In this project, you are asked to apply the architectural design principles that you learned
in this unit to design and create a secure, scalable and highly available AWS architecture
for a system with three main components:

-   Web application: The web application is implemented using PHP. It has the same functionality as the Cafe application you have worked on in assignment 1. It listens on port 80. It handles user interactions and displays information through a web interface.
-   API endpoints: The API endpoints are implemented in Python. These endpoints provide programmatic access to product and order information for third-party applications (both internal and external). It listens on port 5000.
-   Database: The web application and the API endpoints access the same database. The database can be hosted on MySQL or MariaDB engine.

Below are the requirements for the solution architure:

-   Web application: The web application should be hosted securely on t2.micro or
    t3.micro EC2 instances. Administrative users should be able to SSH to the instance(s)
    through an bastion host. You must provide high availability to ensure users can consistently
    access the Cafe application with minimal latency. As the usage pattern is
    unpredictable, the target tracking scaling method should be used. The suggested target
    is 50% CPU utilisation. At any time, there should be at least two web application
    instances in two different AZs.
-   API endpoints: The API endpoints should be hosted securly on t2.micro or t3.micro
    EC2 instances. They should also allow SSH connection from the bastion host for configuration
    purpose. You need to ensure high availability and maintain the cost of such
    1
    services by maintaining a fixed number of healthy instances as API endpoints. You
    should select and configure an appropriate scaling method to maintain two healthy
    instances in two different AZs.
-   Database: The database should be hosted securely on RDS instance. The API endpoints
    need read-only access to the database. The web application needs both read
    and write access to the database. It is essential to provide high availability and read
    scalability at the database level.

The report PDF outlines all the resources required to deploy the application to AWS as required by the specification. \
Assignment 2 Marks: 19.75/20

### Resources:

-   VPC
-   API ec2 instance
-   Bastion Host ec2 instance
-   Web server ec2 instance
-   Load balancer 2
-   Target group 2
-   AMI 2
-   Launch template 2
-   2 Autoscaling groups
