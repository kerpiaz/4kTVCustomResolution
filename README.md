# 4K TV Custom Resolutions Guide (for AMD & NVIDIA)

Run custom resolutions like **ultrawide (21:9)** or a centered **1440p window** on your 4K TV, surrounded by perfect black bars. This method uses your GPU to handle all the scaling, making it simple and effective.

This method is confirmed to work flawlessly with both **AMD Radeon** and **NVIDIA GeForce** GPUs. Tested on: Ryzen 7 5700G and a laptop with Radeon 780M + RTX 5060 on a Mini-LED 4K 144Hz TV.

---

## The Core Method: GPU-Side Scaling

Instead of sending an unsupported resolution to your TV, your PC will **always output a native 4K signal**. Your GPU then renders your chosen resolution (e.g., 2560x1440) in the center of that 4K signal, filling the rest with black. On OLED/Mini-LED TVs, these black bars are completely invisible.

---

## Instructions

### 1. Enable GPU Scaling (Do this once)

**🟢 For NVIDIA (GeForce):**
1.  Open **Nvidia Control Panel** → **Display** → **Adjust desktop size and position**.
2.  Select your TV.
3.  Under the **Scaling** tab, choose **"No scaling"**.
4.  Set **"Perform scaling on:"** to **"GPU"**.
5.  Click **Apply**.

**🔴 For AMD (Radeon):**
1.  Open **AMD Software: Adrenalin Edition** → **Settings (⚙️)** → **Display**.
2.  Enable **GPU Scaling**.
3.  Set **Scaling Mode** to **"Center"** or **"Preserve aspect ratio"**.

### 2. Select Your Resolution

1.  Go to **Windows Display Settings**.
2.  Choose your desired resolution (e.g., 2560x1440, 3840x1600).
3.  That's it! Your GPU will now center it correctly on your 4K screen.

---

## Popular Custom Resolutions for my use case (for a 55" 4K 120Hz+ TV) 
NOTE: if you use smaller or bigger inch TV, the change in reolution X size will vary! if you make a 1080P on a 42" 4K TV it may be too small so one would need to go to 1440p.

| Resolution  | Aspect Ratio | Works at 120Hz+? | Notes                                                  |
| :---------- | :----------- | :-------------- | :----------------------------------------------------- |
| **3840×1600** | 21:9         | ✅ Yes          | **The perfect ultrawide.** Fills the width of the TV.  |
| **2560×1440** | 16:9         | ✅ Yes          | A standard 27" monitor experience.                  |
| **1920×1080** | 16:9         | ✅ Yes          | A smaller, focused window for competitive games.       |
| **3840×1440** | 32:9 (ish)   | ✅ Yes          | Super-ultrawide, great for productivity.               |
| **2560×1080** | 21:9         | ✅ Yes          | A smaller ultrawide window.                            |

💡 **AMD Tip:** If a custom resolution fails at 120Hz, try creating it at **60Hz** in the Adrenalin software first. Apply it, then switch to 120Hz in Windows Display Settings.

Enjoy your ultimate all-in-one display
