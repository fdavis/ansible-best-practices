This repo is intended to show my understanding of 'ideal' Ansible playbook directory structure

It is based on Ansible's 'best practices' [page][1]
[1]: http://ansible.cc/docs/bestpractices.html

<pre>
# root of source control repository
├── acme/
│   ├── setup.yml
│   └── stop.yml
├── files/
│   └── some_file_path_foo.conf
├── handlers/
│   └── main.yml
├── tasks/
│   ├── setup.yml
│   └── stop.yml
├── templates/
│   ├── etc_acme_conf_acme.conf
│   └── etc_other_conf_other.conf
├── vars/
│   └── main.yml
└── global_vars.yml
</pre>


TODO:
* make nxserver an actual working example
* be a bit more verbose
* make it better
