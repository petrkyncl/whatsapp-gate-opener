# WhatsApp & SMS Gate Opener Robot

A smart automation project that allows people to open your gate remotely using a simple **WhatsApp message** or **SMS**.

---

## 📦 Features

- 📱 Open gate using **WhatsApp** or **SMS** by sending a code
- 🔐 Secure access (only approved codes)
- ⏱️ Quick response time
- 📊 Logs

---

## ⚙️ How It Works (visitor POV)

1. Visitor sends a code by WhatsApp or SMS to the Samsung Galaxy A16 device.
2. The robot marks the message as read.
4. When it's the visitor's turn, robot handles the message.
5. The robot checks if the code is valid, it's not public holiday and the time window is correct.
6. If everything is correct, robot will open the gate.

---

## ⚙️ How It Works (developer POV)

1. Visitor sends a code by WhatsApp or SMS to the Samsung Galaxy A16 device.
2. In case of WhatsApp message:
   - WhatsApp Business creates a notification that triggers a profile
   - Profile runs a task that:
   - Reads the phone number and the text from the notification
   - Adds notification's content to ```%ToHandle``` list in format ```WA<splitter><phone_number><splitter><message>```.
3. In case of SMS message:
   - SMS triggers a profile
   - Profile runs a task that:
   - Reads the phone number and the text from the event
   - Adds notification's content to ```%ToHandle``` list in format ```SMS<splitter><phone_number><splitter><message>```.
4. ```%ToHandle``` list having 1 or more messages in it triggers a profile
5. Profile runs a task that:
   - Checks if the code isn't valid (outcome 3)
   - Checks if today isn't holiday (outcome 0)
   - Checks if the actual day and time isn't valid (outcome 2)
   - If we got here, everything succeeded.

---

## 🧰 Tech Stack

- Hardware: Android Device (not too old)
- Messaging App: WhatsApp Business
- Tools: Tasker, AutoInput, AutoNotification

---

## ❗ Important Device Config (do before Install & Set-Up)

- Update Tasker to version ```6.5 or newer```.
- Enable developer options in settings, go there and enable ```Stay awake```. Make sure the device is charging all the time.
- Copy ```holidays.json``` to ```/Tasker/``` folder
- Ensure there are no battery restrictions for Tasker, AutoInput and AutoNotification

---

## 🚀 Install & Set-Up

1. Make sure you have Tasker, AutoInput, AutoNotification installed
2. Turn off all existing profiles in Tasker
4. Open this link on the Android device
```
https://taskernet.com/shares/?user=AS35m8mxdMzkBJZzsjiTsJirNKvbabqnVhLPQFDYeVrRa11slSRTAOl39NaC1lWD0y4T1HUw&id=Project%3AWhatsApp+%26+SMS+Listener
```
4. Click Import (do NOT enable any profiles yet)
5. It will create a tab at the bottom in Tasker. Click it.
6. Open ```User Variables``` task, edit your variables, run the task
7. Open ```Update CSV Data``` task and run it
8. Enable all profiles
