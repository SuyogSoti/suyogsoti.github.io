---
layout: post
comments: true
title: Oatmeal Diaries Launches
date: 2017-06-13
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

The obvious answer that came up was that the data would be modified in some way by a key that the sender has. The recipient would then have the corresponding key turn the data back to the way it was before. The data would also be signed by the sender in some way so the recipient will know for sure that I was the one who sent the data. There is however a problem that comes with this approach. If I was the sender and Bob was the recipient who lives half way around the world, how will Bob and I exchange keys? This question ultimately led to the creation of Public Key Cryptography.  The idea is that I would have a public key and a private key. Bob would also have a public and a private key. I would use Bob's public key to encrypt the message, which could only be decrypted by Bob's private key. When encrypting the message, I would sign it using my private key. Using this method, once Bob received the message, he could decrypt it with only his private key. This ensures that whatever was sent through those messages are is not revealed, and he would verify that I was the sender of the message using my public key. This method made it so that I could just put my public key on a server with enough assurance that anybody could communicate with me securely. 

### The flaw

There is of course a problem with Public Key Cryptography. The question is, how to we know that we are getting the public key from the right person. The who idea would fail if we just sent the message to the wrong entity. How do we know that the public key we receive is correct?

### The Solution -- Keybase 

Keybase goes off of the idea that who we are on the Internet is based on the sum of all of our social media accounts. Who I am in the Internet is a my facebook, twitter, website, reddit profiles and more, so the idea is why not associate your public key with your online presence? Keybase is a client system that lets people interchange data (messages and files) in a secure way. How do you know that you are talking to who you think you are? Just check their facebook or twitter page. I find the implementation of PGP by Keybase to be very creative, and I think that it deserves recognition for it.