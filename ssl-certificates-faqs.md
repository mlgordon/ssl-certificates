---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-28"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

<a name="top"></a>
# FAQs: SSL certificates

## Why doesn't the SSL certificate that I ordered automatically show up on the SSL certificates screen?

SSL certificates are issued by a third party certificate Authority, which sends all of the certificate details directly to you in a confidential email. After receiving that email, you have the option to [import the SSL certificate](import-ssl-certificate.html) to the {{site.data.keyword.slportal_full}} should you choose to use the certificate with {{site.data.keyword.BluSoftlayer_full}} products and services. Because we never receive the details for SSL certificate, we are unable to import this data automatically.

## What is an SSL certificate?

SSL certificates are enabled by websites as a security measure to protect the end-user. They are generally utilized when you are required to transmit confidential information to a website, such as name, address, credit card numbers and other personal data or are managing data that requires authentication (such as within our {{site.data.keyword.slportal}}). SSL certificates are requested by the company that runs the website but are issued by a trusted, third-party company that ensures the validity of the website. Secure websites will be preceded by HTTPS in the URL, as opposed to the standard HTTP.

## How can I order an SHA2 SSL?

If you have already ordered an SSL and it is showing errors that the SSL certificate is using SHA-1 instead of SHA-2, you will need to request that we re-issue the SSL. You can do this by submitting a ticket.

If you have not yet ordered an SSL from us, and need to order one with SHA-2, please submit a ticket to manually order an SSL for the domain in question. Our portal still automatically creates SSL certificates using SHA-1 so if you do this, you will then need to have it re-issued.
