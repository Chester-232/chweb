+++
date = '2025-03-26T13:44:12+08:00'
draft = true
title = "Fixing 'iwlwifi failed with error -110' on Linux After Dual Boot with Windows"
summary = "Fixing “iwlwifi failed with error -110” on Linux After Dual Booting with windows 10/11"
+++

# Fixing “iwlwifi failed with error -110” on Linux After Dual Booting

Dual booting Windows and Linux can be a great way to enjoy the best of both worlds. However, if you’re experiencing issues with your Intel Wi‑Fi card on Linux—especially when switching from Windows—the error message below might look familiar in your system logs:

```
[    6.397335] iwlwifi 0000:02:00.0: probe with driver iwlwifi failed with error -110
```

In this post, we’ll explore what this error means, why it may occur in a dual-boot setup, and a simple fix that worked for me.

---

## What Does “Error -110” Mean?

When you see an error like this in your dmesg output, it tells you that the iwlwifi driver isn’t able to initialize your Intel Wireless 8265/8275 card properly. The “-110” error is often related to a hardware or power management issue. In many cases, this can happen because Windows leaves the Wi‑Fi card in a low-power or “hibernated” state if its Fast Startup feature is enabled.

---

## Why Dual Boot Can Cause Wi‑Fi Problems

**Fast Startup in Windows:**  
Windows Fast Startup (sometimes called Fast Boot) is designed to speed up the boot process by not completely shutting down the system. Instead, Windows saves some system state to disk so that the next boot is faster. While this feature can be helpful for Windows users, it may prevent your Wi‑Fi card from fully resetting its power state when you switch over to Linux. As a result, Linux may not detect or initialize the card correctly, triggering the error.

**What Happens in Linux:**  
When you boot directly into Linux after using Windows, the leftover power state or “hibernation” mode on your Wi‑Fi hardware can lead to the driver failing its probe (or initialization), hence the error message we saw. Interestingly, if you boot into Windows first (which resets the hardware properly) and then switch to Linux, the card works fine.

---

## The Simple Fix: Disable Windows Fast Startup

After some troubleshooting, I discovered that disabling Windows Fast Startup resolved the problem permanently. Here’s how you can do it:

1. **Boot into Windows 10:**  
   Open the Control Panel and navigate to **Power Options** you can press `win + R` and type `control panel` to open it up, or just right click in the battery icon in the taskbar(if only on laptop).

2. **Access Shutdown Settings:**  
   Click on **"Choose what the power buttons do"** on the left-hand side.  
   Then click on **"Change settings that are currently unavailable"** at the top.

3. **Disable Fast Startup:**  
   Under the **Shutdown settings** section, uncheck the box next to **"Turn on fast startup (recommended)"**.

4. **Save and Reboot:**  
   Click **Save changes** and restart your computer.

Once you’ve disabled Fast Startup, the Wi‑Fi card resets fully when shutting down, allowing Linux to initialize it properly during boot. Now, when you check your system logs (using `dmesg`), the error should no longer appear, and your wireless connections should work without a hitch.

---

## How to Confirm the Fix

After making the changes, boot into Linux and run:
```bash
dmesg | grep -i iwlwifi
```
If you no longer see the error message and your wireless interface appears in the output of:
```bash
nmcli device status
```
then you know the issue is resolved!

---

## In Conclusion

Dual boot setups can sometimes bring unexpected challenges, especially when different operating systems manage hardware power states in different ways. Disabling Windows Fast Startup is a simple and effective solution to the “iwlwifi failed with error -110” issue. By ensuring that your hardware resets completely during shutdown, you help Linux initialize your Wi‑Fi card correctly every time.

If you found this post helpful, feel free to share it with others who might be facing the same problem!

---

*Happy dual booting, and may your connections always be strong!*