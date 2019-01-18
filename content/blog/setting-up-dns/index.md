---
title: "Setting up DNS"
description: 'You just created a beautiful website.  Great!  Now you need customers to be able to get to it.  This is where the Domain Name Server (DNS) comes in.'
date: 2016-02-09T13:22:41-05:00
categories: [web development]
aliases: ["blog/2016/2/9/setting-up-dns","blog/2016/02/09/setting-up-dns"]
images:
- 'images/dns.png'

resources:
- name: Setting up DNS
  src: 'images/dns.png'
---

You should be familiar with the Address Bar in your browser.  It looks something like this:

{{< figure src="images/dns_addressbar.png" title="Address Bar" >}}

When your users go to a URL such as "www.drawbuildplay.com", the request will go to a DNS server which routes the request to the correct place where your website is hosted.  Think of it like regular mail you send through the post office.  You send a letter marked with the recipients address.  The postal service will pick up the mail and route it to the appropriate place, going through a bunch of intermediary postal locations, until it reaches the destination.

DNS works pretty much the same way. You have an address which is mapped to a destination where your website resides.  These destinations are typically mapped with either what is called an "A" record, or a "CNAME" record.

A RECORDS
---------

An A Record maps a fully qualified domain name (FQDN) to an IP Address.  This is useful if you want your domain name to point to the IP address of your load balancer or directly to your server.

CNAME RECORDS
-------------

CNAME records stand for "Canonical Name Record".  It is used to indicated that the domain name is an alias for another domain name.  Here are drawbuildplay, we often create CNAME records to point to (alias) another domain owned by squarespace.

Another time we often use CNAME records is when integrating with a CDN (Content Delivery Network).  It allows us to point our domain to another domain owned by a CDN provider such as Akamai, Fastly, or Amazon CloudFront.

TXT RECORDS
-----------

TXT Records are used to add arbitrary text records to your DNS settings.  These are often used to verify ownership of a domain, or to signal certain information to humans or other machines that rely on it.

MX RECORDS
----------

MX Records are used to route where Email messages should be sent.  If you are using Google's Gmail to power your email hosting, then this is where you add the appropriate MX records pointing to Googles' Servers.

NS RECORDS
----------

NS Records are used to tell your Domain Name Server where your settings are kept.  A lot of users will have their Name Server at the same provider as where they purchased their domain.  Others however, control their DNS settings from somewhere else like Rackspace or Google Domains.  This is where they would set the NS record at the provider where the domain ownership exists.
 
{{< figure src="images/dns_records.png" title="Sample DNS Record Fields" >}}

DNS PROVIDERS
-------------

There are many DNS providers out there.  One of the more popular ones is GoDaddy.  I personally am not a fan of their interface, and I tend to manage my domains through either Rackspace or Google Domains.  You can still buy your domain from any of your preferred providers, and then set up your NS records to point to Rackspace or Google Domains.

Once you have purchased your domain, and set up the appropriate Name Server records, you will be able to create your A records or CNAME records and point it at your website.

DNS PROPOGATION
---------------

Any changes you make to your DNS settings takes time to propogate around the world.  In other words, your DNS settings are copied to hundreds of servers around the world so that the internet runs a little bit faster.  These copies have what is called a TTL (Time to live).  When that TTL expires, the server with the copy looks for a fresh copy of the data in case anything changed.  So whenever you make a change, it could take up to 24 hours before all your users can see your change.  When playing around with DNS, I suggest setting it to 5 minutes a few days before you need the changes applied.

