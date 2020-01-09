Ubuntu Server Student Environment
=================================

Scripts and config files for configuring an Ubuntu server for multiuser student use

Installation
------------

After a clean installation of Ubuntu Server, a new system can be configured by running as a sudoer:

`curl https://raw.githubusercontent.com/jncraton/ubuntu-server-student-env/master/setup | bash`

For a complete list of packages and tools that are available, view the `setup` script. There are a few flags provided to add packages that may be useful only in certain courses. Here's the complete usage that can be viewed by running `./setup -?`:

    SYNOPSIS
    ./setup: [-lsd]
    
    DESCRIPTION
    
    Installs packages and configures system
    
      -l Include uncommon programming languages
      -s Include data stores
      -d Include data science tools and languages
    
    This program is idempotent, so a newer version can be run on an existing system without issues.

Adding Students
---------------

After successful installation, students can be added using the following command:

`addstudent [student]...`

For example:

`addstudent alice bob charlie`

Here's the usage info for that command:

    SYNOPSIS
    ./addstudent [student]...
    
    DESCRIPTION
    
    Adds new students to the system.
    
    This will create new users and home directories for each student. Accounts will be given a default password of Password1. Students will be prompted to change this password on first login.
