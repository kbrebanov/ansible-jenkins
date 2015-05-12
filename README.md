jenkins
=======

Installs Jenkins.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                        | Default                                                                                                                                                                                                                                                                | Description                         |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| jenkins_version             | 1.596.2                                                                                                                                                                                                                                                                | Version of Jenkins LTS to install   |
| jenkins_plugins             | [ant, credentials, cvs, external-monitor-job, javadoc, junit, ldap, mailer, matrix-auth, matrix-project, maven-plugin, antisamy-markup-formatter, pam-auth, script-security, ssh-credentials, ssh-slaves, subversion, translation, windows-slaves] | List of installed plugins           |
| jenkins_num_executors       | 2                                                                                                                                                                                                                                                                      | Number of executors to start        |
| jenkins_url                 | http://localhost:8080/                                                                                                                                                                                                                                                 | Jenkins URL                         |
| jenkins_admin_address       | "address not configured yet &lt;nobody@nowhere&gt;"                                                                                                                                                                                                                    | Jenkins admin email address         |
| jenkins_no_usage_statistics | "false"                                                                                                                                                                                                                                                                | Disable sending of usage statistics |

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
