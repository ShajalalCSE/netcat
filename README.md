# 🧠 Python Socket Command Execution (Client-Server Lab)

A simple **client-server socket project** in Python where a server sends commands and the client executes them locally and returns output.

⚠️ **Educational Use Only** — Run only in your own lab environment or authorized systems.

---

# 📦 Requirements

- Python 3.x
- Works on Windows / Linux / macOS
- No external libraries required

---

# 🛠️ Package Installation
```
No pip packages are required.
```
Just ensure Python is installed:

### Check Python version
```
python --version
```
📁 Project Files
```
project/
│── server.py
│── client.py
```
How to Run (Local Lab)
Step 1: Start server
```
python server.py
```
Step 2: Start client (new terminal)
```
python client.py
```
Step 3: Send commands

Example:
```
$ whoami
$ ls
$ ipconfig / ifconfig
```
🌐 How to Use on Remote System (Lab Setup Only)

You can test on two devices in the same network (LAN/WiFi).

🔹 Step 1: Find server IP

On server machine:
```
ipconfig   # Windows
ifconfig   # Linux
```
Example:
```
192.168.0.10
```
🔹 Step 2: Update client.py

Replace:
```
s.connect(("127.0.0.1", 8888))
```
With:
```
s.connect(("192.168.0.10", 8888))
```
🔹 Step 3: Allow port (Firewall)

Make sure port 8888 is open:

Windows Defender Firewall → Allow Python
Linux:
```
sudo ufw allow 8888
```
🔹 Step 4: Run order  
Run server.py on host machine  
Run client.py on remote machine  
Send commands from server terminal  

⚠️ Important Security Notes  
Do NOT expose this to the internet  
Use only in:  
Local machine testing  
Virtual machines (VMware / VirtualBox)  
Authorized lab environments  
This executes system commands → misuse can be dangerous  
🧠 Learning Purpose    

This project helps you understand:  

Socket programming  
Client-server architecture  
Process execution in Python  
Basic networking communication  
📌 Possible Improvements  
Add encryption (secure communication)  
Add multi-client support  
Add authentication system   
Add logging system   
