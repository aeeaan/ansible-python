correcthorse.python
=========

This role is for installing the requirements for a python web application.

Role Variables
--------------


| Variable                              | Default                       | Notes                                         |
| :---                                  | :---                          | :---                                          |
| python_base_name			| 'python' or 'python3'			| 'python3' is default on RHEL 8 |
| python_install_python2  | false                   | install RHEL 8 python 2 stream  |
| python_pip_executable			|	version ansible chooses |					|
| python_pip_packages			| []				| 						|
| python_virtualenvs			| []				|						|
| python_virtualenv_root		| /opt/virtualenvs		|						|
| python_virtualenv_owner		| root				|						|
| python_extra_packages			| []				| meant for global python packages that are part of distro |

#### Complex variables

    python_virtualenvs:
      - name: localhost.localdomain          (required)
        requirements: /tmp/requirements.txt  (required)
        owner: vagrant			     (optional, defaults to python_virtualenv_owner)
        site_packages: yes		     (optional, defaults to virtualenv default of no)
      - name: localhost2.localdomain
        requirements: /tmp/requirements.txt

| Other Variables                       | Default                       | Notes                                         |
| :---                                  | :---                          | :---                                          |
| common_development_tools		| false				| Does your requirements.txt need a C compiler? |

Example Playbook
----------------

NOTE: Since we use virtualenv parameter in pip module, you may need to set INTERPRETER_PYTHON so the correct pip is used.
INCOMPLETE: using virtualenvs with non-default python_base_name's

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: correcthorse.python }

License
-------

MIT

Author Information
------------------

* [Joshua Rusch](https://correct.horse/)
