&lt;h1&gt;Honeypot Deployment with T-Pot on Vultr&lt;/h1&gt;

&lt;h2&gt;Overview&lt;/h2&gt;
&lt;p&gt;This project involves setting up a Honeypot using &lt;a href=&quot;https://github.com/telekom-security/tpotce&quot;&gt;T-Pot&lt;/a&gt; on a cloud-based instance. The deployment was carried out on &lt;a href=&quot;https://www.vultr.com/&quot;&gt;Vultr&lt;/a&gt; using an Ubuntu 24.04 server.&lt;/p&gt;

&lt;h2&gt;Prerequisites&lt;/h2&gt;
&lt;ul&gt;
    &lt;li&gt;A Vultr account&lt;/li&gt;
    &lt;li&gt;A deployed Ubuntu 24.04 server instance&lt;/li&gt;
    &lt;li&gt;SSH access to the server&lt;/li&gt;
&lt;/ul&gt;

&lt;h2&gt;Installation Steps&lt;/h2&gt;

&lt;h3&gt;1. Deploy Ubuntu 24.04 on Vultr&lt;/h3&gt;
&lt;ul&gt;
    &lt;li&gt;Log in to your Vultr account.&lt;/li&gt;
    &lt;li&gt;Deploy a new cloud instance with Ubuntu 24.04.&lt;/li&gt;
    &lt;li&gt;Ensure the instance has sufficient resources (recommended: at least 4GB RAM and 2 vCPUs).&lt;/li&gt;
&lt;/ul&gt;

&lt;h3&gt;2. Connect to the Server&lt;/h3&gt;
&lt;pre&gt;&lt;code&gt;ssh root@your-server-ip&lt;/code&gt;&lt;/pre&gt;

&lt;h3&gt;3. Update and Upgrade System Packages&lt;/h3&gt;
&lt;pre&gt;&lt;code&gt;apt update &amp;&amp; apt upgrade -y&lt;/code&gt;&lt;/pre&gt;

&lt;h3&gt;4. Install T-Pot&lt;/h3&gt;
&lt;p&gt;Navigate to the official T-Pot GitHub repository: &lt;a href=&quot;https://github.com/telekom-security/tpotce&quot;&gt;T-Pot GitHub&lt;/a&gt;&lt;/p&gt;
&lt;pre&gt;&lt;code&gt;
wget https://github.com/telekom-security/tpotce/raw/master/install.sh
chmod +x install.sh
./install.sh
&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Follow the installation prompts to complete the setup.&lt;/p&gt;

&lt;h3&gt;5. Reboot the Server&lt;/h3&gt;
&lt;pre&gt;&lt;code&gt;reboot&lt;/code&gt;&lt;/pre&gt;

&lt;h3&gt;6. Access T-Pot Dashboard&lt;/h3&gt;
&lt;p&gt;After rebooting, access the T-Pot web interface at:&lt;/p&gt;
&lt;pre&gt;&lt;code&gt;https://your-server-ip:64297&lt;/code&gt;&lt;/pre&gt;
&lt;p&gt;Log in using the credentials set during installation.&lt;/p&gt;

&lt;h2&gt;Features&lt;/h2&gt;
&lt;ul&gt;
    &lt;li&gt;Collects data on malicious activities targeting the server.&lt;/li&gt;
    &lt;li&gt;Provides a web-based dashboard for monitoring attacks.&lt;/li&gt;
    &lt;li&gt;Includes multiple honeypot services to emulate different types of systems.&lt;/li&gt;
&lt;/ul&gt;

&lt;h2&gt;Notes&lt;/h2&gt;
&lt;ul&gt;
    &lt;li&gt;Ensure that the necessary firewall rules are configured to allow access to the T-Pot dashboard.&lt;/li&gt;
    &lt;li&gt;Regularly update T-Pot to maintain security and efficiency.&lt;/li&gt;
&lt;/ul&gt;

&lt;h2&gt;Resources&lt;/h2&gt;
&lt;ul&gt;
    &lt;li&gt;&lt;a href=&quot;https://github.com/telekom-security/tpotce&quot;&gt;T-Pot Documentation&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href=&quot;https://www.vultr.com/docs/&quot;&gt;Vultr Documentation&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;


