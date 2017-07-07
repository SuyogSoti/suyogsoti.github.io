---
layout: post
comments: true
title:  "Dell XPS 9560 - Perfect Linux Laptop"
date:   2017-07-07
blog: true
categories: Education Technology Linux Arch
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

There are arch snobs out there, who take pleasure in thinking that they are above everyone else just because they run arch, but I am not one of them. I have used a debain based OS for the most of my life, and I was OK with that, but I do have to admit that the somebody who has installed arch once will know more about how an OS works and all of its moving parts than someone who does not. If there is a problem where your laptop crashes, arch users will not panic because they know how to diagnose what crashed. From that point on, fixing the problem is just a Google search away.