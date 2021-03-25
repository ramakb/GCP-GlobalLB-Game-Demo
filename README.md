A WebGL maze game built with Three.js and Box2dWeb. 
Credits & Source from: https://github.com/wwwtyro/Astray and LearnGCPWithMahesh

# Simple game which is used for GCE or Managed Instance Ggroups with Global-LoadBbalancer

1. Provision a Google Compute Engine (GCE) with Apache Web Server and Git Installed using below startup script. <br/><br/>
apt update <br/>
apt install -y git <br/>
apt install -y apache2 <br/>
cd /var/www/html <br/>
git clone https://github.com/ramakb/GCP-GlobalLB-Game-Demo.git <br/>

2. Open http://EXTERNAL-IP-GCE/GCP-GlobalLB-Game-Demo in your browser

Steps to follow:

1. Create the Boot Disk Image through GCE and run this game app from that GCE Instance [This is a simple use case but in case if you want to have the ability to reach to the global audience, this is not enough] <br/>
2. For Better Auto-Scaling & End-user Reachingabilities: [You've option to go either for Regional or Multi-Regional with Global LoadBalancer which is possible with MIGs] <br/>
3. Delete that instance and create Instance Template using the Boot Disk Image <br/>
4. Create MIG <Managed Instance Group> using the Instance Template. Make a note to NOT to have External-IP for this MIGs as we'll have GLB facing the outside world <br/>
5. Create a Global Load Balancer <HTTPS> - Ensure to have 'Health-check' set up along with 'Auto-scaling' parameters taken in to consideration <br/>
6. Configure Backend and Frontend services for the implementation <br/>
7. Once the GLB is up and running <usually takes about 5 mins>., you can see the traffic flows in the GCP console under <br/>
8. Use the External-IP to access the Game or the Application
9. That's it - End of the Story as a Phase-1 Approach

Many more features or services of GCP can be utilised and I'll update that here as a Phase-2 Approach

Till then - Happy Learning!

![GLB Before](https://github.com/ramakb/GCP-GlobalLB-Game-Demo/blob/main/Before.png)
![GLB After](https://github.com/ramakb/GCP-GlobalLB-Game-Demo/blob/main/After.png)
