# OnlineLearn
Simple Startup Website


Link *************************************http://13.82.219.34****************************



Hosted on azure 
*****************************************************************************************

     +++Note I used Azure Portal for all activities


Resorces Used 

    1] Virtual Machine as server in differnt region - 4 VM / 2 In US + 2 In India
    2] Load Balancer 
    3] Traffic Manager

******************************************************************************************

    Steps To Host it On azure
        
       1] Deploy Two Virtual Machine In Us & Two in India (Which acts as Server for us)
   helpfull link https://docs.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal 
    
       2] ssh into it
       3] install apache2 into all 4 vm for hosting web-application
       
       4] into each vm- into networking option on portal add inbound rule for port 80/8080
   helpfull link https://docs.microsoft.com/en-us/azure/virtual-machines/windows/nsg-quickstart-portal    
         
         
       5] add subnet in virtual network of us server
   helpfull link https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-manage-subnet
   
   
       6] put load balancer on top of vm which is application gateway
          - taget type= virtual machine and add its ip
          - add backend in that gateway
          - add routing rule
          - create
   
   helpfull link https://docs.microsoft.com/en-us/azure/load-balancer/quickstart-load-balancer-standard-public-portal?tabs=option-1-create-load-balancer-standard
   
          
       7] now from step 5 to 6 do the same for indian server also
       
       
       
       8] Now its time for traffic manager
       
       9] Create traffic manager
            - Important 
              add routing method = geographic
            - configure it as to connect to load balancer
            - add end point for us and indian server 
      
   helpfull link https://docs.microsoft.com/en-us/azure/traffic-manager/quickstart-create-traffic-manager-profile
