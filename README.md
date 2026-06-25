<h3>Setup Environment</h3>
<p>A single script to set up the basics for testing OnPath Attacks
</p>
<h4>Running this script to test Bettercap sslstrip.  Firstly</h4>
<ul>
    <li>run arp_spoof, test against target vm using arp -a</li>
    <li>run packet_sniffer, test against http test sites</li>
</ul>
<h4>Now we run our script here</h4>
run <b>sudo python main.py</b> from the setup_environment folder.
<br/>
What is going on under  the hood, you CAN do all this manually by the way.
<ol>
    <li>Check Port Forwarding. Enable Port Forwarding.</li>
    <li>Set IP Tables.
        <br/>
        I set both local and remote because there is no conflict and why not.
    </li>
    <li>Start Bettercap on eth0, but there is an option to change interface.</li>
    <li>Listen for Ctrl+C and when we get it shut it all down.</li>
    <li>You need to Ctrl+C arp_spoof and packet_sniffer separately</li>
</ol>
<h4>UPDATE: Tested and works fine</h4>
On certain sites, those that don't have HSTS strictly implemented, and then
<br/>
When you type the domain name into the address bar, rather than click a link
<br/>
from a search engine etc.  Not tested against raw IPs.
<h4>UPDATE: RVM connection bug.</h4>
There can be a connect to the internet bug on remote targets,
<br/>
This can be cleared with restart of Kali Linux, something to do about 
<br/>
a cache bug - iptables, scapy...  all of it.