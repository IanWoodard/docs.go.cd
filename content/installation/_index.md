---
description: GoCD installation instructions for both server and agent.
keywords: install gocd, open source cd tool, free cd tool, gocd agents, gocd server, jenkins
title: Installing GoCD
url: /installation/
BookShowToc: false
---


# Installing GoCD

GoCD consists of two installable components. The GoCD Server and one or more GoCD Agents. They have a one-to-many
relationship in that many GoCD agents can connect to one GoCD Server. To do any real work, you need at least one agent,
since agents are the real builders or work executors in the system.

Since installation instructions vary per operating system, the installation instruction pages linked below will ask you
to choose your operating system and then provide you instructions for that operating system.

<div id="go-to-gocd-server-installation-instructions-installing-go-server-html">
  Go to: <a href="installing_go_server.html">GoCD Server installation instructions</a>
</div>

<div id="also-go-to-gocd-agent-installation-instructions-installing-go-agent-html">
  Also, go to: <a href="installing_go_agent.html">GoCD Agent installation instructions</a>
</div>

Whatever operating systems you install the GoCD server and (at least one) GoCD agent on, the default port used by the
server is 8153 (HTTP). So, after installation you should be able to access `http://localhost:8153` and see a screen
such as this:

![Initial screen, upon installation](/images/gocd_new_installation_startup.png)

Once the agent is started, switching to the agents tab by clicking on the "Agents" link in the header should take you to
a screen where the agent shows up and is idle. Like this:

![Agents screen, with one idle agent](/images/gocd_new_installation_agents_page.png)

An agent or agents can be installed on any node, and not necessarily the node that the GoCD Server is installed on. The
only requirement is that port 8153 of the GoCD Server (or an alternative HTTPS port, if using a fronting [reverse proxy](configure-reverse-proxy.html)) 
is accessible from the node that the agents are installed on.

If you are still having trouble with the installation, take a look at the [troubleshooting guide](troubleshoot_installer.html).
