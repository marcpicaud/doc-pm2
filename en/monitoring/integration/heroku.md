---
layout: page
title: Heroku | Integration | PM2 Plus Documentation
menu: starter
lang: en
redirect_from: "/monitoring/integration/heroku"
---

# Monitor your Node.js app in Heroku

In seconds, this tutorial will show you how to monitor a node.js application with `pm2` and Heroku.

We assume that your app has already been wrapped with pm2. If not, follow the [heroku tutorial]({{site.baseurl}}/runtime/integration/heroku.md).

---

## Create an account

Register [here](https://app.keymetrics.io/api/oauth/register).

---

## Link with pm2 Monitoring

In order to connect pm2 to the dashboard, you need to add your public and private keys in the environment.

To add your keys, run:

```bash
heroku config:set PM2_PUBLIC_KEY=XXXXXXXXXX PM2_SECRET_KEY=YYYYY
```

?> You can access your keys at the top right of your dashboard

---

## Set the server name in pm2 Monitoring

Set the `PM2_MACHINE_NAME` environment variable to specify a server name:

```bash
heroku config:set PM2_MACHINE_NAME=heroku-server
```

?> The default server name is the hostname (`HOST` environment variable) with a few random characters.

?> Be careful, in case of duplicate hostnames the dashboard will receive data from both instances and flicker.

---

## Next step

Complete your [dashboard configuration]({{site.baseurl}}/monitoring/guide/configuration.md)

---

## Questions ?

We are always happy to help with questions you might have. Search our documentation or check out answers to common questions. You can also post questions or comments to our community forum.