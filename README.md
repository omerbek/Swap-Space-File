### Links
* **omerbek Telegram**  
  https://t.me/omerbekta_s

* **omerbek Twitter**  
  https://twitter.com/omerbekta_s



## 🟢 Introduction
In Linux systems, **swap space** is an essential component for memory management.  
When your physical RAM becomes full, swap provides additional virtual memory by temporarily storing inactive data. This helps maintain system stability and prevents crashes or performance drops.


## 🟢 Functions of Swap Space
### 1 — Memory Overflow Handling
If your RAM is fully used, swap takes over and stores inactive process data.  
This prevents system instability and memory-related errors.

### 2 — Swap File Flexibility
A swap file is created inside the existing filesystem and acts as swap space.  
It is flexible and allows the swap size to be easily increased or decreased.


## 🟢 Recommended Swap Size
Swap size depends on system usage and installed RAM:

- **4 GB RAM or less:** 2× RAM  
- **4–8 GB RAM:** 1.5× RAM  
- **8–16 GB RAM:** Equal to RAM  
- **16 GB RAM and above:** Adjust as needed, usually half of RAM is enough  

If the system uses **hibernation**, swap should be at least equal to the amount of RAM.


---

## 🟢 View Active Swap
```
swapon --show
```
🟢 Add Swap Space (Example: 2 GB Swap File)
```
sudo fallocate -l 2G /swapfile
```
```
sudo chmod 600 /swapfile
```
```
sudo mkswap /swapfile
```
```
sudo swapon /swapfile
```
🟢 Make Swap Permanent
```
echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
```

🟢 Disable All Swap
```
sudo swapoff -a
```
🟢 View Swap Usage
```
htop
```
```
free -m
```
```
sudo swapon -s
```
