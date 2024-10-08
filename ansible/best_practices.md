<h1 align="center"> Ricardo's best practices for automation with Ansible </h1>

<h2 align="center"> Recommendations </h2>




- keep it simple, complexity kills productivity

- optimize for readability, if something is easy to read then it's easy to understand and easy to troubleshoot

- use a good editor like VSCode, VSCodium, Sublime Text Editor etc and even try vim-ansible

- think declaratively understanding that your playbooks aren't code but the declared state that Ansible will synchronize your inventory hosts to

- stay organized and use version control

- adopt a style guide or create one yourself for your own needs

- don't reinvent the wheel and use roles where you can and pick trusted or well-known authors and even better use Red Hat Certified Collections

- use variables and while there are 22 different ways to use variables, you should use them in a way that makes sense for your solution

- take advantage of inventory groups and the group_vars/ and host_vars/ directories, remembering that hosts can be members of many groups structured by geography, environment, purpose, etc

- endeavor to use dynamic inventories to allow Ansible to contact an infrastructure provider to enumerate the latest list of inventory hosts known to that provider (e.g. Satellite knows which clients are currently registered with it)

- use descriptive variable names and avoid naming your variables in a way that conflicts with module options

- name your plays, blocks, tasks, handlers

- "use includes to your advantage: divide and conquer"

- use modules like command and shell when a suitable module cannot be found

- use {{ ansible_managed }} to mark files as being managed by Ansible so that users don't overwrite their content

- enable privilege escalation only when needed

- avoid automating by logging in as root as transactions are harder to audit, use sudo instead

- run your playbooks from a centralized controller

- use execution environments for frequently executed Ansible operations that require customizations in the form of collections, python dependencies, and system executables
