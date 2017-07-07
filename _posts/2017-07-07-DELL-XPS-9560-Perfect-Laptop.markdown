---
layout: post
comments: true
title:  "Dell XPS 9560 - Perfect Linux Laptop"
date:   2017-07-07
blog: true
categories: Education Technology Linux Arch KDE
author: "Suyog Soti"
---

This is my blog post on what I learned from trying to set up my new XPS to be the perfect machine. I have learned a lot for these experiences, and I hope that other too can learn a lot from my experiences.

<!--excerpt-->

## System

| Features          | Specs                                    |
| ----------------- | ---------------------------------------- |
| Type              | Dell XPS 9560                            |
| RAM               | 32 GB (custom added)                     |
| Graphics Card     | Integrated Intel and Nvidia GTX 1050     |
| CPU               | Intel I7 7700HQ                          |
| SSD               | 512 GB                                   |
| Linux kernel      | 4.8.17-1                                 |
| OS                | Manjaro KDE - Installed through Architect |
| GPU Configuration | Nvidia and Bumblebee                     |

## The History

I first installed Ubuntu on my laptop, and dual booted with windows. The configuration worked great, expect for the fact that my battery life was literally 4 hours and I that I never booted into windows. I first started to look into why Ubuntu had such horrible battery life, and I discovered that the main reason that I was not using the proper Nvidia drivers. When I looked at the hardware configuration section of the OS, I saw nvidia prime 375, and I just clicked that button to install it. After logging out and logging back in again, I was just shocked to find that my battery consumption had actually increased. I then did some more research and came upon the conclusion that the main reason was that my graphics card was the thing draining it. I went to the nvidia-prime settings, and disabled the graphics driver. I through my problems were solved then, but was I shocked to find out that I now could not shutdown my computer, reboot, or ever call "screenfetch" on the terminal. Any actions related to the GPU would just hang, and so like any other hot blooded Linux newbie, I installed another OS, sort of. I actually moved to Xubuntu, which is not different from Ubuntu except for the fact that it gave me a bit more customizations. I did not modify the graphics at all, and stayed as far away as possible from it. The problem was that I still had 4 hours of battery life. Though Xubuntu may use less system memory than Unity, Gnome, or KDE, they all have about the same battery life. As I gained the nerve to start playing around with my configurations again, I caught smell of Bumblebee. I thought this was exactly the product I needed, and it is important to remember that at this point, I still had not learned about prime vs optimus technology. I thought bumblebee would work for any old graphics card without the need for the optimus technology, but even as I had the optimus technology, I still failed to configure it correctly. I needed up deleting my display drivers, not knowing what to do and trying to install Arch.

## The Arch

There are arch snobs out there, who take pleasure in thinking that they are above everyone else just because they run arch, but I am not one of them. I have used a debian based OS for the most of my life, and I was OK with that, but I do have to admit that the somebody who has installed arch once will know more about how an OS works and all of its moving parts than someone who does not. If there is a problem where your laptop crashes, arch users will not panic because they know how to diagnose what crashed. From that point on, fixing the problem is just a Google search away. I am not saying that everyone must use Arch, but I do think that everyone should at least try to install it on their own system because I believe the experience it provides will be monumental in understand what is happening 'under the hood' in the laptop.

## The Fix

Lets get this correct, if you want to install *Manjaro* on a Dell XPS 9560, you **must** do so using Manjaro Architect, because none of the regular live iso will even boot. In addition to that, use Linux kernel 4.8 and above and make sure to use the nvidia proprietary divers because nouveau, the open source version, still does not support the pascal series. This also means that you may not use Wayland as the display driver since Wayland does not support nvidia. Gnome runs on Wayland by default now, so Gnome 3 is not an option, at least until kernel 4.12 is released with nouveau is expected to start supporting the pascal series. I chose KDE and the architect menu installer installed **and** configured bumblebee for me. Make sure to also install the Linux headers because the boot will not be consistent otherwise. Talking about booting consistency, adding `acpi_osi=! acpi_osi="Windows 2009"` to the end of your [/etc/default/grub](file:///etc/default/grub) will help you boot into your machine more often. 

## KDE

This was my first time trying KDE, and I just want to say that I like it a lot. Configuring it so that it would notify me when I have mail in all of my accounts took some time, but I think that it is really cool. Just a shout-out to the KDE team for an amazing DE.