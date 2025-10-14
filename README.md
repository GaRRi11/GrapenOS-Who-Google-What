It’s never been a secret that our pocket devices are used to listen and watch us 24/7, and track all our actions by governments. But nowadays they do not even try to hide that fact :) They started laughing at us by selling that data to highest bidder profit corporations. We see ads and content on the internet based on the data they collected and analyzed.

<img width="1400" height="780" alt="image" src="https://github.com/user-attachments/assets/1a52b44d-2b79-49ec-b57d-e60da0817e8a" />


Making your device completely private and untraceable is nearly impossible these days. But there are ways of minimizing it.

They run closed-source blobs (binary files) because it’s impossible to reverse or see what’s inside. That’s the primary weapon of their “magic” :)

## Stock Android
I am a long-time lover of Android devices and I have a Pixel 8.
On stock Android, it has built-in Google Play Services which has all the permissions on my device:

Location

Contacts, Calendar, Call logs, SMS

Storage

Camera & Microphone

Network

Device ID & telemetry

Account access

System settings

Activity recognition & sensors

Notification access

I cannot modify it because it’s built-in and runs as a “system-level process”.
So that’s why I decided to change the OS completely and installed GrapheneOS – degoogled Android OS.

## Installation
No adb, no fastboot, no fiddling with recoveries and sideloading.
You unlock the bootloader, connect the phone to the computer, open Graphene’s WebUSB installer in a compatible browser and basically just click through the individual steps.

## GrapheneOS Security
GrapheneOS’s main thing is it sandboxes everything, so apps and system processes are isolated.

Built-in defense systems:

Sensors can be disabled globally

Randomizing memory location – important data is constantly moving on random locations

Seccomp filters – limit system calls by apps

W^X – prevents writing to executable memory regions

Exec-spawning restriction – restricting it limits apps to only their own code and prevents them from launching other system tools or scripts

UID filtering – adds per-app UID filtering; if the app is blocked, the request is dropped and the app gets a failure — the kernel never sees the connection attempt

Many other interesting defense systems...

The main thing is it manages to do all these defense actions without breaking apps.

## App Replacement
In GrapheneOS, there is a built-in browser named Vanadium.
It uses DuckDuckGo as search engine and gives ability to turn off JavaScript and delete all cookies every time you close the browser.

So I prefer to use all the apps which provide web versions with that browser — especially social media apps like Instagram, Facebook, Telegram, etc.
Just give Vanadium network permission only and use the web versions of those.
Every time you close the browser, cookies are deleted.

## VPN and Firewall
GrapheneOS has an ability named “Block connections without VPN”, so you just put your VPN on “always-on” and even if you forget, you will not get network connection unless you turn it on.

I prefer Mullvad VPN — payment with crypto and no identity details required :) + DNS over HTTPS.

NetGuard — local VPN-based firewall on Android.
Lets you block per-app IP/DNS traffic without root by routing traffic into a local VPN and dropping/forwarding packets.

Android’s VPNService gives ability to route all the network traffic through it without having root access.
So by using those apps, we can do multi-hop and monitor, apply firewall rules (block/filter), and route through VPN.

## Banking and Payments
Banking and payment do not work on that OS because they cannot work without Google services.
So use the web version of your bank for banking and just keep your credit card with you and use it for payments.

## Developer Perspective
Also, for Android developers, GrapheneOS is an interesting testing environment to test how their apps behave without Google dependencies and under hard app restrictions.

## Network Monitoring
There is an app named PCAPdroid for monitoring in/out network traffic like Wireshark — for paranoid like me :)
