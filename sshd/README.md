
Config:

PermitRootLogin yes
UsePAM no
exposed port 22
default command: /usr/sbin/sshd -D
root password: root

Run example

```BASH
docker run -d -P --name test_sshd rastasheep/ubuntu-sshd:14.04
docker port test_sshd 22
>0.0.0.0:49154

ssh root@localhost -p 49154
# The password is `root`
root@test_sshd $
```