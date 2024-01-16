ansible-gradle
=========

Ansible role to automate the installation and configuration of Gradle.

Requirements
------------

- unzip
- wget
- Java installed

Access [gradle Installation link](https://gradle.org/install/#manually) for more details.

Role Structure
--------------

```shell
roles/ansible-gradle
├── defaults
│   └── main.yml
├── files
├── handlers
│   └── main.yml
├── LICENSE
├── meta
│   └── main.yml
├── README.md
├── tasks
│   ├── java_home.yml
│   └── main.yml
├── templates
│   └── gradle_home.sh.j2
├── tests
│   ├── inventory
│   └── test.yml
└── vars
    └── main.yml

8 directories, 11 files

```

Role Variables
--------------

- defaults
### Example
```yaml
gradle_home_path: "/opt/gradle"
gradle_profile: "/etc/profile.d/gradle.sh"
```

- vars
### Example
```yaml
gradle_version: "8.5"
java_home_path: "/usr/local/java/jdk-17.0.9"
```

Dependencies
------------

Java should be installed. Check you system using the following command:

```shell
java -version
```

If you prefer, feel free to use my role [ansible-oracle-java](https://github.com/alexmbarbosa/ansible-oracle-java)

Example Playbook
----------------

An example of how to use your role:

```yml
- hosts: nodes
  become: yes
  roles:
    - ansible-gradle
```

License
-------

GPL-3.0 License

Author Information
------------------

Alex Mendes

https://www.linkedin.com/in/mendesalex
