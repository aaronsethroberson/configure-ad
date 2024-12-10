<p align="center">
<img src="https://i.imgur.com/nBkHqaM.png" height="80%" width="80%" alt="Setting Up in Azure"/>
<br />

<h1>How to Setup and Use a VPN (ProtonVPN) </h1>

<h2>Description</h2>
In this project, I set up an Azure Virtual Machine (VM) and proceeded to download, install, and use ProtonVPN, a free Virtual Private Network (VPN). <br />
<br />
A VPN establishes secure network connections through encrypted tunnels, offering increased security. They are primarily used for two key purposes: facilitating remote work for organizations and enabling access to otherwise restricted content.
<br/>


<h2>Environments and Utilities Used</h2>

- <b>Microsoft Azure</b>
- <b>ProtonVPN</b>

<h2>Project Walk-through:</h2>

<p align="center">
We will start by visiting https://www.whatismyipaddress.com. Next, open Notepad on your computer and record your physical IP address along with your location, as we will need this information later in the project. <br/>
  
![image](https://github.com/user-attachments/assets/c5c264c2-04f4-4947-b585-9f2f6540a254)

<br/>

<p align="center">
Next, we will create a VM in Microsoft Azure
<br/>
  
![image](https://github.com/user-attachments/assets/721614ea-8a3f-4fbd-b9ab-4845044d7a1e)
![Screenshot 2024-10-01 124446](https://github.com/user-attachments/assets/e445ccb6-0c50-40eb-8ed0-82ad4f8595c1)

<br/>

<p align="center">
Next we will log into the VM with Remote Desktop
<br/>
  
![Screenshot 2024-10-01 125300](https://github.com/user-attachments/assets/8da4cc8e-a0b4-4064-803b-bb373ff70fae)

<br/>

<p align="center"> 
After logging into the VM through the remote desktop, we'll revisit https://www.whatismyipaddress.com. Then, reopen Notepad on your personal computer and note the changes in your physical IP address and location. This difference is due to the RDP functioning like a VPN, essentially tunneling a connection between your personal computer and the Virtual Machine
<br/>
  
![Screenshot 2024-10-01 131800](https://github.com/user-attachments/assets/ba0497aa-6248-4b74-936b-ebe649597c15)

<br/>

<p align="center">
On our personal computers, we will sign up for the free version of ProtonVPN.
<br/>
  
![Screenshot 2024-10-01 133113](https://github.com/user-attachments/assets/dff92a65-aa97-458a-a0c8-0111cdc3aa5b)

<br />

<p align="center">
After we've created our account, we will download the windows version
<br/>
 
![Screenshot 2024-10-01 134118](https://github.com/user-attachments/assets/ca357c8d-6bea-4e89-a3da-5eddeca2b722) 
![Screenshot 2024-10-01 134043](https://github.com/user-attachments/assets/1530fb0e-d382-4a58-96ee-1e072e0b66c8)

<br />

<p align="center">
Once the download begins, we will install the software. After the installation is complete, it will prompt you to enter the login credentials you just created.
<br/>
  
![image](https://github.com/user-attachments/assets/2dc298b4-b29f-4ceb-9cb6-a86b41919515)

<br/>

<p align="center">
Selecet "Quick Connect" and it the VPN will randomly choose and start your connection
<br/>
  
![image](https://github.com/user-attachments/assets/ed35928d-a6c6-4913-ac4f-526a2cccb095)
![Screenshot 2024-10-01 134816](https://github.com/user-attachments/assets/2f088e49-2731-4109-862b-9111fde1f88a)

<br/>

<p align="center">
Now, if we return to the website https://whatismyipaddress.com and refresh the page, we can observe that our IP address and location have changed.
<br/>

  
![Screenshot 2024-10-01 135323](https://github.com/user-attachments/assets/c0e23d92-b9f8-426d-a8f9-df7f3f98f01f)

<br/>

<p align="center">
Finally, we'll visit Google and Disney.com to check for any differences based on the location of your VPN server. You might notice changes such as the language or the URL being different.
<br/>
  
![Screenshot 2024-10-01 135753](https://github.com/user-attachments/assets/cc9b0e13-c973-4e09-906e-161c9f0cfd4b)
![Screenshot 2024-10-01 135840](https://github.com/user-attachments/assets/c07588e8-9dd0-44d3-8d0c-feff4db42280)
![Screenshot 2024-10-01 135952](https://github.com/user-attachments/assets/7f984a6d-4417-4282-a0a0-3c1a10a9a41f)


