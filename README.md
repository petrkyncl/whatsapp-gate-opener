# WhatsApp & SMS Gate Opener Robot

A smart automation project that allows people to open your gate remotely using a simple **WhatsApp message** or **SMS**.

---

## 📦 Features

- 📱 Open gate using **WhatsApp** or **SMS** by sending a code
- 🔐 Secure access (only approved codes)
- ⏱️ Quick response time
- 📊 Logs

---

## ⚙️ How It Works

1. Visitor sends a code by WhatsApp or SMS to the Samsung Galaxy A16 device.
2. The robot marks the message as read.
3. The robot adds visitor's message to a %ToHandle list.
4. When it's the visitor's turn, robot handles the message.
5. The robot checks if the code is valid, it's not public holiday and the time window is correct.
6. If everything is correct, robot will open the gate.

---

## 🧰 Tech Stack

- Hardware: Android Device (not too old)
- Messaging App: WhatsApp Business
- Tools: Tasker, AutoInput, AutoNotification

---

## 🚀 Install & Set-Up

1. Remove all Tasks and Profiles on your device
2. Make sure you have Tasker (version 6.5 or newer!), AutoInput, AutoNotification installed
3. Copy holidays.json to the folder /Tasker/ on your device
4. Open this link on the Android device
```bash
https://taskernet.com/shares/?user=AS35m8mxdMzkBJZzsjiTsJirNKvbabqnVhLPQFDYeVrRa11slSRTAOl39NaC1lWD0y4T1HUw&id=Project%3AWhatsApp+%26+SMS+Listener
```
4. Click Import
5. Enable all profiles
