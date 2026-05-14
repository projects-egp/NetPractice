_This project has been created as part of the 42 curriculum by \<enrgil-p\>_

  <h2 id="top">Index</h3>
  <ol type ="1">
    
  <li><a href="#description">Description</a></li>
  <li><a href="#instructions">Instructions</a></li>
  <li><a href="#resources">Resources</a></li>
</ol>
<h1 id="description">Description</h1>

NetPractice is an introduction to basics of computer networking. In this project, 42's students are asked to not only
learn about concepts like TCP/IP, netowrk routes and subnet masks, IP directions, OSI model, etc; but also test how this would be used
in order to configure hypothetical small-scale networks.

Therefore, you will find the 10 exercises I have done with this simulated cases. Networking concepts learned are explained in this README.md file, at **<a href="#resources">Resources</a>** section.

<h1 id="instructions">Instructions</h1>

<h3>How to run training interface</h3>
At evaluation 

<h1 id="resources">Resources</h1>

<h2>Concepts</h3>

  <h4>IP - Internet Protocol</h4> Standard protocol to communicate devices and networks. It's routing functions allows to interconnect multiple networks. IP delivers packets from one host to another. Network nodes 'see' which is the destination because this packets have it's destination at headers.
  <ul><li>"<b>Internet Protocol</b>". Wikipedia®, CC BY-SA <https></https>https://en.wikipedia.org/wiki/Internet_Protocol</https></li></ul>

---
  
  <h4>IPv4</h4> Fourth version of Internet Protocol. IPv4 addresses 32 bits, so it allows 4.294.967.296 unique adresses to identify internet devices. As long as this amount of addresses will not be enough to manage internet in future, exists sine 90's IPv6, which use addresses based in 128 bits, this means, 340 undecillion (340.282.366.920.938.463.463.374.607.431.768.211.456) unique adresses.
  Nowadays, IPv4 still be the most common version. 32 bits are divided in 4 bytes, four groups of 8 bits. This bytes are expressed as decimal number between 0 and 255. For example, 12.255.62.254. 
  
  <ul><li><b>"IPv4"</b>. Wikipedia®, CC BY-SA <https>https://en.wikipedia.org/wiki/IPv4</https></li></ul>

  ---
  
   <h4>Subnet Masks</h4>
  An IP address is divided in two parts: first part, the most signficant bits, represent the network (or subnetwork) where it belongs; and second part, bits that represent each device on from a network.
  Number of bits for this parts vary on network size. To represent this different network sizes, there is a way to divide them by classes:
  
  
  <ul><li>Class A: 16.777.214 hosts on a network</li>
      <li>Class B: 65.534 hosts on a network</li>
      <li>Class C: 254 hosts on a network</li></ul>
  
  If IP addresses have 32 bits in IPv4, masks use other 32 bits. Their purpose is to indicate which bits from IP address are part of network prefix, represented in mask with 1 valued bits, and which of them indicates the host identifier, by 0 valued bits. This is done with bitwise AND.
  So, 32 bits, again 4 bytes. With first 18 bits set to '1', for example, a mask could be represented as 255.255.192.0. It is also represented as /18, and can be put together with an IP address, so it represents one device, or a complete netork, with size of this one. For example, 192.10.24.0/24. 
  To know how many host are allowed in a network, we do substraction of 32 bits with the number of 1-bits from mask. For example, /25 means that we have free 32 - 25 == 7 bits. With this 7 bits, we have 2⁷ - 2 hosts, 62. In a network, first IP address is used to refer the whole netwrok, and last address is used for broadcast. That's the reason to why network has 62 possible hosts instead of 64.


  
   <ul><li>"<b>Subnet</b>". Wikipedia®, CC BY-SA <https>https://en.wikipedia.org/wiki/Subnet</https></li>
   <li>"<b>Classless Inter-Domain Routing</b>". Wikipedia®, CC BY-SA <https>https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#IPv4_CIDR_blocks</https></li>
   <li><b>"IPv4 CIDR Visualizer"</b> <https>https://cidr-subnet.netlify.app/</https></li></ul>

---
   
  <h4>Broadcast</h4>
  Method to send a message from one sender node to all possible endpoints. Is used, for eample, when sender doesn't know which host from a network has to receive some packets or datagrams. As said above, every network has a boradcast address, the biggest of the network, which has all host bits with value 1. 
  <ul><li>"<b>Difusión amplia</b>". Wikipedia®, CC BY-SA <https>https://es.wikipedia.org/wiki/Difusi%C3%B3n_amplia</https></li></ul>
  <li>Open Systems Interconnection (OSI) model</li>
  Reference model to coordinate different standards used in networks. Divided in seven abstracion layers, classifies protocols in their respective purposes. For example, famous TCP and IP. These protocols use to work together because they take charge of different needs for connection: IP establish route beetween devices, and TCP guarantees data delivery.
  OSI model's levels are these ones:
  <ul><li>7. Application</li>
    For example, HTTPS<li>6. Presentation</li>Translation of data, enryption/decryption, etc.<li>5. Session</li>Continous exchange of information on a session<li>4. Transport</li><li>3. Network</li><li>2. Data link</li><li>1. Physical</li></ul>
  <h4>TCP/IP</h4>
  <h4>(default) gateway</h4>

<a href="#top">Back to index</a>
