---
title: "Introduction to SSL"
description: 'The infamous question.  What is SSL?  Or, more importantly, why should I care about it?'
date: 2016-02-16T13:38:48-05:00
categories: [web development]
aliases: ["blog/2016/2/16/introduction-to-ssl","blog/2016/02/16/introduction-to-ssl"]

images:
- 'images/ssl.png'

resources:
- name: Introduction to SSL
  src: 'images/ssl.png'
---

SSL stands for Secure Socket Layer. It's actually a deprecated technology, now replaced by a newer acronym - TLS.  TLS stands for Transport Layer Security.

Okay, enough of this gobbledygook!  What do all these fancy words mean?!?!  In a nutshell, its all about security on the internet.

When you visit your bank website, or these days even Facebook and Google, you will see a lock icon next to the URL in the address bar.

{{< figure src="images/ssl_lock.png" title="The Green Lock" >}}


THE GREEN LOCK
--------------

The green lock, and the "https://" next to it means that the communication between your device (computer/iphone/ipad etc) is secure.  No one else can read the data that is sent and received, and no one can modify it.

This is important if you care about your privacy.  Obviously you don't want anyone else seeing your communication with your bank.  Your passwords should stay secret.  Your account numbers should stay secret.  Likewise your emails, and pretty much anything you do online should stay secret between you and the site you are visiting.

When you see a green lock, what you are being told is that this domain has been verified with the owner and that your communication will be encrypted between you and this domain.  This means that if someone intercepts your traffic (also called a "man in the middle" attack), they cant see what is being transmitted, and they cannot change anything since all the data is encrypted.

HOW DOES THE ENCRYPTION WORK?
-----------------------------

First, the owner of the domain has to apply for a Secure Certificate.  There are a few Certificate Authorities (CA) that are approved CA's by the browser makers such as Google (Chrome) or Microsoft (Internet Explorer/Edge).  A Certificate Authority is a trusted authority who can issue Certificates.

For the lock to be displayed, the owner of the website must first request a secure certificate from one of these approved CA's.

Next, the CA will verify the domain ownership rights with the owner.  In a later blog post I will talk about the different ways the domain verification can occur (DV, EV, OV verification types).  Once the domain ownership has been verified, a certificate is issued.

The certificate consists of a public key and a private key.  The private key always remains in possession of the certificate owner and is never shared.  The public key is made available to all.  When you submit a request to the website (eg to your bank site), the data from your device is first encrypted with the bank websites' public key.  Only the bank is able to decrypt your request using their private key.  The bank will then respond to your request with the response encrypted using your public key.  Only you have a private key which can decrypt their response.

_For the more technical folks out there - I am simplifying this process and will go into deeper technical details in a later post._

BUT HOW GOOD IS THE ENCRYPTION?  
-------------------------------

Like all good encryption, eventually computers are powerful enough to break it.  That is why current TLS certificates are recommended to have public/private keys that are at least 2048 bits long.  The more bits, the harder it is to hack.  But the trade-off is it also requires faster and more powerful computers to use.

WHY SHOULD I CARE?
------------------

Okay, back to the question, why should I care about all this?  Well, for starters, search engines are starting to look at HTTPS support as a ranking factor, where supporting HTTPS on your website will increase your rank.

Also, why risk compromising your customers data?  Even if your website doesn't deal with sensitive data, everyone still has a right to privacy.

ISN'T IT EXPENSIVE?
-------------------

Traditionally, SSL/TLS Certificates have been expensive.  Recently, cheap to free alternatives have emerged.  One option is LetsEncrypt who offer free certificates.  Another option is CloudFlare.  CloudFlare will give you a free SNI certificate along with their CDN services.


Source: https://en.wikipedia.org/wiki/Transport_Layer_Security