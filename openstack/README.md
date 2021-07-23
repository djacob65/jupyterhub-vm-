
## About authentication to the OpenStack server 

To use an OpenStack cloud you need to authenticate against the Identity
service named keystone, which returns a **Token** and **Service Catalog**.
The catalog contains the endpoints for all services the user/tenant has
access to - such as Compute, Image Service, Identity, Object Storage, Block
Storage, and Networking (code-named nova, glance, keystone, swift,
cinder, and neutron).

Using the 3 *Identity API* does not necessarily mean any other
OpenStack API is version 3. For example, your cloud provider may implement
Image API v1.1, Block Storage API v2, and Compute API v2.0. OS_AUTH_URL is
only for the Identity API served through keystone.

The **clouds.yaml** file can be used by OpenStack tools as a source
of configuration on how to connect to a cloud. If this is your only cloud,
just put this file in ~/.config/openstack/clouds.yaml and tools like
python-openstackclient will just work with no further config. (You will need
to add your password to the auth section)
If you have more than one cloud account, add the cloud entry to the clouds
section of your existing file and you can refer to them by name with
OS_CLOUD=openstack or --os-cloud=openstack

You can retrieve the openstack RC scripts from **OpenStack Dashboard** (web interface) 
at the **API access** section. There, on the upper right corner, a drop down list 
allows you to download the **OpenStack RC file** as well as the **clouds.yaml** file.

![get_auth](https://raw.githubusercontent.com/inrae/jupyterhub-vm/master/images/openstack_authfiles.png)


## About the scripts

The scripts provided here only serve to illustrate an example of VM creation on the OpenStack infrastructure of [IFB GenOuest bioinformatics](https://www.genouest.org/2017/03/02/cluster/). This of course requires access to this infrastructure, as any other infrastructure for that matter.


For more details on the procedure, see https://inrae.github.io/jupyterhub-vm/cloud/


Please refer to the following online documentation:

#### OpenStack Client

* OpenStackClient
  https://docs.openstack.org/python-openstackclient/latest/

* OpenStack Python SDK
  https://docs.openstack.org/mitaka/user-guide/sdk.html

* How to use the OpenStackClient on Microsoft operating systems
  https://docs.ukcloud.com/articles/openstack/ostack-how-use-cli.html

* python-openstackclient 
  https://pypi.org/project/python-openstackclient/


## Acknowledgements

We would like to thank the [IFB GenOuest bioinformatics](https://www.genouest.org/2017/03/02/cluster/) for providing storage and computing resources on its national life science Cloud.

