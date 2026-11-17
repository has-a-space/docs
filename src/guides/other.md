---
order: 100
label: Other services
icon: server
tags: guides
---

# Setting up other services with has-a.space

## Setting up records

Read the [domain file structure](../useful/domain-structure) and set up the records accordingly.

## Configuring your server

After the pull request is merged, configure your server (apache, nginx, etc.) to work with `subdomain.has-a.space`. If you are unsure how to configure your server, you can [create an issue](https://github.com/has-a-space/register/issues/new/choose) for support.

You should also include `subdomain.has-a.space` in your ssl certificate to get rid of certificate errors.
