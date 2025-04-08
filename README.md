<h1>Common Networking Commands</h1>
While I was studying for my Network+ I made this write up of five of the most common networking commands and their uses. <br />


<h2>Environments and Technologies Used</h2>

- PowerShell

<h2>Operating Systems Used </h2>

- Windows 11

<h2>Deployment and Configuration Steps</h2>

<p>
Knowledge of networking commands is essential for anyone working in IT and also a good to know for any computer-savvy individual. Basic knowledge of commands will allow for some simple troubleshooting of network issues, help manage networks, and for me the most important is an improved understanding of how networks function.

In this post, I go over five of the most common commands and some functions that they are used for. I made this post as a way to help study for my Network+ exam and I feel that writing a post for others to see helps solidify your knowledge. I look forward to any feedback anybody might have.

1. Ping

Ping is the only command that I knew prior to starting my studies and is with out a doubt one of the most common commands. Ping is used to test the connectivity and reachability of a device on a network. You can ping an IP address or a server (such as google.com).
</p>

![Screenshot 2025-03-24 201132](https://github.com/user-attachments/assets/f07dcb1a-aeea-496c-b50b-e87489ef4463)


<p>
This will send four ICMP echo requests which will either get a reply (the connection works!) or time out. If you get a time out that is a sign your network connection could have a problem or perhaps the server you reached out to is down. Try to ping another device and see what response you get.
</p>

![Screenshot 2025-03-24 201335](https://github.com/user-attachments/assets/3111c25d-869d-4e1d-9b3e-71d2c4dffe7e)


<p>
IP address 10.0.0.2 is not assigned in my network therefore when I send a ping request, I get the message, "Destination host unreachable."

A common address to ping is 127.0.0.1 which is called a loopback address. This will test the functionality of your current machine itself. If this fails then it is safe to assume that you have a networking issue.
</p>

![Screenshot 2025-03-24 201731](https://github.com/user-attachments/assets/51caa528-2c69-4172-907e-c829c6931f99)

<p>
2. Ipconfig/ Ifconfig
  
Ipconfig (Windows) or ifconfig (Linux/macOS) is a common command that displays network configuration for your local host. Using the following commands for the respective operating system will provide information on your current IP address, subnet mask, default gateway, and DNS server addresses.

ipconfig /all on Windows or ifconfig -a on Linux/macOS
</p>

![Screenshot 2025-03-24 201920](https://github.com/user-attachments/assets/ba2e6c03-8f5f-4721-b465-776bb54cb147)

<p>
The terminal shows information about the computers current configuration this can be use for troubleshooting network connectivity issues.

Some common issues that could come up are an incorrect IP address, subnet mask or default gateway. These could happen when a DHCP server is down or perhaps an IP address is supposed to be automatically assigned to a network but the device is set to manual or vise versa.

Understanding the information using ipconfig will be a great help when it comes to adjusting network settings and troubleshooting based on what you find.

3. Tracert/ Traceroute
   
Tracert (Windows) or traceroute (Linux/macOS) traces the routes that packets take to reach a destination host. This command will show each hop a packet takes to reach its destination which can help identify where a connection may be failing. You can use this route with a domain name or an IP address as follows:

tracert google.com - traceroute google.com - traces route to Google's servers
tracert 8.8.8.8 - traceroute 8.8.8.8 - traces route to Google's public DNS server
</p>

![Screenshot 2025-03-24 202528](https://github.com/user-attachments/assets/e8683a5f-6862-40e0-904d-223374cf6c6a)

<p>
Tracert is commonly used when you can't connect to a website or server to diagnose where the connection is failing. This can be used to see if there is a routing issue withing your organization or perhaps this is an issue with an ISP.

It is also a good practice to use tracert for testing after making changes to your network such as adding or removing new devices.

4. Nslookup
   
Nslookup is used to query Domain Name Server (DNS) to resolve domain names to IP addresses or vice versa. 

The most common use of nslookup is to resolve domain names to IP addresses. Providing a domain name the command queries the configured DNS server to find an IP address.

For example:
nslookup google.com - will resolve the domain name "google.com" to its IP address(es)
</p>

![Screenshot 2025-03-24 202828](https://github.com/user-attachments/assets/11393f66-84d3-478c-8f8e-2001aadb3f25)


<p>
A reverse lookup is used to find a domain name associated with an IP address. For example, running the command nslookup 8.8.8.8 will resolve to the Google DNS server.
</p>

![Screenshot 2025-03-24 202918](https://github.com/user-attachments/assets/ec401711-9143-4d77-924d-4508c894bb96)


<p>
This command can also help to troubleshoot DNS server issues. Say your unable to access a website, using nslookup can help determine if there is a problem with your DNS server configuration. If nslookup fails to resolve domain names it could indicate a settings issue.

5. Netstat / SS
   
Netstat (Windows) or SS (Linux) is a useful command that displays active network connections, listening ports and network statistics.

Running the command: netstat -a

You will see all of your machines active connections. This shows both inbound and outbound connections, including the protocol (TCP or UDP), local address and port, remote address and port, and connection state.
</p>

![Screenshot 2025-03-24 203151](https://github.com/user-attachments/assets/8e8ad059-2306-4146-9c26-7de740844cfa)


<p>
Running the command: netstat -l

Will give you a list of different commands you can run with netstat, where you can filter content based on protocol, specific ports, and many more combinations.
</p>

![Screenshot 2025-03-24 203831](https://github.com/user-attachments/assets/1647d4f9-73df-47f2-8f10-c8ec121cc5ab)


<p>
These commands can be useful for detecting suspicious connections or listening ports that might indicate malware or just simply let you know which applications are using excessive bandwidth.

Obviously there are hundreds of networking commands I didn't cover that are valuable to use to troubleshoot connection problems or monitor network traffic. I'm excited to learn more about networking and be able to use these commands when the occasion arises.
</p>
