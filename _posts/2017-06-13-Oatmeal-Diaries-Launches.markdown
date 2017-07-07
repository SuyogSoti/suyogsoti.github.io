---
layout: post
comments: true
title: Oatmeal Diaries Launches
date: {}
blog: true
categories: Education Technology Encryption Keybase
author: Suyog Soti
published: true
---

Hello Everybody,

I have recently launched my own podcast. It will explore the intricacies of technology, life, politics and beyond. My very first episode has been launched and I hope that all of you will listen to it.

<!--excerpt-->

## First Episode

The very first episode will go over why I want to start this podcast in addition to going over my new interest, keybase. I was recently introduced to this new application named [keybase](https://keybase.io). It can be decribed as a public hosting of your public keys for communication using public cryptography by verifying your identifies using all of your varius social media accounts. Please listen to the podcast for more of my thoughts/information.

PSA: My main hosting for this podcast is [Archive.org](https://archive.org/details/@suyogsoti) because it is free. I will add the first few episodes to [soundcloud](https://soundcloud.com/suyog-soti) as well because soundcloud is a popular platform.

<iframe src="https://archive.org/embed/OatmealDiariesEpisodeOne" width="500" height="40" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" allowfullscreen></iframe>

## Keybase

Since you all already know already know who I am, I will just jump straight to why I find keybase to be so cool. There is really only one reason why I find this technology so cool. It is because keybase goes by this philosophy that your public presence is the sum of all of your different social media accounts. Before I get into exactly why I think that keybase is such an interesting tool, I think that some background on encryption is necessary. Feel free to skip the next section on encryption if you come from such a background.

### A Short History of Cryptography

I think that most everybody has some idea on what cryptography is and how it works. I am not an expert on it so I will not go into too much detail in fear of misinforming you. I think the best way to explain crypto is by using examples. Let us say that I want to send a secure message to a friend, lets name him Bob for now, who lives around the world. The question becomes how to protect the information even if someone gains control of the channel that the information is moving in. So in our context, if someone intercepts my message to Bob, how do I make it so that

1. the content of my message will not be revealed
2. the hacker can not pretend to be me and gain information from Bob

The obvious answer that came up was that the datat would be modified in some way by a key sy the sender. The recepient would then have the corresponding key turn the data back to the way it was before. The data would also be signed by the sender in some way so the recipient wll know for sure that I was the one who sent the data. There is however a problem that comes with this approact. If I was the sender and Bob was the recipient who lives half way around the world, how will Bob and I exchange keys?
