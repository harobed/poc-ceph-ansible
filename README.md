# Quickstart

```
$ git clone git@github.com:harobed/poc-ceph-ansible.git
$ cp poc-ceph-ansible
$ git submodule init
$ git submodule update
```

Next:

* go in [vagrant-3mons-3osd](vagrant-3mons-3osd/) folder
* or go in [vagrant-3mons-osd](vagrant-3mons-osd/) folder

# Operations

## Show where rbd disk are mapped

```
root@ceph-test-1:/home/vagrant# rbd info image2
rbd image 'image2':
	size 400 MB in 100 objects
	order 22 (4096 kB objects)
	block_name_prefix: rbd_data.102174b0dc51
	format: 2
	features: layering
	flags:
root@ceph-test-1:/home/vagrant# rados -p rbd listwatchers rbd_header.102174b0dc51
watcher=172.28.128.9:0/3104046451 client.4135 cookie=1
```
