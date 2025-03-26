<h1>Honeypot Deployment with T-Pot on Vultr</h1>

<h2>Overview</h2>
<p>This project involves setting up a Honeypot using <a href="https://github.com/telekom-security/tpotce&quot;&gt;T-Pot&lt;/a> on a cloud-based instance. The deployment was carried out on <a href="https://www.vultr.com/&quot;&gt;Vultr&lt;/a> using an Ubuntu 24.04 server.</p>

<h2>Prerequisites</h2>
<ul>
<li>A Vultr account</li>
<li>A deployed Ubuntu 24.04 server instance</li>
<li>SSH access to the server</li>
</ul>

<h2>Installation Steps</h2>

<h3>1. Deploy Ubuntu 24.04 on Vultr</h3>
<ul>
<li>Log in to your Vultr account.</li>
<li>Deploy a new cloud instance with Ubuntu 24.04.</li>
<li>Ensure the instance has sufficient resources (recommended: at least 4GB RAM and 2 vCPUs).</li>
</ul>

<h3>2. Connect to the Server</h3>
<pre><code>ssh root@your-server-ip</code></pre>

<h3>3. Update and Upgrade System Packages</h3>
<pre><code>apt update && apt upgrade -y</code></pre>

<h3>4. Install T-Pot</h3>
<p>Navigate to the official T-Pot GitHub repository: <a href="https://github.com/telekom-security/tpotce&quot;&gt;T-Pot GitHub</a></p>
<pre><code>
wget https://github.com/telekom-security/tpotce/raw/master/install.sh
chmod +x install.sh
./install.sh
</code></pre>
<p>Follow the installation prompts to complete the setup.</p>

<h3>5. Reboot the Server</h3>
<pre><code>reboot</code></pre>

<h3>6. Access T-Pot Dashboard</h3>
<p>After rebooting, access the T-Pot web interface at:</p>
<pre><code>https://your-server-ip:64297&lt;/code&gt;&lt;/pre>
<p>Log in using the credentials set during installation.</p>

<h2>Features</h2>
<ul>
<li>Collects data on malicious activities targeting the server.</li>
<li>Provides a web-based dashboard for monitoring attacks.</li>
<li>Includes multiple honeypot services to emulate different types of systems.</li>
</ul>

<h2>Notes</h2>
<ul>
<li>Ensure that the necessary firewall rules are configured to allow access to the T-Pot dashboard.</li>
<li>Regularly update T-Pot to maintain security and efficiency.</li>
</ul>

<h2>Resources</h2>
<ul>
<li><a href="https://github.com/telekom-security/tpotce&quot;&gt;T-Pot Documentation</a></li>
<li><a href="https://www.vultr.com/docs/&quot;&gt;Vultr Documentation</a></li>
</ul>



