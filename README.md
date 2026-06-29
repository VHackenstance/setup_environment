<h3>Setup Environment</h3>
<p>A single script to set up the basics for testing OnPath Attacks
</p>
<h4>Running this script to test Bettercap sslstrip.  Firstly</h4>
<ol>
    <li>run arp_spoof.py, test against target vm using arp -a</li>
    <li>run packet_sniffer.py, test against http test sites</li>
    <li>run setup_environment, which is main.py</li>
</ol>
You CAN do all this manually by the way.
<h4>UPDATE: This does work, but only if you type in the actual domain name</h4>
You have to give the server the opportunity to connect to the http service
<br/>
first, otherwise, for example if you click a https link, it just goes to 
<br/>
HTTPS.  I have not tested against raw IP Addresses.  
<h4>What is happening in the script</h4>
<ol>
    <li>Checking Port Forwarding. Enable Port Forwarding.</li>
    <li>Set IP Tables.
        <br/>
        I set both local and remote because there is no conflict and why not.
    </li>
    <li>Start Bettercap on eth0, but there is an option to change interface.</li>
    <li>Listen for Ctrl+C and when we get it shut it all down.</li>
    <li>You need to Ctrl+C arp_spoof and packet_sniffer separately</li>
</ol>
<h4>UPDATE: RVM connection bug.</h4>
There can be a connect to the internet bug on remote targets,
<br/>
This can be cleared with restart of Kali Linux, something to do about 
<br/>
a cache bug - iptables, scapy...  all of it.