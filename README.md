# Honeypot Deployment with T-Pot on Vultr

## Overview
This project involves setting up a Honeypot using [T-Pot](https://github.com/telekom-security/tpotce) on a cloud-based instance. The deployment was carried out on [Vultr](https://www.vultr.com/) using an Ubuntu 24.04 server.

## Prerequisites
- A Vultr account
- A deployed Ubuntu 24.04 server instance
- SSH access to the server

## Installation Steps

1. **Deploy Ubuntu 24.04 on Vultr**
   - Log in to your Vultr account.
   - Deploy a new cloud instance with Ubuntu 24.04.
   - Ensure the instance has sufficient resources (recommended: at least 8GB RAM and 4 vCPUs).
     <img src="https://github.com/user-attachments/assets/b48b2bb2-eaaf-4c2e-a81c-5eae63ef9a9a" width="700">

2. **Connect to the Server**
   - Use SSH to access the server:
     ```sh
     ssh root@your-server-ip
     ```
<table>
<tr>
<td><img src="https://github.com/user-attachments/assets/34437006-6b7a-4850-aac2-63f9b1f63748" width="700"></td>
<td><img src="https://github.com/user-attachments/assets/045160f7-f0fc-4a6e-8964-73258377aed3" width="700"></td>  
</tr>
</table>

3. **Update and Upgrade System Packages**
   ```sh
   apt update && apt upgrade -y
   ```

4. **Install T-Pot**
   - Navigate to the official T-Pot GitHub repository: [https://github.com/telekom-security/tpotce](https://github.com/telekom-security/tpotce)
   - Run the installation script:
     ```sh
     wget https://github.com/telekom-security/tpotce/raw/master/install.sh
     chmod +x install.sh
     ./install.sh
     ```
   - Follow the installation prompts to complete the setup.

5. **Reboot the Server**
   ```sh
   reboot
   ```

6. **Access T-Pot Dashboard**
   - After rebooting, access the T-Pot web interface at:
     ```
     https://your-server-ip:64297
     ```
     <img src="https://github.com/user-attachments/assets/e9ca83d7-3c2b-41d7-bbd8-62b3651ef1db" withd="700">

   - Log in using the credentials set during installation.
     <table>
<tr>
<td><img src="https://github.com/user-attachments/assets/89927694-6c97-43bc-b406-984e973bff03" withd="700"></td>
<td><img src="https://github.com/user-attachments/assets/5abaabea-8e11-48cd-9d98-fc2a8e6e483e" withd="700"></td>
</tr>
</table>

## Features
- Collects data on malicious activities targeting the server.
- Provides a web-based dashboard for monitoring attacks.
- Includes multiple honeypot services to emulate different types of systems.

 <h2>Monitoring and Analysis</h2>
    <p>Once deployed, T-Pot provides various tools to monitor and analyze attacks in real-time:</p>
    <ul>
        <li><strong>Attack Map:</strong> Displays live attack attempts and scanning activities targeting the honeypot.</li>
        <li><strong>Kibana Dashboard:</strong> Provides an in-depth visualization of collected attack data.</li>
        <li><strong>Kibana Discover Board:</strong> Allows for detailed exploration and filtering of logged attack events.</li>
        <table>
<tr>
       <td><img src="https://github.com/user-attachments/assets/96646f70-716a-43b4-b429-0ab695ea90e4" width="700"></td>
        <td><img src="https://github.com/user-attachments/assets/8f54d550-13c7-405e-9288-eb9ab42ec2df" width="700"></td>
       </tr>
</table>
        <li><strong>Cisco Talos:</strong> Enables checking the reputation and integrity of attacking IP addresses.</li>
        <img src="https://github.com/user-attachments/assets/6610ff04-3f89-4041-afa4-681d0d0d27de" width="700">

  </ul>
    

## Notes
- Ensure that the necessary firewall rules are configured to allow access to the T-Pot dashboard.
- Regularly update T-Pot to maintain security and efficiency.

## Resources
- [T-Pot Documentation](https://github.com/telekom-security/tpotce)
- [Vultr Documentation](https://www.vultr.com/docs/)

