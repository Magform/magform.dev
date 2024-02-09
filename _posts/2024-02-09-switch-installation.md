---
Title: "Switch Planet WGSW-28040 Configuration"
toc: true
categories:
    - Home Lab
tags:
    - Home Lab
    - Networking
    - Switch
    - Configuration
excerpt: "Planet WGSW-28040 switch setup and configuration."
---

# Switch Planet WGSW-28040 Configuration
Hello, everyone! In this post, I'll be sharing the steps I took to configure the Planet WGSW-28040 switch in my Home Lab.\\
Towards the end, I'll also provide my thoughts on this switch, though I won't be able to offer a comprehensive review as I lack the necessary devices to run all the required tests.

## Configuration
For the entire setup, I used only the switch, a computer, and an Ethernet cable to connect them.

### Step 1: Reset everything
To ensure a clean slate for the new configuration, I connected the switch to power and initiated a reset.\\
Holding down the power button for 5 seconds triggers the reset process, signified by the illumination of LAN ports 1,2,3,4 and 5.\\
This step clears any previous configurations, providing a fresh starting point for the setup.

### Step 2: Connect the PC
Next, I connected the computer to the switch using the LAN cable.\\
Since there was no router providing IP addresses with DHCP, I manually set the computer's IP address to 192.168.0.10 (any IP in the range 192.168.0.x with x not equal to 100 is acceptable).

### Step 3: Access the Switch
I opened the browser and navigated to 192.168.0.100 to access the switch's settings. \\
After logging in with the default credentials (admin/admin), I changed the administrator password for added security.\\
To do this, navigate to System -> User configuration, create a new user with the User Name "admin," and set the new password, selecting "encrypted" for additional security.

### Step 5: Set up the Switch IP
Since my router's IP is 192.168.1.1, and I want my switch on the same subnet, I changed the switch's IP to a static 192.168.1.100.\\
Navigate to System -> IP Configuration, change the IP address to 192.168.1.100, and set the Gateway as 192.168.1.1, I then connected the router and re-enabled DHCP on my PC.\\
Additionally, I logged into the new switch page (192.168.1.1) for further configurations.

### Step 6: Save the New Configuration
Given that this is my baseline configuration, and I want it to persist after a reboot, I proceeded to, in the top-left corner, Save -> Save Configuration to Flash set the source as Running Configuration and the destination as Startup Configuration. Apply the changes.

### Step 7: Plug in all
Now, I can connect all my devices to the switch.

### Step 8: Start the fun
You can now start experimenting with the configurations, exploring all the possibilities. If something goes awry, a simple restart is enough to revert to a safe state.

## Conclusion

In conclusion, the switch appears to be quite robust, offering more than sufficient performance for my needs.\\
While having a few 2.5Gb or 10Gb ports would have been nice, considering its release date and the price at which I acquired it, it more than meets my requirements.\\
In terms of configurations, it provides a lot of choices which I hope will allow me to learn something new.

## Useful links

- [User's Manual](https://www.planet.com.tw/storage/products/41091/EM-WGSW-28040_28040P_v1.2.pdf)
- [Product Specification (V3)](https://planet.com.ru/storage/products/48629/PS-WGSW-28040_V3.0.pdf)
- [Official Quick Installation Guide](https://planet.com.tw/storage/products/41039/EMQ-WGSW-28040_v1.1.pdf)