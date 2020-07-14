---
title: "Introducing Able3 Chart Services"
date: 2020-07-14
---
AppSheet allows you to use a workflow rule with a webhook action to post to any web service on the Internet. This is a powerful way to integrate your AppSheet app with a variety of popular services like Zapier, Slack, Twitter, Twilio, and IFTTT among others. Currently AppSheet apps can use a webhook as a means of invoking a "fire and forget" operation using the web service. This means that a webhook cannot make dynamic changes to the app data which would change the behavior of the app in real time.

As opposed to other services like Zapier, Twitter and other REST APIs, Able3 REST API services are designed in a slightly different way. They leverage a combination of AppSheet actions which can launch external sites and Google Apps Scripts which can have endpoints to return data managed within your apps.

The figure below illustrates this architecture.

![Able3 Architecture]({{ BASE_PATH }}/images/callback-arch.png)

To use external web services, in general, you must set up a developer account with the web service which assigns you an API key. However, as Able3 Chart Services (ACS) are still in beta testing, all that is needed is to register your app for using the service.

## Steps involved in the use of Able3 Chart Service

1. Set up an action in AppSheet to go to an external URL (External: go to a website). 
2. Register to use the Able3 Chart Service by providing three pieces of information.
   1. Your email address
   2. Your App Name
   3. A URL endpoint (see below).
3. Create a Google App Script project containing a doGet() function to return a JSON payload and publish it as a web app.

If you are ready to get started, you will find a demo app and its internals here
