---
layout: page
title: "Instructor Notes"
permalink: /guide/
---

To create a VM for students to use for setting up their remote desktops use `cloud_init_desktop.yml` file in the [cloud-init-files](https://github.com/acenet-arc/desktops_in_the_cloud/tree/main/cloud-init-files) folder when creating the VM to perform setup. Copy and paste the contents of that file into "Customization Script" under the "Configuration" tab in the popup while creating a VM in OpenStack. Under the `users` section add the name for an admin user and their public key. This script will also setup a guest account on the VM. It is best to create 1 VM per student with a minimal flavor, 1 VCPU, 1-2GB of RAM, and 20GB of disk should be plenty.

Once setup has completed have a look at the VM log to find the login password for guest accounts. Search for "Guest accounts passphrase:".
