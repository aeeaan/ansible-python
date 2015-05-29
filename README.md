correcthorse.python
=========

This role is for installing the requirements for a python web application.

Role Variables
--------------


| Variable                              | Default                       | Notes                                         |
| :---                                  | :---                          | :---                                          |
| python_base_name			| 'python'			| 						|
| python_wsgi_embedded			| false				|						|
| python_wsgi_ignore_deprecation	| true				|						|
| python_wsgi_optimize			| 0				|						|

| Other Variables                       | Default                       | Notes                                         |
| :---                                  | :---                          | :---                                          |
| common_development_tools		| false				| Does your requirements.txt need a C compiler? |

Example Playbook
----------------

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
