On second thought, I was probably wrong, under the included ascii art depiction 
of the directory structure is a comment of 
    The tasks are individually broken out in ‘acme/tasks/setup.yml’
... I think an individual folder per task/service/other like [sfromm's repo][1] uses is probably the way to go.  (???)
[1]: https://github.com/sfromm/ansible-playbooks


This repo is intended to show my understanding of 'ideal' Ansible playbook directory structure

At a glance this seems like a simple structure, bit in practice it seems awfully complex to break up tasks.
On one hand, it does not make sense to mix a bunch of files for different playbooks because they are
pretty disjoint operations.
If playbooks are so simple that they are practically atomic, then is nothing to share.
If playbooks are very complex then they probably cannot be used for any other purpose than their own.
The middle ground where playbooks guts can be swapped around seems like a slim ground to me at the moment.

It is based on Ansible's [best practices][1]
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
* be a bit more verbose
* make it better
