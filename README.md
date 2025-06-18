# 🛡️ Snort IDS on Ubuntu

A quick and effective setup of Snort IDS on Ubuntu to detect real-time ICMP, SSH, and HTTP traffic threats. Built as part of my cybersecurity learning journey.

---

# ⚙️ Tools Used
- Ubuntu 20.04 / 22.04  
- Snort 2.x  
- Apache & SSH  
- Attacker VM (Kali Linux)

---

# 🚨 Custom Rules

alert icmp any any -> $HOME_NET any (msg:"ICMP Packet Monitor"; sid:100786; rev:1;)  
alert tcp any any -> $HOME_NET 22 (msg:"SSH Brute Force Attempt"; sid:107806; rev:1;) 
alert tcp any any -> $HOME_NET 80 (msg:"HTTP alert"; sid:708603;)

---

# 🧪 Test Commands

ping [Ubuntu IP]  
ssh user@[Ubuntu IP]  
curl http://[Ubuntu IP]

Run Snort with:

sudo snort -A console -q -c /etc/snort/snort.conf -i eth0

---

# 👨‍💻 Author

Faizanullah Syed 
faizanullah.syed19@gmail.com
SOC Analyst in Training | Cybersecurity Learner
