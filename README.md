# Cloud Formation
Trambo Cloud- Ejercicio 5
### Autor: Jhosef Omar Cáceres Aguilar

La arquitectura consiste en una vpc con 6 subredes, tres de ellas son privadas y las otras son públicas, también se dispone de un EFS que será montado en las instancias que se crear en el auto scaling group junto a un balanceador de carga con un Launch Configuration.
 
## Servicios utilizados

| Servicio     | Descripción 
| :---          |    :----  
| VPC    | Configuraciones de red     
| AG    | Auto scaling group que contiene las configuraciones para el auto escalado de EC2     
| EFS    | Sistema de archivos que contiene la página web     
| LB    | Balanceador de carga que trabaja en conjunto con el launch configuration.
| LC    | Configuración de las especificaciones de la máquina a lanzar en el Auto-Scalig group          
```
http://localhost:3000/obtenerEstadoLlegadaPiloto
```


# Archivo - main
Template que une los servicios antes indicados.

## Parámetros


| Parámetro     | Descripción | Tipo 
| :---          |    :----   |    :----  
| VPCName    | Nombre de la VPC  | String   
| BucketName    | Bucket donde se encuentran | String almacenados los templates | String 

## Recursos

| Recurso     | Descripción | Tipo 
| :---          |    :----   |    :----  
| VPC    | Configuraciones de red | AWS::CloudFormation::Stack   AWS::CloudFormation::Stack 
| EFS | Sistema de archivos  |  AWS::CloudFormation::Stack  | AWS::CloudFormation::Stack
| LaunchConfig  | Configuración para el auto scaling group  |  AWS::CloudFormation::Stack  | AWS::CloudFormation::Stack
| LoadBalancer    |  Balanceador de carga  | AWS::CloudFormation::Stack
| WebServerGroup    |  Auto scaling group | AWS::CloudFormation::Stack


## Diagrama de la arquitectura
![Diagram](AWS.png)