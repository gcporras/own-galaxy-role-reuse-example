# Own-Galaxy-Role-Reuse-Example

This is an example of the use of [librarian-ansible](https://github.com/bcoe/librarian-ansible) to install and reuse
roles defined outside [Ansible Galaxy](https://galaxy.ansible.com). In this example the external role is installed
from a private [Gitlab](https://about.gitlab.com) repository.

Used for
[DevOps Montreal](http://www.devopsmtl.com) Get Back to Work edition - September 2014.

Presentation Title:  [Create your Orchestration Galaxy With Ansible](https://speakerdeck.com/gerardocepeda/create-your-orchestration-galaxy-with-ansible)

## Instructions:

Install librarian-ansible (bundler will install librarian-ansible - Defined in Gemfile):

``` shell
> bundle install
```

Install external roles ([own-galaxy-gitlab-server](https://github.com/gcporras/own-galaxy-gitlab-server) must be running)

``` shell
> cd ansible
> librarian-ansible install
```

Execute the ansible playbook 

```shell
> cd ..
> ansible-playbook ansible/site.yml -i ansible/hosts
```

