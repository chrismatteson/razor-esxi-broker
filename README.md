# razor-esxi-broker

This project is a broker for Razor that uses William Lam's python
script to automate the attachment of a new ESXi host to an existing
vCenter server.  The broker should be installed into the brokers
directory for the Razor Server, which by default is:
/opt/puppetlabs/server/apps/razor-server/share/razor-server/brokers/

There are four configuration variables which can be specified when 
the broker is created:
vc_server: Required.  The vCenter server which to connect to.
vc_cluster: Optional.  The path of the vCenter cluster to add to.
vc_username: Required.  The username to authenticate to vCenter
vc_password: Required.  The password to authenticate to vCenter

The recommendation is to create a limited user account just for
adding hosts to vCenter so it's less of a security issue if this
username and password is compromised as it is sent to any new
system.  Instructions for how to do this are included in William 
Lam's blog post which can be found here:
http://www.virtuallyghetto.com/2011/03/how-to-automatically-add-esxi-host-to.html
