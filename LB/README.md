# Load balancer

Create a load balancer

 

## Parameters

| Parameter | Description | Type 
| :--- | :---- | :----  
| Subnet6 | Public Subnet | String   
| LBName | Load Balancer Id | String
| SGName | Id del launch configuration | String  

## Resources

| Resource | Description | Type 
| :--- | :---- | :----  
| ElasticLoadBalancer | Elastic load Balancer | AWS::ElasticLoadBalancing::LoadBalancer


## Outputs

| Name | Description 
| :--- | :----   
| idLB | ElasticLoadBalancer 