How to setup Vagrant, Ruby on Rails and deploying with Capistrano
=======================================================================

The purpose of this repository to practice setting up a virtual 
environment through Vagrant, for developing a Ruby on Rails application 
and then deploying the application to a remote service (like Heroku) via 
Capistrano.

_This is also for use for fellow students to learn from and copy._

Step 1
---------------------------------------------------------------------
First download and install the following programs:
- [Git][]
- [Vagrant][]
- [VirtualBox][] or [VMFusion][]

You will need Git to clone repositories, but also to use its included 
"Git bash" if you are running on Windows and do not have some basic 
Linux plugins installed (via [MinGW][], [Cygwin][], etc).

Step 2
---------------------------------------------------------------------
In order to quickly setup the developer environment find a premade 
manifeat or recipe to use in Vagrant for installing the appropraite 
software, like [MySQL][] for databases and [Apache][] for serving webpages 
or applications.

_*Note: Any premade Vagrant box will by default have Ruby installed, to 
allow provisioners like [Chef][] or [Puppet][] to run and install software._

For this Project I will be following SpinUpLabs' 
[Vagrant: Rails development environment][] article and using their 
[Vagrant file and Puppet manifest][SpinUpLabs' Vagrant Dev Box] to quickly 
start building an ideal Ruby on Rails developer environment.

References:
---------------------------------------------------------------------
### Articles
- [Vagrant: Rails development environment][]

### Repositories
- [SpinUpLabs' Vagrant Dev Box][]

### Tools
- [Apache][]
- [Bundler][]
- [Capistrano][]
- [Chef][]
- [Cygwin][]
- [Git][]
- [MinGW][]
- [MySQL][]
- [Puppet][]
- [Vagrant][]
- [VirtualBox][]
- [VMFusion][]

### others
- [How to set up SSH (for the beginner)](http://inside.mines.edu/~gmurray/HowTo/sshNotes.html)

[Vagrant: Rails development environment]: http://www.spinuplabs.com/posts/vagrant-rails-development-environment

[SpinUpLabs' Vagrant Dev Box]: https://github.com/redsparklabs/spinuplabs-vagrant-dev-box

[Apache]:     http://www.apache.org/                 "Apache"
[Bundler]:    http://bundler.io/                     "Bundler"
[Capistrano]: http://www.capistranorb.com/           "Capistrano"
[Chef]:       http://www.opscode.com/chef/           "Chef"
[Cygwin]:     http://www.cygwin.com/                 "Cygwin"
[Git]:        http://git-scm.com/                    "Git"
[MinGW]:      http://www.mingw.org/                  "MinGW32"
[MySQL]:      http://www.mysql.com/                  "MySQL"
[Puppet]:     http://puppetlabs.com/                 "Puppet"
[Vagrant]:    http://www.vagrantup.com/              "Vagrant"
[VirtualBox]: https://www.virtualbox.org/            "VirtualBox"
[VMFusion]:   http://www.vmware.com/products/fusion/ "VMFusion"