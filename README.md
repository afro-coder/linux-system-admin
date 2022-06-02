# Linux System Admin Primer
A repository for getting started with Linux

To get started, install Linux in a Virtual machine.

Easiest way to do this is via [Vagrant](https://www.vagrantup.com/downloads)
```
$ vagrant init
```
After that edit the vagrant file.
```
vim Vagrantfile
```
Change this to the following or any VM you'd like,
```
config.vm.box = "centos/stream8"
```
Or follow the official [docs](https://www.vagrantup.com/docs/boxes)

Finally do
```
vagrant up

Once that is done
vagrant ssh
```

This guide is a simple primer of what I taught, I haven't followed any linux tutorials before so I'm not sure how I'd teach that to someone.

The first guide is stored in day_1.md
