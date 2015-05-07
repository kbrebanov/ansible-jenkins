jenkins
=======

Installs Jenkins.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name            | Default                                                                                                                                                                                                                                            | Description                       |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| jenkins_version | 1.596.2                                                                                                                                                                                                                                            | Version of Jenkins LTS to install |
| jenkins_plugins | "ant credentials cvs external-monitor-job javadoc junit ldap mailer mapdb-api matrix-auth matrix-project maven-plugin antisamy-markup-formatter pam-auth scm-api script-security ssh-credentials ssh-slaves subversion translation windows-slaves" | List of installed plugins         |

Dependencies
------------

- kbrebanov.java (OpenJDK 7)

Example Playbook
----------------

Install Jenkins
```
- hosts: all
  roles:
    - { role: kbrebanov.jenkins }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
