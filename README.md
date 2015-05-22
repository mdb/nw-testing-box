# nw-testing-box

A ready-to-go headless Ubuntu box for running NW.js unit and end-to-end
tests via Xvfb.

## Getting started

Install [Vagrant](https://www.vagrantup.com) & [ansible](http://www.ansible.com).

1. `vagrant up` to provision the box with the ansible playbook
2. `vagrant ssh` to shell into the box
3. `cd /vagrant` to enter the directory syncd to your host machine
4. `git clone https://github.com/mdb/nw-app-testing.git` to clone an example app
5. `cd nw-app-testing`
6. `npm install`
7. `gulp test` to run unit tests
8. `gulp e2e` to run end-to-end tests

## Bonus - debug from your Mac via VNC

The Vagrant box has no GUI, but your Mac does! Connect to the Vagrant box from
your Mac via VNC to observe and debug.

Install & run x11vnc on the vagrant box

1. `vagrant ssh`
2. `sudo apt-get install x11vnc`
3. `x11vnc -display :0 &`

Install and run Tiger VNC Viewer on your Mac

1. `brew install Caskroom/cask/tigervnc-viewer`
2. start Tiger VNC viewer on `localhost:5901`

Run the tests on the Vagrant box and watch from Tiger VNC Viewer.
