Role Name
=========

Installes a PostgreSQL Database.

Role Variables
--------------

| var-name | default | description |
| -------- | ------- | ----------- |
| postgresql_version | 12 | postgres version to install |
| postgresql_subnet | 0.0.0.0/0 | subnet to reach the database |
| postgresql_password | "changemeplease" | postgresPW should be set in pipeline |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
        - role: postgresql
          postgresql_version: 12
          postgresql_subnet: "0.0.0.0/0"
          postgresql_password: "changemeplease"
