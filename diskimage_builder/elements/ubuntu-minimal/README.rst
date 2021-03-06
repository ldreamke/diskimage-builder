==============
ubuntu-minimal
==============

The ``ubuntu-minimal`` element uses debootstrap for generating a
minimal image. In contrast the ``ubuntu`` element uses the cloud-image
as the initial base.

By default this element creates the latest LTS release.  The exact
setting can be found in the element's ``environment.d`` directory in
the variable ``DIB_RELEASE``.  If a different release of Ubuntu should
be created, the variable ``DIB_RELEASE`` can be set appropriately.

Note that this element installs ``systemd-sysv`` as the init system for
18.04+.

Environment Variables
---------------------

DIB_UBUNTU_KERNEL:
  :Required: No
  :Default: ``linux-image-generic``
  :Description: Specifies the kernel meta package to install in the image.
  :Example: ``DIB_UBUNTU_KERNEL=linux-image-kvm``
  :Options: ``linux-image-generic``, ``linux-image-kvm``,
            ``linux-image-virtual``
  :Notes: The element must know about the package, otherwise it will select
          the default.

.. element_deps::
