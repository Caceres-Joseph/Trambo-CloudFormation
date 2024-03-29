# Cloud Formation
Trambo Cloud- Exercise 5
### Author: Jhosef Omar Cáceres Aguilar

The architecture has a vpc whit 6 subnets, 3 are private, 3 are public subnets, and so we have an EFS, the EFS are used in the instances to create in the auto scaling group together a load balancer whit a launch configuration


## Services

| Service     | Descripción 
| :---          |    :----  
| VPC    | Network configuration     
| AG    | Auto scaling group that contains one or more EC2     
| EFS    | File system that contains the web application     
| LB    |   Load balancer that works together whit the launch configuration
| LC    | Configuration of the specifications of the machine to be launched in the Auto-Scalig group          
```
http://localhost:3000/obtenerEstadoLlegadaPiloto
```


# File - main
Template joining the services listed above.

## Parameters


| Parameter | Description | Type 
| :--- | :---- | :----  
| VPCName | VPC Name | String   
| BucketName | Bucket where the templates are | String stored | String 



## Resources

| Resource | Description | Type 
| :--- | :---- | :----  
| VPC | Network Settings | AWS::CloudFormation::Stack AWS::CloudFormation::Stack 
| EFS | File System | AWS::CloudFormation::Stack | AWS::CloudFormation::Stack
| LaunchConfig | Configuration for auto scaling group | AWS::CloudFormation::Stack | AWS::CloudFormation::Stack
| LoadBalancer | Load Balancer | AWS::CloudFormation::Stack
| WebServerGroup | Auto scaling group | AWS::CloudFormation::Stack


## Diagram of the architecture
![Diagram](AWS.png)
 