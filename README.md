You are better off with the notes from Techo Tim. My notes are heavily inspired by his Youtube video "Before I do anything on Proxmox, I do this first..." and notes. This is merely my interpretation and to make it easier to remember. I learn from copying notes so please go there instead.

## Updating Proxmox 

Out of the box, a subscription is required. If you do not have a subscription, my recommendation is to disable the Proxmox repo as it requires a valid subscription plan. At 105 Euros per year for a community subscription (as at 2023-12-10), that is a bit steep for me.

### Disable `pve-enterprise` and `enterprise` repos

![[01-enterprise-repos.png]]

Disable the repos using the web interface
![[03-disable-enterprise-repos.gif]]

You can also do this directly with nano, for example ....
From the file `/etc/apt/sources.list.d/pve-enterprise.list` disable pve-enterprise
![[02-disable-enterprise-repo-nano.png]]

However I failed to get the .gpg file to make the repo trusted, the web interface worked better.


### Add the 'no subscription' repos.

Use the web interface to add the repos
![[04-add-no-sub-repos.gif]]

### Run apt-get update and upgrade

![[05-apt-update-upgrade.gif]]


I stopped the animated video after 2 minutes as the .gif was getting too big.




