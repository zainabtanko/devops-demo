# Install Puppet cluster on Ubuntu
## On Puppetserver

``` bash
wget https://apt.puppet.com/puppet7-release-focal.deb
dpkg -i puppet7-release-focal.deb
apt-get update
apt install openjdk-8-jre-headless puppetserver  puppet-agent
source /etc/profile.d/puppet-agent.sh
export PATH=/opt/puppetlabs/bin:$PATH
puppet config set server <puppetserver-fqdn> --section main
```

set correct java heapsize values for puppet in file `/etc/defaults/puppetserver`

Start puppetserver 
```bash
systemctl start puppetserver
```

## On Puppet Agent Node

wget https://apt.puppet.com/puppet7-release-focal.deb
dpkg -i puppet7-release-focal.deb
apt-get update
apt-get install puppet-agent
source /etc/profile.d/puppet-agent.sh
export PATH=/opt/puppetlabs/bin:$PATH
puppet config set server <puppetserver-fqdn> --section main

# Add the Agent machine as Node to Puppetserver
## On Puppet Node
`puppet ssl bootstrap`

## On Puppetserver
`puppetserver ca sign --all`

## On Puppet Node
`puppet ssl bootstrap`
