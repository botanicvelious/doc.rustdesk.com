---
title: All with Github Actions
weight: 35
---

{{% notice note %}}
This build uses github actions, you will need a github account, also building can be slow, however this requires no development enviroment.
{{% /notice %}}

## Make a Fork

Goto https://github.com/rustdesk/rustdesk/fork and click "create fork"

## Set your enviroment variables (Optional)

{{% notice note %}}
You only need to do this if you want to change the default server and public key.

The server url and key you are using is hidden from other users on Github however they can download your client and connect to your server. If you require a fully private repo you can import the rustdesk client repo using https://github.com/new/import. **If you use a private repo you have limited amounts of builds you can create per month, if you need more you will need to have a paid Github account.**
{{% /notice %}}

On your fork you just created goto settings -> Secrets and Variables -> Actions

Click New repository Secret for the name put RENDEZVOUS_SERVER for the secret put your servers name/ip address.

Click Add Secret

Click New repository Secret for the name put RS_PUB_KEY for the secret put your servers public key.

Click Add Secret

## Enable workflows

On your fork you just created goto settings -> Actions -> General

On the right select "Allow all actions and reusable workflows"

Once workflows are enabled you can click "Flutter Nightly Build" on the left then click "Run workflow" on the right to build the rustdesk clients for all of the supported platforms.

## Enable upload permissions for workflows

On your fork you just created goto settings -> Actions -> General 

Scroll down and under Workflow permissions enable "Read and Write permissions.

## Download your built packages

After the workflow is done running you can download the packages it built. 

Goto the main page of your fork, on the right click releases. The packages you just built will show up under nightly.
