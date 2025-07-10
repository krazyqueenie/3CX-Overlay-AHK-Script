# 3CX-Overlay-AHK-Script
Adds a custom, click-through overlay to the 3CX softphone using AutoHotkey.

This AutoHotkey script displays a custom image overlay on top of the 3CX softphone window. The overlay stays locked to the app, moves with it, and supports click-through interaction. Perfect for customizing the look of your 3CX softphone with your own personalized skin or design.

⚠️ **For personal use only. Redistribution not permitted.**

---

## 🖼️ How to Create Your Own Overlay

1. Open the 3CX app and take a screenshot of the full window.
2. Upload the screenshot to a design tool like:
   - [Dzine.AI](https://dzine.ai) (used in this example)
   - Canva
   - Adobe Express
   - Photoshop
   - GIMP
3. Design your custom overlay:
   - Add graphics, logos, text, colors — whatever you want.
   - Erase or cut out the window area so 3CX shows through underneath.
   - Save/export it as a **.png** file with a transparent background.
4. Keep the image the same size as your screenshot to maintain alignment.

---

## 🛠️ How to Use the Script

1. **Download and install AutoHotkey**  
   - Go to [https://www.autohotkey.com](https://www.autohotkey.com) and install it manually.
   - Windows may auto-prompt on first `.ahk` launch, but not always.

2. **Edit the script**
   - Open the `.ahk` file in a text editor.
   - Update the image path:
     ```ahk
     imagePath := "C:\Path\To\Your\Overlay.png"
     ```
   - (Optional) Tweak the overlay position if it doesn’t align perfectly:
     ```ahk
     offsetX := 201
     offsetY := -6
     ```

3. **Check the 3CX window class (if needed)**  
   This script tracks the 3CX window using the default class name `#32770`.  
   If the overlay doesn’t follow the app, you may need to update the class name.

   To find your 3CX window class:
   - Open AutoHotkey’s **Window Spy** tool manually:
     - Press `Win + R`, type `AutoHotkeyWindowSpy`, and hit Enter  
       *(or navigate to it in the Start Menu after installing AutoHotkey)*
   - Click the 3CX app window to focus it
   - Look at the "ahk_class" value shown in the spy window
   - Update this line in the script:
     ```ahk
     WinGetPos, x, y, w, h, ahk_class YOURCLASSNAME
     ```

4. **Save and run the script**  
   - Double-click the `.ahk` file
   - The overlay will appear and follow your 3CX window automatically

---

## ⌨️ Hotkeys & Controls

- **Ctrl + M** → Unlock/lock the overlay (lets you drag it if needed)
- **Esc** → Close the overlay/script
- **Click-through enabled by default** so buttons on the phone still work

---

## ✅ Tested On

- 3CX Desktop App (Windows)
- AutoHotkey v1.1.36.02

---

## 📜 License

This project is licensed under **Creative Commons Attribution-NonCommercial 4.0 (CC BY-NC 4.0)**

- ✅ Free to use and modify for personal use
- ❌ Not allowed to redistribute, re-upload, or include in paid products

See [`LICENSE.txt`](LICENSE.txt) for full terms.
