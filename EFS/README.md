# EFS

Creates a new file system (EFS)

 
## Parameters

| Parameter | Description | Type 
| :--- | :---- | :----  
| VPC | VPC ID | String   
| Subnet6 | Public Subnet | String
| SGName | Security Group Id | String  
| EFSName | Name of EFS | String
## Resources

| Resource | Description | Type 
| :--- | :---- | :----  
| InstanceSecurityGroup | Security Group | AWS::EC2::SecurityGroup 
| MountTarget | Mount | AWS::EFS::FileSystem 


## Outputs

| Name | Description 
| :--- | :----   
| idEFS | EFS Id 
| IdSecurityGroup | Security Group Id 