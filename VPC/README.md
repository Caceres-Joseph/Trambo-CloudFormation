# VPC

Template generating 6 Subnets (3 private and 3 public) and 2 route-tables  

## Subnet addresses
 
| CIDR | Name | Type |
| :--- | :---- | :--- |
| 10.0.0.0/27 | Private1 | Private |
| 10.0.0.96/27 | Public1 | Public | 
10.0.0.128/27 | Public2 | Public | Public | 
| 10.0.0.160/27 | Public3 | Public | 

## Parameters

| Parameter | Description | Type 
| :--- | :---- | :----  
| VPCName | VPC Name | String   
| Subnet1Name | Name of private subnet 1 | String
| Subnet2Name | Name of private subnet 2 | String  
| Subnet3Name | Name of private subnet 3 | String  
| Subnet4Name | Name of public subnet 4 | String  
| Subnet5Name | Name of public subnet 5 | String  
| Subnet6Name | Name of public subnet 6 | String  
| GatewayName | Gateway Name | String  
| PublicRouteTableName | Public Route Table Name | String  
| PrivateRouteTableName | Private Route Table Name | String   


## Resources

| Resource | Description | Type 
| :--- | :---- | :----  
| VPC | Network Settings | AWS::CloudFormation::Stack    
| Subnet1 | Private Subnet 1 | AWS::EC2::Subnet  
| Subnet2 | Private Subnet 2 | AWS::EC2::Subnet 
| Subnet3 | Private Subnet 3 | AWS::EC2::Subnet 
| Subnet4 | Public Subnet 4 | AWS::EC2::Subnet 
| Subnet5 | Public Subnet 5 | AWS::EC2::Subnet 
| Subnet6 | Public Subnet 6 | AWS::EC2::Subnet   
| InternetGateway | Internet Outlet | AWS::EC2::InternetGateway 
| GatewayToInternet | Internet Gateway | AWS::EC2::VPCGatewayAttachment    
| PublicRouteTable | Public Subnetwork Table | AWS::CloudFormation::Stack    
| PublicRoute | Public Route | AWS::EC2::Route   
| PublicRouteTableAsosociation4 | Partnership with Subnet4 | AWS::EC2::SubnetRouteTableAssociation    
| PublicRouteTableAsosociation5 | Partnership with Subnet5 | AWS::EC2::SubnetRouteTableAssociation    
| PublicRouteTableAsosociation6 | Partnership with Subnet6 | AWS::EC2::SubnetRouteTableAssociation    
| PrivateRouteTable | Table with private subnets | AWS::EC2::RouteTable
| PublicRouteTableAsosociation1 | Partnership with Subnet1 | AWS::EC2::SubnetRouteTableAssociation
| PublicRouteTableAsosociation2 | Partnership with Subnet2 | AWS::EC2::SubnetRouteTableAssociation  
| PublicRouteTableAsosociation3 | Partnership with Subnet3 | AWS::EC2::SubnetRouteTableAssociation   


## Outputs

| Name | Description 
| :--- | :----   
| idVPC | VPC ID 
| IdSubRed4 | Subnet ID Public 4 
| IdSubRed5 | Subnet ID Public 5
| IdSubRed6 | Subnet ID Public 6
