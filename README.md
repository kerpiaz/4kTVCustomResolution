# 4kTVCustomResolution

Your 4K TV is handling 3840×2160 @ 120Hz, which is ~32 Gbps bandwidth.
---

### **📜 Custom Resolutions for 4K TVs (16:9) with AMD Radeon GPUs**
**Last Updated:** 2025  

This guide explains how to **create custom ultrawide resolutions** on a **4K 120Hz TV using an AMD Radeon GPU** (tested on Radeon 5700G iGPU). 
It may work with Intel or Nvidia GPU's, but I have not tested with them, but I don't see why it shouldn't work too!

---

## **🖥️ Why Do This?**
4K TVs are **always 16:9**, but some users want to use only **a portion of the screen** for a **1:1 pixel-mapped** ultrawide or standard monitor layout. This allows:  
✅ **Ultrawide gaming (21:9 or 32:9) without stretching**  
✅ **Better workspace organization (dual/triple monitor simulation)**  
✅ **Lower GPU load by rendering only a portion of the screen**  

---

## **🛠️ Step 1: Enable Custom Resolutions in AMD Adrenalin**
1. **Open AMD Adrenalin Software**  
   - Right-click desktop → **AMD Software: Adrenalin Edition**  
2. **Enable GPU Scaling**  
   - Go to **Settings (⚙️) → Display**  
   - Enable **GPU Scaling**  
   - Set **Scaling Mode** to **Preserve Aspect Ratio**  
3. **Create a Custom Resolution**  
   - Scroll down to **Custom Resolutions**  
   - Click **Create New Resolution**  
   - Enter a **resolution & refresh rate** (see list below)  
   - Use **"CVT-RB" (Reduced Blanking)** for better compatibility  
4. **Apply and Test** in Windows Display Settings  

---

## **🎯 Tested Resolutions (For 4K 120Hz TVs)**

| **Resolution** | **Aspect Ratio** | **Refresh Rate** | **Bandwidth (Gbit/s)** | **Notes** |
|---------------|-----------------|----------------|----------------|----------|
| **1920×1080** | 16:9 | ✅ 60-120Hz | **3.32 - 6.64** | Standard 1080p patch (1/4 of 4K screen) |
| **2560×1440** | 16:9 | ✅ 60-120Hz | **5.96 - 11.92** | Standard 1440p (works natively) |
| **3440×1440** | 21:9 | ❌ Fails | **8.00 - 16.00** | **Too wide for 16:9 TV** |
| **2560×1080** | 21:9 | ✅ 60Hz | **4.47** | Works but 120Hz fails |
| **3840×1600** | 21:9 | ✅ 60-120Hz | **9.22 - 18.44** | **Trick: Set at 60Hz first, then switch to 120Hz!** |
| **5120×2160** | 21:9 | ❌ Impossible | **16.77 - 33.54** | **Too wide for 16:9 TV** |
| **3840×1440** | 32:9 | ✅ 60Hz | **8.29** | Dual 1440p setup equivalent |
| **1920×2160** | 9:18 | ✅ 60Hz | **6.64** | Stacked dual 1080p setup |
| **2560×2880** | 9:18 | ❌ | **9.95** | Stacked dual 1440p (too tall) |

---

## **🔥 Step 2: Unlock 120Hz for Ultrawide**
Some TVs **block 21:9 resolutions at 120Hz**, but **this trick works**:  
✅ **Create & apply** `3840×1600 @ 60Hz` first  
✅ **Manually switch** to 120Hz in Windows  
✅ The resolution stays at **3840×1600** but runs at **120Hz!**  

💡 **Why does this work?**  
TV firmware sometimes **rejects ultrawide resolutions at 120Hz**, but once applied at 60Hz, it doesn't revert when you increase refresh rate manually.

---

## **🚀 Bandwidth Considerations (HDMI 2.1 / DisplayPort 1.4)**

| **Resolution & Refresh Rate** | **Bandwidth (Gbit/s)** | **Notes** |
|----------------|-------------|----------|
| 3840×2160 @ 60Hz | **12.54 Gbps** | Standard 4K 60Hz |
| 3840×2160 @ 120Hz | **25.08 Gbps** | Requires HDMI 2.1 |
| 3840×1600 @ 60Hz | **9.22 Gbps** | Easily fits within HDMI 2.0 |
| 3840×1600 @ 120Hz | **18.44 Gbps** | Works if TV supports it |
| 3440×1440 @ 120Hz | **14.22 Gbps** | Often rejected |
| 2560×1080 @ 120Hz | **7.96 Gbps** | Should work, but some TVs block it |

🔹 **Lower Refresh Rate = More Compatible Custom Resolutions**  
🔹 **HDMI 2.1 or DisplayPort 1.4 needed for 4K 120Hz & ultrawide**  

---

## **🛠️ Step 3: Fixing Issues**
**🔴 Problem: Custom resolution fails to add (Pixel Clock stays red)**  
✅ Use **CVT-RB2** (even lower blanking)  
✅ Lower refresh rate to **60Hz**, then manually increase  

**🔴 Problem: TV stretches ultrawide resolution instead of letterboxing**  
✅ Set **Scaling Mode** to **Preserve Aspect Ratio** in AMD settings  
✅ Look for **"Screen Fit" or "1:1 Mode"** in TV settings  

**🔴 Problem: Flickering or black screen when switching to 120Hz**  
✅ Lower refresh rate to **100Hz or 90Hz**  
✅ Try **Custom Resolution Utility (CRU)** to adjust blanking values  

---

## **📌 Final Thoughts**
🎯 If your **4K 120Hz TV doesn't accept ultrawide resolutions**, use the **60Hz trick** to bypass firmware limitations.  
🎯 For **best performance**, use **3840×1600 @ 120Hz** for a **perfect ultrawide gaming setup** inside your 4K display.  
🎯 If **nothing works**, try **AMD Virtual Super Resolution (VSR)** to force the resolution, but it won't be true 1:1 pixel mapping.  

---

### **💾 Save & Share!**
This guide is designed for **4K TV + AMD Radeon users** who want ultrawide setups. If you found this helpful, share it! 🚀  

---
