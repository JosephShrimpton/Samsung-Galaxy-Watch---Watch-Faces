# Watch Face Collection

A collection of custom Samsung Galaxy Watch faces built with Samsung Watch Face Studio, designed for Galaxy Watch 6 Classic running One UI / Wear OS 5. Each face is a personal project and homage to its respective source material.

---

## Watch Faces

### A Perfectly Useless Afternoon
A watch face based on the Mr Jones Watches design of the same name, created by Belgian illustrator Kristof Devos. The original watch features an illustrated pool scene where a figure floating on a rubber ring indicates the hours with their outstretched leg, and a small duck marks the minutes. This watch face takes its name and spirit from a quote by Chinese philosopher Lin Yutang — "If you can spend a perfectly useless afternoon in a perfectly useless manner, you have learnt how to live" — and translates that contemplative aesthetic into a digital face for the Galaxy Watch 6 Classic.

---

### GTA IV Mini Map
A watch face recreating the iconic Liberty City mini map from Grand Theft Auto IV. Features the original map texture as the dial, GTA HUD-style icons as hour markers, and circular progress bars tracking battery and step count in the style of the in-game UI.

---

### Seiko Willard
A recreation of the Seiko 6105-8110 "Willard" dive watch dial — the watch famously worn by Captain Willard in Apocalypse Now. Features applied-style lume indices, broad arrow hands with cream lume fill, and a white date window at 3 o'clock.

---

### TTT#1 Seoul Olive
A watch face inspired by the TTT#1 Hidden Time Watch — a collaboration between Anicorn and Seoul-based designer Jiwoong Jung. The original watch uses a conic gradient dial as an optical illusion, where the dark end of the rotating gradient reveals white hour numerals printed on the glass above as it passes beneath them, hiding the passing of time. This watch face recreates that sweeping olive-to-white gradient aesthetic for the Galaxy Watch 6 Classic's AMOLED display.

---

### Timex Q
A recreation of the Q Timex GMT reissue dial — the Pepsi bezel colourway with its classic navy/red split, round lume dot indices, day-date complication, and gilt hands.

---

## Compatibility

These watch faces are built using **Samsung Watch Face Studio** and are compatible with:

- Samsung Galaxy Watch 4 series
- Samsung Galaxy Watch 5 series
- Samsung Galaxy Watch 6 series
- Samsung Galaxy Watch 6 Classic

They are **not compatible** with non-Samsung Wear OS devices such as Google Pixel Watch or Fossil watches.

---

## Installation via ADB

### Requirements
- [Android Platform Tools](https://developer.android.com/tools/releases/platform-tools) installed on your PC
- Your Samsung Galaxy Watch and PC connected to the same Wi-Fi network
- Developer Options enabled on your watch

### Step 1 — Enable Wireless Debugging
Go to **Settings → Developer Options → Wireless Debugging** and enable it.

### Step 2 — Pair your watch
Tap **Pair new device** on the Wireless Debugging screen. Your watch will display an IP address, pairing port, and 6-digit pairing code.

Open a command prompt on your PC and run:
adb pair YOUR_WATCH_IP:PAIRING_PORT

Enter the 6-digit pairing code when prompted:
Enter pairing code: XXXXXX
Successfully paired to YOUR_WATCH_IP:PAIRING_PORT

### Step 3 — Connect
Go back to the main Wireless Debugging screen on your watch. Note the IP address and port shown there — this is different from the pairing port.
adb connect YOUR_WATCH_IP:DEBUG_PORT

Verify the connection:
adb devices

Your watch should appear as a connected device.

### Step 4 — Install the APK
Run the following command with the path to your chosen APK:
adb -s YOUR_WATCH_IP:DEBUG_PORT install "PATH\TO\WATCHFACE.apk"

Example:adb -s 192.168.1.100:12345 install "C:\Users\YourName\Downloads\Seiko_Willard.apk"

You should see:
Performing Streamed Install
Success

### Step 5 — Apply the watch face
On your watch, long press the current watch face to open the watch face selector. Swipe through to find the installed face, or find it under **My watch faces** in the Galaxy Wearable app on your phone.

### Notes
- The debug port changes every time Wireless Debugging is toggled. Always check the current port on your watch before connecting.
- If you receive a `more than one device/emulator` error, always specify the device using `-s YOUR_WATCH_IP:DEBUG_PORT` as shown above.
- If a face fails to appear after install, uninstall the previous version first: `adb -s YOUR_WATCH_IP:DEBUG_PORT uninstall com.package.name`

---

## Legal

All watch faces in this collection are personal, non-commercial homage projects created out of appreciation for the original designs. No commercial use is intended or implied.

**A Perfectly Useless Afternoon** — design inspired by the Mr Jones Watches design of the same name, created by Kristof Devos. Mr Jones Watches and all related trademarks are the property of Mr Jones Design Limited. This project is not affiliated with or endorsed by Mr Jones Watches or Kristof Devos.

**GTA IV Mini Map** — design inspired by Grand Theft Auto IV. All trademarks, map assets, and visual elements related to Grand Theft Auto IV are the property of Rockstar Games and Take-Two Interactive. This project is not affiliated with or endorsed by Rockstar Games or Take-Two Interactive.

**Seiko Willard** — design inspired by the Seiko 6105-8110. Seiko and all related trademarks are the property of Seiko Holdings Corporation. This project is not affiliated with or endorsed by Seiko.

**TTT#1 Seoul Olive** — design inspired by the TTT#1 Hidden Time Watch by Anicorn and designer Jiwoong Jung. All trademarks and design rights are the property of Anicorn and their respective collaborators. This project is not affiliated with or endorsed by Anicorn or TTT Watches.

**Timex Q** — design inspired by the Q Timex reissue. Timex and all related trademarks are the property of Timex Group. This project is not affiliated with or endorsed by Timex Group.

These projects are shared freely for personal use only. Redistribution for commercial purposes is not permitted.
