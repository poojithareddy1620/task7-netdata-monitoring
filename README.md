# Task 7: Monitor System Resources Using Netdata

## 🛠 Objective:
Install Netdata using Docker on an EC2 instance and visualize system performance metrics.

## 🚀 Setup Steps:
1. Launched Amazon Linux EC2 instance
2. Opened ports 22 (SSH) and 19999 (Netdata UI) in security group
3. Installed Docker and started Docker service
4. Ran Netdata container:
   ```bash
   sudo docker run -d --name=netdata -p 19999:19999 \
     --cap-add=SYS_PTRACE \
     --security-opt apparmor=unconfined \
     netdata/netdata

Accessed dashboard at:
http://107.22.134.16:19999/

📊 Features Monitored:
CPU usage

Memory and Disk I/O

Docker containers

System processes and alerts

✅ Outcome:
Successfully visualized live system metrics using Netdata.
