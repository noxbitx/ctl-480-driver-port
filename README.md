
# Wacom CTL-480 Driver Port for Android (SM-T819 / MSM8976)

WARNING: This driver porting process is extremely difficult. Proceed only if you’ve got stable mental firmware.

DISCLAIMER: I am not responsible for bricked devices, kernel panics, or spontaneous combustion. You know the drill.


---

Status: In Progress

Target Kernel: android_kernel_samsung_msm8976-lineage-16.0
Platform: Samsung Galaxy Tab S2 9.7 (SM-T819)
Tablet: Wacom CTL-480 (USB, 5V 100mA)
Environment: OTG-powered (3.5V), rooted Android 14 LineageOS 21


---

What This Project Is

This is a highly experimental driver porting project that brings Wacom CTL-480 pen tablet support to a rooted Android tablet running a custom kernel.

Goal: Achieve full pen + hover detection using custom-compiled kernel modules and modified input drivers.
Why? Because drawing on a tablet that wasn’t meant for this is peak chaos engineering—and I’m all for it.


---

Features

[x] Kernel source tree prepared

[x] modules_prepare success

[x] Wacom driver files (wacom_sys.c / wacom_wac.c) merged into wacom.c

[x] Compilation flags + defines resolved

[x] HID macros conflict resolved

[x] Compilation errors mapped and fixed

[ ] modpost completed

[ ] Working .ko module

[ ] Tested on-device

[ ] Stable pen + hover detection

[ ] Voltage-based stability tests



---

Notes

Power draw through OTG is limited to ~3.5V. The tablet likely steps it up internally, but stylus hover distance might be shorter.

Future patching may include timing tweaks for low-voltage behavior, once the basics are stable.

Every error, fix, and kernel interaction is being documented and explained—for future devs who dare follow this path.



---

Screenshot Dump

(Coming soon)


---

Explanation: soon

A full guide is being written, covering:

Kernel macro landmines

Header conflicts

HID struct duplications

Why recordmcount hates you

And how to survive make with your sanity intact



---

Stay tuned. This rabbit hole goes deep.
