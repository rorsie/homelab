<h1>Homelab</h1>

<h2>Description</h2>
Project consists of a repurposed laptop running an Ubuntu Server 22+ OS. I began this project before creating this page, so some sections may not be as complete. I have gone through the creation of this server with the help of online guides and videos. Some uses and applications I have configured are remote SSH via OVPN, Pi-Hole, and the built-in UFW
<br />


<h2>Languages and Utilities Used</h2>

- <b>Linux CLI</b> 
- <b>Pi-hole</b>
- <b>SSH</b>
- <b>Open VPN</b>
- <b>Linux UFW</b>
- <b>Docker</b>
- <b>More to come</b>

<h2>Environments Used </h2>

- <b>Ubuntu Server Version 22.x</b>

<h2>Project walk-through:</h2>

<p align="center">
<h3>Initial setup</h3> <br/>
I decided to opt for a physical server as that is my preference and I felt it would be more of a challenge to set up and get running, instead of using any preconfigurations with cloud software. I had an Acer laptop lying around that my father never used, so it seemed like the perfect piece of hardware to repurpose into something useful. The first thing I did was physically integrate it into my SOHO network by simply using a category 5e ethernet cable and plugging it into my nice little tplink switch. <br/>
 It had Windows 11 installed on it, but obviously that was not going to do. I opted for an Ubuntu server since it was completely free and it would give me more experience with Linux as a whole, also it would be more lightweight. Configuration was fairly simple, but I did have some <a href="https://www.youtube.com/watch?v=2Btkx9toufg">help</a> to make sure nothing would instantly destroy itself. I made sure to give it a static IP too, so I could always easily access it from my other computers. After creating another account, so that I was not always in root, and make sure all the packages were updated. it was pretty much sqaured away for me to start adding programs and experimenting. 
<br />
<br />
<h3>Programs</h3> <br/>
 <p align="center">
  SSH is the first thing I had to test out. I had only used it before in some tryhackme.com labs, but was eager to try it on my own creation. I know its relatively simple, but being able to securely access my server from my desktop or other laptop seemed (and still seems) so cool to me. I used the PuTTY application on my Windows desktop since I liked its simplicity. I made a profile for the server to make connecting even faster. Shortly after, I discovered I could add an RSA key pair to my desktop and server to make it even more secure. I used PuTTYgen to generate an RSA public and private key that I could share with the server. After moving my mouse around a bit to create some randomiziation, it was complete! It was a little tricky adding it to the server, but thanks to the video I mentioned earlier I found the corret configuration file and editied it with the SCP protocol. I also edited to configuration to disallow password connections, so it would only allow connections from those who had the RSA keys that I put in the configuration file. Being able to securely connect to the server from my desktop was cool and all, but I had a laptop which I used for studying at my workplace and I thought it would be even better if I could connect from my workplace to my server at home, securely of course. This brings me to....
<br />
 OpenVPN was what I chose to provide a secure tunnel from wherever my laptop may be back to my server at home.
<br />
Pictures and descriptions coming soom (TM)!
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
