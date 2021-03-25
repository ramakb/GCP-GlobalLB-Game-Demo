A WebGL maze game built with Three.js and Box2dWeb. 
Credits & Source from: https://github.com/wwwtyro/Astray and LearnGCPWithMahesh

# Simple game which is used for hands-on project like a real time project experience
# Game application on Google Compute Engine or Managed Instance Group
### Launching the VM

1. Provision a Google Compute Engine (GCE) with Apache Web Server and Git Installed using below startup script. <br/><br/>
apt update <br/>
apt install -y git <br/>
apt install -y apache2 <br/>
cd /var/www/html <br/>
git clone https://github.com/ramakb/GCP-GlobalLB-Game-Demo.git <br/>

2. Open http://EXTERNAL-IP-GCE/GCP-GlobalLB-Game-Demo in your browser

Steps to follow:

1. Create the Boot Disk Image through GCE and run this game app from that GCE Instance [This is a simple use case but in case if you want to have the ability to reach to the global audience, this is not enough] <br/>
2. For Better Auto-Scaling abilities: [You've option to go either for Regional or Multi-Regional] <br/>
3. Delete that instance and create Instance Template using the Boot Disk Image <br/>
4. Create MIG <Managed Instance Group> using the Instance Template <br/>
5. Create a Global Load Balancer <HTTPS> - Ensure to have 'Health-check' set up along with 'Auto-scaling' parameters taken in to consideration <br/>
6. Configure Backend and Frontend services for the implementation <br/>
7. Once the GLB is up and running <usually takes about 5 mins>., you can see the traffic flows in the GCP console under <br/>
