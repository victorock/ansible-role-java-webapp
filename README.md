Ansible Phillyapp
=========

Simple Role to Deploy Phillyapp.

Requirements
------------

None

Role Variables
--------------

```YAML
phillyapp_version:        "1.0"
phillyapp_stage:          "release"
phillyapp_repository_url: "http://artifactory.devops.victorock.io/artifactory/"
phillyapp_repository:     "{{ phillyapp_repository_url }}/libs-{{ phillyapp_stage }}-local"
phillyapp_group_id:       "com.phillyair"
phillyapp_artifact_id:    "phillyapp"
phillyapp_extension:      "war"
phillyapp_dir:            "/usr/share/tomcat/webapps/"
```

Dependencies
------------

The following dependencies are required:

None

Example Playbook
----------------

```YAML
- name: "Deploy Phillyapp"
  hosts: phillyapp
  become: true

  roles:
    - victorock.phillyapp
```

License
-------

GPLv3

Author Information
------------------

Victor da Costa
