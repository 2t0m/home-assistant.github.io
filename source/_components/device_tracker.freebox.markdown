---
layout: page
title: "Freebox"
description: "Instructions how to integrate Freebox routers into Home Assistant."
date: 2017-10-27 23:00
sidebar: true
comments: false
sharing: true
footer: true
logo: http://www.free.fr/freebox/im/logo_free.png
ha_category: Presence Detection
ha_release: "?"
ha_iot_class: "Local Polling"
---


The `freebox` platform offers presence detection by looking at connected devices to a [Freebox](https://fr.wikipedia.org/wiki/Freebox) based router from [Free](https://www.free.fr/), which is one of the main Internet provider in France. Freebox is a generic name for different hardware routers. The platform has only been tested on a Freebox mini because it's the only model the developer owns. 

For now, the Freebox must be on the same local network as the Home Assistant installation. To get the username (aka `app_id`) and password (aka `app_token`), you need to [Request authorization](https://dev.freebox.fr/sdk/os/login/#request-authorization) and [Track authorization progress](https://dev.freebox.fr/sdk/os/login/#track-authorization-progress) following this [guide](https://dev.freebox.fr/sdk/os/login/). You can use [Postman](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop) to easily make GET and POST requests.

To use a Freebox router in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
device_tracker:
  - platform: freebox
    username: fr.freebox.testapp
    password: bi9dpCD4v75mtX7HTGFxPeATc0kYWe0+aHfdBDx3wiEYEtULZ3kRKwdjvJHYDFGAT
```

See the [device tracker component page](/components/device_tracker/) for instructions how to configure the people to be tracked.
