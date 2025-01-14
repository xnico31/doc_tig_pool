---
title: Set up Worker  
description: How to add and configure machines for TIG Pool mining.  
---

# Adding Machines  

Once your account is created, you will have access to your dashboard. To add machines to your mining setup, follow these steps:  

1. **Click on the "New Worker" button:**  
   - Navigate to your dashboard and click the **"New Worker"** button.  

2. **Name Your Machine:**  
   - Assign a unique and descriptive name to each machine to easily identify them.  
   - **Warning:** Ensure you have reviewed the necessary requirements for mining before proceeding.  
     [Go to the Minimum Requirements section](/docs/getting_started/01_requirements).  

3. **Generate an Installation Script:**  
   - Once the machine is created, an installation script will be generated.  
   - Copy this script and run it on your machine using a Linux-based operating system.  

4. **Follow Plan Limits:**  
   - You can add as many machines as the limits specified in your selected plan allow.  

---

# Installation on the Machine  

After creating a new machine in your dashboard, follow these steps to install the mining software:  

1. **Open Your Terminal:**  
   - Navigate to the `/home/user/` directory in your terminal.  
   - **Paste and run the installation script you copied earlier. Ensure you run it as a normal user, not as root!**  

2. **Important Reminder:**  
   - Ensure you are using the correct script for the specific machine you created.  
   - **Warning:** Using the wrong script can result in a temporary **1-hour ban**. Remember, the rule is **one script per machine**.  

3. **Run the Installation:**  
   - Let the installation process complete.  
   - Once finished, a success message will appear, indicating that the setup is complete and the machine is ready.  

---

# Mining Operation  

After installation, the mining process will automatically start in the background using `screen`. Two distinct screens will be created:  

- **Client Screen:** `pool_tig`  
- **Worker Screen:** `slave_tig`  

To monitor logs, use the following commands:  

```bash
tail -f ~/tig_pool_main/logs/pool_tig.log
tail -f ~/tig_pool_main/logs/slave_tig.log
```

To turn off Mining 

```bash
pkill -f slave_tig && pkill -f pool_tig*
```

To relauch mining on wake up or restart

```bash
cd tig_pool_main  && screen -wipe && screen -dmL -Logfile logs/pool_tig.log -S pool_tig -dm bash -c "./pool_tig_launch_*; exec bash" && screen -r pool_tig
```
