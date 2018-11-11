# Ansible Linux Containers to install an OpenWISP 2 server

## Getting Started

This README file is inside a folder that contains a `.lxdock.yml`, which tells LXDock how to set up your container in Linux Containers.

To use the lxdock file, you will need to have done the following:

  1. Install [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html)
  2. Install [Linux Containers](https://linuxcontainers.org/lxd/getting-started-cli/#getting-the-packages)
  3. Install [LXDock](https://lxdock.readthedocs.io/en/stable/getting_started.html#building-lxdock-on-linux)
  4. Clone this repository. See the [GitHub article](https://help.github.com/articles/cloning-a-repository/) if you're unsure how to do this.
  5. Open a shell prompt (Terminal app on a Mac) and navigate to the directory that was created. 
  ```
  cd openwisp-lxdock
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
https://openwisp/admin
username: admin
password: admin
```

## License

Licensed under the GPLv3 License. See the LICENSE file for details.

## Author Information

Reza Juliandri
