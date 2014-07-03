OpenStack Nova - Eguan distribution
*************************************

This is OpenStack's Nova compute service, patched for the eguan project.

The patch adds support for the NBD network storage protocol to the libvirt hypervisor driver. It is designed to communicate with the eguan volume driver installed with the Cinder storage service.

Upon detecting NBD client support on the hypervisor, the patch adds a 'nbd_client_id' field to the client connection initiation request that is answered by the eguan volume driver with NBD-specific connection parameters.

Please refer to the eguan documentation for more details on how to setup the eguan service.

Below is the original README content.

OpenStack Nova README
=====================

OpenStack Nova provides a cloud computing fabric controller,
supporting a wide variety of virtualization technologies,
including KVM, Xen, LXC, VMware, and more. In addition to
its native API, it includes compatibility with the commonly
encountered Amazon EC2 and S3 APIs.

OpenStack Nova is distributed under the terms of the Apache
License, Version 2.0. The full terms and conditions of this
license are detailed in the LICENSE file.

Nova primarily consists of a set of Python daemons, though
it requires and integrates with a number of native system
components for databases, messaging and virtualization
capabilities.

To keep updated with new developments in the OpenStack project
follow `@openstack <http://twitter.com/openstack>`_ on Twitter.

To learn how to deploy OpenStack Nova, consult the documentation
available online at:

   http://docs.openstack.org

For information about the different compute (hypervisor) drivers
supported by Nova, read this page on the wiki:

   https://wiki.openstack.org/wiki/HypervisorSupportMatrix

In the unfortunate event that bugs are discovered, they should
be reported to the appropriate bug tracker. If you obtained
the software from a 3rd party operating system vendor, it is
often wise to use their own bug tracker for reporting problems.
In all other cases use the master OpenStack bug tracker,
available at:

   http://bugs.launchpad.net/nova

Developers wishing to work on the OpenStack Nova project should
always base their work on the latest Nova code, available from
the master GIT repository at:

   http://github.com/openstack/nova

Developers should also join the discussion on the mailing list,
at:

   http://lists.openstack.org/cgi-bin/mailman/listinfo/openstack

Any new code must follow the development guidelines detailed
in the HACKING.rst file, and pass all unit tests. Further
developer focused documentation is available at:

   http://nova.openstack.org/

For information on how to contribute to Nova, please see the
contents of the CONTRIBUTING.rst file.

-- End of broadcast
