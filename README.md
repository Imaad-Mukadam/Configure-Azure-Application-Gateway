# Configure-Azure-Application-Gateway

### **Summary: Deploying Azure Application Gateway for Load Balancing**  

In this project, I configured **Azure Application Gateway** to securely route traffic to a web application. The steps include:  

- **Creating a Virtual Network (VNet)** with **two subnets**:  
  - One for the **Application Gateway**.  
  - One for the **Application (VMs hosting the website)**.  
- **Deploying a Virtual Machine (VM)** in the application subnet.  
- **Connecting to the VM via RDP** and installing the **IIS server** to host a dummy website.  
- **Configuring the Application Gateway** to route traffic to the IIS server.  
- **Retrieving the Public IP of the Application Gateway** to access the hosted website.  

This setup enables **secure, scalable, and efficient web traffic management** using Azure's **Layer 7 load balancing**. 🚀

## Step - 1 

i. Create a virtual Network

![image alt](1.PNG)

ii. I have reserved 64 Ip address for the virtual machine and 64 for the application gateway

![image alt](2.PNG)

iii. Once the virtual Network is done , Lets create a VM , make sure you selected this ports.

![image alt](3.PNG)

iv. Deploy the VM in subnet that you created

![image alt](4.PNG)

## Step- 2 

i. Connect your VM with the RDP

![image alt](5.PNG)

ii. Go into server manager , then click on add roles and features

![image alt](6.PNG)

iii. Install Web Server IIS 

![image alt](7.PNG)

## Step - 3

i. Create Application Gateway, select your virtual network then click on Manage subnet configuration

![image alt](8.PNG)

ii. Click on + subnet , give the name and the left 64 ip address will be asign to this application gateway

![image alt](9.PNG)

iii. Now you can see your subnet is added

![image alt](10.PNG)

iv. Once the basic is configure lets configure the frontends, Just give the public ip name

![image alt](11.PNG)

v. In backend , click on Add backend pool then configure as per shown in the image

![image alt](12.PNG)

vi. host a demo webiste on Web server IIS

![image alt](13.PNG)

vii. Lets configure the configuration part

![image alt](14.PNG)

![image alt](15.PNG)

![image alt](16.PNG)

![image alt](17.PNG)

![image alt](18.PNG)

