# ansible-role-mylar3
 
=========

Ansible Role to install mylar3, an automated downloader, watchlist, monitoring program for Comic Books.

Requirements
------------

Minimum Ansible version required is Ansible 2.9

Role Variables
--------------
Role variables have good defined defaults, which are located in `defaults/main.yml`.
Current version includes the following variables with default values:

### Defaults
| Name               | Default Value | Description                  |
|--------------------|---------------|------------------------------|
| `mylar_user`       | mylar | The primary user to run Mylar3       |
| `mylar_uid`        | *optional* | Commented out by default |
| `mylar_group`      | media | The primary group for `mylar_user` |
| `mylar_group_gid`  | *optional* | Commented out by default |
| `mylar_install_dir` | /opt/Mylar | Install directory for Mylar3 |
| `mylar_config_dir` |  /opt/data/mylar | Data directory to store configuration |
| `mylar_git_repo` | https://github.com/mylar3/mylar3 | Link to the Mylar3 git hub repo |
| `mylar_port` | 8090 | Port in which Mylar operates on, to add to Firewalld |
| `mylar_python_version` | python38 | Minimum Python version to run Mylar |
| `mylar_packages` |   ```- unrar```  ```- git``` | List of Packages Required to install and run Mylar3 |

Dependencies
------------

None

Example Playbook
----------------

   - hosts: mylar3_servers
      roles:
        - aaron-cole.mylar3


License
-------

GPLv3

Author Information
------------------

Created by Aaron Cole

