# ansible-local-demo

## about

This repository is a public sample repository for our remote configuration management tool.
It's designed to test our remote configuration management client on your systems without having any impact on your system, so there's only one task: have a 10-second-break.


```
- name: Pause for 10 seconds
  ansible.builtin.pause:
    seconds: 10
```

The remote configuration management tool is a program designed to (secure) checkout a (secure) git repository containing any ansible playbooks you need to configure your Linux systems - both client and servers.

## manually testing

At first you should test the playbook on your desired system to make sure you have everything you need.

```
ansible-playbook playbook.yaml --inventory 127.0.0.1,
```

## agent testing

Since this is a public repository you can use test the agent both with or without authentication.

## compatibility

Tested without warnings and errors using
- ansible core 2.16.4
- python 3.10.12

on Linux Mint 21.3 but should work on many other systems since it's very simple ansible code.