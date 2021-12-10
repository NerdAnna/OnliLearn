# OnlineLearn
Simple Startup Website


Link *************************************http://13.82.219.34****************************



Hosted on azure 
*****************************************************************************************

Resorces Used 

    1] Virtual Machine as server in differnt region - 4 VM / 2 In US + 2 In India
    2] Load Balancer 
    3] Traffic Manager

******************************************************************************************

    Steps To Host it On azure
        
       1] Deploy Two Virtual Machine In Us & Two in India (Which acts as Server for us)
Here is link might be helpfull https://docs.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal 
       2] ssh into it
       3] install apache2 into all 4 vm for hosting web-application
       4] into each vm- into networking option on portal add inbound rule for port 80/8080
         
       5] add subnet in virtual network of us server
           5]
