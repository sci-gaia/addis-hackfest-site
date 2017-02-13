---
layout: page
title: Development Environment
permalink: /dev-env/
author: brucellino
octocat: constructocat2.jpg
contributors:
---
<div class="row">

</div>
The **development environment** refers to a setup where all of the dependencies and configuration needed to both **develop** and **test** your applicaiton are available. The development environment should be as close as possible to the **deployment** environment. The tools described here are the **bare minimum** needed to complete the warmup exercises.

## General description

You will need :

### OS libraries

<ul>
{% for tool in site.data.hackfest.dev_env_generic %}
<li>
  <span class="devicons devicons-{{ tool.icon }}" style="font-size: 2em;"></span><strong>{{ tool.name }}</strong>: {{ tool.more }}.
  <a href="{{ tool.link.url }}" class="btn btn-small">More</a>
</li>
{% endfor %}
</ul>

### Language-specific stacks

**Suggested applications and libraries**

We expect you to know your application stack well and use whichever tools make sense to you. It is very useful to have a REST inspector in your browser for testing, and we suggest using [Postman](https://www.getpostman.com/) for testing how your code uses the APIs of the various components of the platform.



Here are a few suggestions for language-specific stacks:


  * <span class="devicons devicons-python"></span>**Python** : [Python Requests](http://docs.python-requests.org/en/master/)
  * <span class="devicons devicons-ruby"></span>**Ruby** : [HTTParty](http://johnnunemaker.com/httparty/)



# Use a machine provided for you

We have set up access to a machine (via ssh) which is preconfigured as a development environment. We use _your_ ssh keys from your github account to provide you access (see the [before checklist]({{ site.url}}/before-checklist/)). In order to access the machine, you should use your github username :

`ssh <gihtub username>@sgw-dev.sci-gaia.eu`

_e.g._ :

`ssh brucellino@sgw-dev.sci-gaia.eu`

This machie hass been provisioned with most of  the tools we mention above, so that you can do the warmup sessions during hte hackfest. However, it will be destroyed soon after the hackfest; it may be easier and more comfortable to work on your own machine, or a remote development environment closer to home.

# Set up your own


## <i class="fa fa-asterisk"></i> (Beta) Use our playbook

You can use the same Ansible playbook that we use to set up the development environment. Some tweaking on your part may be necessary (and we would welcome pull requests for things you consider necessary !), but here's what to do when setting up the development environment :

  1. Clone the [Hackfest-Prep](https://github.com/AAROC/e-Research-Hackfest-Prep) repo : `git clone https://github.com/AAROC/e-Research-Hackfest-Prep`
  1. Get Ansible, if you don't : [see Ansible website](http://docs.ansible.com/ansible/intro_installation.html)
  1. The playbooks are in `e-Research-Hackfest-Prep/services/Ansible`
  1. Run the playbook against your local machine  : `ansible-playbook -i localhost, -c local development-environment.yml`

<span class="text-info">More details coming soon</span>

# Use Docker

We're working on a Docker image for you to use. Stay tuned.
<span class="text-info">Coming soon</span>
