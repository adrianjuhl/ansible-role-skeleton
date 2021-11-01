Ansible role: skeleton
=========

A skeleton of a role. See below for how the role was initialized.

Requirements
------------

None.

Role Variables
--------------

None.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: adrianjuhl.skeleton }

License
-------

MIT

Author Information
------------------

[Adrian Juhl](http://github.com/adrianjuhl)


Development Notes
-----------------

Procedure to create this skeleton:
```
Create a new repository in github named ansible-role-skeleton
$ git clone git@github.com:adrianjuhl/ansible-role-skeleton.git
$ cd ansible-role-skeleton
$ git.init-clone-main
    equivalent to:  $ touch .gitignore && git add .gitignore && git commit -m 'Initial commit.' && git branch -M main && git push -u
$ git checkout -b 1.0.0-develop
$ ansible-galaxy init skeleton
$ mv skeleton/meta .
$ rm -rf skeleton
    edit the readme as appropriate (this readme is an example)
    edit the meta/main.yml file as appropriate, including setting role_name (see the example in this repo)
    edit the tasks/main.yml file and others as appropriate to implement the role tasks
$ git add .
$ git commit -m "Implement role."
$ git push -u
    continue development, commits, pushes
```

While the role is in development, the role can be imported by including the following in the requirements.yml file:
```
- src: https://github.com/adrianjuhl/ansible-role-skeleton
  scm: git
  version: 1.0.0-develop
  name: adrianjuhl.skeleton
```
(where version is a branch name)

Once a version of the role is stable:
- (optionally) rebase/squash onto main
- create a tag
```
$ git tag 1.0.0
$ git push origin 1.0.0
```

Then, import the role into Ansible Galaxy [here](https://galaxy.ansible.com/my-content/namespaces), click 'Add Content' and then choose the repo.

Then, the requirements.yml file section can be updated to refer to the ansible galaxy role name and version like:
```
- src: adrianjuhl.skeleton
  version: 1.0.0
```
(where version is a tag value)
