===================================
 The :program:`nova` Shell Utility
===================================

.. program:: nova
.. highlight:: bash

The :program:`nova` shell utility interacts with OpenStack Nova API from the
command line. It supports the entirety of the OpenStack Nova API.

First, you'll need an OpenStack Nova account and an API key. You get this by
using the `nova-manage` command in OpenStack Nova.

You'll need to provide :program:`nova` with your OpenStack username and API
key. You can do this with the `--os-username`, `--os-password` and
`--os-tenant-id` options, but it's easier to just set them as environment
variables by setting some environment variables:

.. envvar:: OS_USERNAME

    Your OpenStack Nova username.

.. envvar:: OS_PASSWORD

    Your password.

.. envvar:: OS_TENANT_NAME

    Project for work.

.. envvar:: OS_AUTH_URL

    The OpenStack API server URL.

.. envvar:: OS_COMPUTE_API_VERSION

    The OpenStack API version.

.. envvar:: OS_REGION_NAME

    The Keystone region name. Defaults to the first region if multiple regions
    are available.

For example, in Bash you'd use::

    export OS_USERNAME=yourname
    export OS_PASSWORD=yadayadayada
    export OS_TENANT_NAME=myproject
    export OS_AUTH_URL=http://<url-to-openstack-keystone>:5000/v3/
    export OS_COMPUTE_API_VERSION=2.1

From there, all shell commands take the form::

    nova <command> [arguments...]

Run :program:`nova help` to get a full list of all possible commands, and run
:program:`nova help <command>` to get detailed help for that command.

Reference
---------

For more information, see the reference:

.. toctree::
   :maxdepth: 2

   /cli/nova
