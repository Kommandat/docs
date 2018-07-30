---
seo:
  title: Interspire Integration
  description: Interspire Integration
  keywords: marketing, interspire, integration
title: Interspire Integration
group: partners
weight: 0
layout: page
zendesk_id: 200182048
navigation:
  show: false
---

## _Why_ to integrate Interspire with SendGrid

Interspire's [Email Marketer](http://www.interspire.com/emailmarketer/) is a powerful email marketing tool used by some SendGrid customers to carry out more in-depth marketing campaigns. Email Marketer has all the bells and whistles of an email marketing suite, and it's really good at helping customers carry out marketing campaigns from start to finish. SendGrid is really good at giving mail senders all the necessary tools to ensure their mail gets delivered to the inbox. This is why some customers choose to create their email marketing campaigns with Interspire and send the mail through SendGrid, to ensure optimized deliverability of the mail to the inbox. Luckily, Interspire makes this integration with SendGrid simple.

## _How_ to integrate Interspire with SendGrid

First things first, you'll need to log into your Email Marketer account. Once you've done that you can set the application's outbound mail server to point to SendGrid, allowing you to send the mail to us so we can send it to the end recipient. You'll want to navigate to the Dashboard within the account, which should look like this: ![Interspire_doc.1.png](https://sendgrid.zendesk.com/attachments/token/adaznndwouktdj1/?name=Interspire_doc.1.png)

You'll then want to navigate to **Settings > Email Settings** in the upper right corner of the Dashboard. Once inside the Email Settings page you'll see the "Mail Server Details" header near the bottom of the page:

![Interspire_doc.2.png](https://sendgrid.zendesk.com/attachments/token/poikwudjgiidmmx/?name=Interspire_doc.2.png)

In order to set Email Marketer's outbound mail server to point to SendGrid, click the "Let me specify my own SMTP server details" bubble. From there, input the following authentication details:

- **SMTP Hostname** : smtp.sendgrid.net
- **SMTP Username** : [your SendGrid account's username]
- **SMTP Password** : [your SendGrid account's password]
- **SMTP Port** : [the port of your choosing. For more information, see [How to Send an SMTP Email]({{root_url}}/for-developers/sending-email/getting-started-smtp/)]

Once these settings changes have been made within the Email Settings page within your Email Marketer account, all mail from the application will be sent to SendGrid so we can send it to the end recipient. Simple as that.

## Bounce integration

A bounce event occurs when mail is not able to be handed off to the mail servers at the end recipient's address. This could happen for a number of reasons such as a full mailbox at the address, or the address not existing at all. SendGrid generates a Bounces suppression list when you send mail to addresses that end up bouncing. We suppress subsequent mail to these addresses unless you tell us otherwise in the Email Reports tab within your account. There are two primary ways you can integrate these bounces, generated by SendGrid's system, with Email Marketer. You can download a .CSV file of bounced addresses by navigating to Email Reports > Bounces within your SendGrid account. You can then upload this list into Email Marketer's system in order to mark "subscribers" as "unsubscribed." You can also handle bounces more programmatically by using our Event API to capture POSTed events and then unsubscribing subscribers in the Email Marketer system by making calls to their XML API.

More info on SendGrid's Event API can be found [here](http://sendgrid.com/docs/API_Reference/Webhooks/event.html)

More info on Interspire's XML API can be found [here](http://www.interspire.com/emailmarketer/pdf/XMLApiDocumentation.pdf)

