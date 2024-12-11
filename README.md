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

We will start by visiting https://www.whatismyipaddress.com. Next, open Notepad on your computer and record your physical IP address along with your location, as we will need this information later in the project. <br/>
  
<img src="https://i.ibb.co/RyV78ft/1.jpg" height="80%" width="80%" alt=""/>

<br/>

Next, we will create a VM in Microsoft Azure
<br/>
  
<img src="https://i.ibb.co/PczpNF1/2.jpg" height="80%" width="80%" alt=""/>
<img src="https://i.ibb.co/Rjt8vML/3.jpg" height="80%" width="80%" alt=""/>

<br/>

Next we will log into the VM with Remote Desktop
<br/>
  
<img src="https://i.ibb.co/KzJ9698/4.jpg" height="80%" width="80%" alt=""/>

<br/>

After logging into the VM through the remote desktop, we'll revisit https://www.whatismyipaddress.com. Then, reopen Notepad on your personal computer and note the changes in your physical IP address and location. This difference is due to the RDP functioning like a VPN, essentially tunneling a connection between your personal computer and the Virtual Machine
<br/>
  
<img src="https://i.ibb.co/JnGF0gn/5.jpg" height="80%" width="80%" alt=""/>

<br/>

On our personal computers, we will sign up for the free version of ProtonVPN.
<br/>
  
<img src="https://i.ibb.co/z5jwd3q/6.jpg" height="80%" width="80%" alt=""/>

<br />

After we've created our account, we will download the windows version
<br/>
 
<img src="https://i.ibb.co/7Wg9yCv/7.jpg" height="80%" width="80%" alt=""/>
<img src="https://i.ibb.co/DbD7TgX/8.jpg" height="80%" width="80%" alt=""/>

<br />

Once the download begins, we will install the software. After the installation is complete, it will prompt you to enter the login credentials you just created.
<br/>
  
<img src="https://i.ibb.co/DWzmXXg/9.jpg" height="80%" width="80%" alt=""/>

<br/>

Selecet "Quick Connect" and it the VPN will randomly choose and start your connection
<br/>
  
<img src="https://i.ibb.co/ZgyLhP3/10.jpg" height="80%" width="80%" alt=""/>
<img src="https://i.ibb.co/V2Bdz5B/11.jpg" height="80%" width="80%" alt=""/>

<br/>

Finally, by revisiting the website [WhatIsMyIPAddress.com](https://whatismyipaddress.com) and refreshing the page, we can clearly see that both our IP address and location have been successfully updated. This change confirms that the process we implemented to alter our network identity has been effective.<br/>

  
<img src="https://i.ibb.co/6nmwh7y/12.jpg" height="80%" width="80%" alt=""/>

<br/>



