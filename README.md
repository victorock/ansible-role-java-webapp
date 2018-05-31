Ansible Tomcat Webapp
=========

Simple Role to Deploy in Tomcat an webapp taken from maven repository.

Requirements
------------

None

Role Variables
--------------

```YAML
java_webapp_version:        "1.0"
java_webapp_repository_url: "http://artifactory.devops.victorock.io/artifactory/libs-release-local"
java_webapp_group_id:       "com.phillyair"
java_webapp_artifact_id:    "phillyapp"
java_webapp_extension:      "war"
java_webapp_dir:            "/usr/share/tomcat/webapps/"
```

Dependencies
------------

The following dependencies are required (`see meta/main.yml`):

```YAML
dependencies:
  - role: victorock.tomcat
```

Example Playbook
----------------

```YAML
- name: "Deploy Tomcat Webapp"
  hosts: tomcat
  become: true

  roles:
    - victorock.tomcat-webapp
```

License
-------

GPLv3

Author Information
------------------

Victor da Costa
