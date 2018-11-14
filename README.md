# LXDock  OpenWISP2

Ansible LXDock profile to install an OpenWISP 2 server

## Background

LXDock and LXD can be used to quickly build or rebuild Linux Containers (LXC).

This LXDock profile installs OpenWISP2 server using the [Ansible](http://www.ansible.com/) provisioner.

This README file is inside a folder that contains a `lxdock.yml`, which tells LXDock how to set up your container in Linux Containers.

To use the lxdock file, you will need to have done the following:

  1. Install [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html)
  2. Install [LXD](https://linuxcontainers.org/lxd/getting-started-cli/#getting-the-packages)
  3. Install [LXDock](https://lxdock.readthedocs.io/en/stable/getting_started.html#building-lxdock-on-linux)
  4. Clone this repository. If you're unsure how to do this see:
      * [Gitlab Repository](https://docs.gitlab.com/ee/gitlab-basics/command-line-commands.html#start-working-on-your-project)
      * [GitHub Repository](https://help.github.com/articles/cloning-a-repository/)
  5. Open a shell prompt (Terminal app on a Mac) and navigate to the directory that was created.
  ```
  cd lxdock-openwisp2
  ```
  6. Run the following command to install the necessary Ansible roles for this profile:
  ```
  ansible-galaxy install -r requirements.yml
  ```

Once all of that is done, you can simply type in `lxdock up` in this directory, and LXDock will create a new container, install the base box, and configure it.

Once the new Container is up and running (after `lxdock up` is complete and you're back at the command prompt), you can log into it by typing in `lxc exec <container-name> -- bash`. Otherwise, the next steps are below.

### Login on OpenWISP2

When the playbook ran successfully, you can log in at:

```code
https://openwisp.lxd/admin
username: admin
password: admin
```

## License

Licensed under the GPLv3 License. See the LICENSE file for details.

## Author Information

[Marco Giuntini](https://gitlab.com/hispanico)  
Reza Juliandri  
