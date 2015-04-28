---
layout: post
title: "Sending Drupal 7 email from Acquia Cloud Free with SMTP and Gmail"
date: 2015-04-28 08:24:23 -0400
comments: true
categories: [Drupal, Acquia Cloud]
---
<p>The goal was simple. I wanted to add a "Contact" page in Drupal where someone could send me a message via email. I enabled the contact module that comes with drupal and tested the form. The result was:</p>

<p style="color:red">"Unable to send e-mail. Please contact the site administrator if the problem persists."</p>

<p>The first thing I checked was the Acquia Cloud documentation for email settings. Immediately I see:</p>

<p>"<strong>Note</strong>: You cannot send email from Acquia Cloud Free sites"</p>

<p>Looks like I need to try something else. Turns out there is a module called <strong>SMTP Authentication Support</strong> that I should be able to use with one of my Gmail accounts. I download and install it. The settings for gmail are:</p>
<p>
<strong>SMTP server</strong>: smtp.gmail.com<br>
<strong>SMTP port</strong>: 465<br>
<strong>Use encrypted protocol</strong>: Use SSL<br>
<strong>Username</strong>: [Your full gmail account name including @gmail.com]<br>
<strong>Password</strong>: Your Gmail password<br>
<strong>E-mail from address</strong>: same as Username above<br>
</p>
<p>Everything is set up but I tried sending a test email and it still doesn't work. I check the logs and see:</p>

<p style="color:red">"ERROR:Password not accepted from server"</p>

It turns out Gmail will still block the authentication for security reasons. The solution is to visit this link to enable authentication from a different server. More details found in [this article](http://www.rocketideas.com/2012/05/gmail-error-password-not-accepted-from-server-solved/).

[https://accounts.google.com/b/0/DisplayUnlockCaptcha](https://accounts.google.com/b/0/DisplayUnlockCaptcha)

<p>Now everything seems to be working. I hope this might help someone else.</p>
