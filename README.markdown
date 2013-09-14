How to setup Vagrant, Ruby on Rails and deploying with Capistrano
=======================================================================

The purpose of this repository to practice setting up a virtual 
environment through Vagrant, for developing a [Rails][] application 
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
software, like [MySQL][] for databases and [Apache][] for serving 
webpages or applications.

_*Note: Any premade Vagrant box will by default have Ruby installed, to 
allow provisioners like [Chef][] or [Puppet][] to run and install 
software._

For this Project I will be following SpinUpLabs' 
[Vagrant: Rails development environment][] article and using their 
[Vagrant file and Puppet manifest][SpinUpLabs' Vagrant Dev Box] to 
quickly start building an ideal Ruby on Rails developer environment.


### Step 2 - Alternative
Alternatively you could chose to configure your Vagrant install with 
something like SaltStack. _which is a great alternative if you find Chef 
and Puppet hard to configure or too slow_. 

SaltStack is Python based script that uses [YAML][] files for 
configuration manifests. To use it with Vagrant you will need to install 
[Salty Vagrant][] by running ```vagrant plugin install vagrant-salt``` 
after installing Vagrant.

Quickly searching the web found the 
["Red Tide Hobo Surfer" repositroy][Red Tide Hobo Surfer], which should 
install and setup a Rails environment using SaltStack.


Step 3
---------------------------------------------------------------------
Download and copy your chosen Vagrant file, with provision manifests, 
into the project's root folder.


Step 4
---------------------------------------------------------------------
Change to the project's root directory in Terminal (Linux or Mac OS X), 
Git bash or Command Prompt as Admin (Windows); 

e.g. ```cd ~/My\Documents/GitHu/setup_vagrant_rails_and_cap_deploy/```

Run the command ```vagrant up```

This will download the appropriate Vagrant box, a virtual machine built 
for use with Vagrant, and install the software listed in the manifests. 

_*Note: This will take some time and may fail from timing out when 
installing some packages. If that happens restart the virtual machine 
with ```vagrant reload```. This also useful for making changes take 
affect after updating the configure manifests._


Step 5
---------------------------------------------------------------------
After the installation has finished, login into the virtual machine with
```vagrant ssh```.

_*Note: SSH will NOT work in Windows' Command Prompt without additional 
tools like Cygwin. I would recommend downloading Git and using its Git 
bash_


Step 6a
---------------------------------------------------------------------
Once logged in run the command ```gem install bundler``` . 

[Bundler][] is a Ruby Gem for managing Gems and their dependencies, 
ensuring that they will all work with another despite version differences.


Step 6b
---------------------------------------------------------------------
Install Ruby on Rails

```gem install rails```

_*Note: If installing any Gems is taking an unsually long time, 
```Ctrl+c``` to cancel out and try again or add ```-V``` (case-sensitive) 
or ```--verbose``` to get the full output what it is doing whilst it 
installs._


Step 7
---------------------------------------------------------------------
Generate a new Rails Application; e.g.

```rails new blog```


Step 8 
---------------------------------------------------------------------
Change into the new project directory; e.g.

```cd /vagrant/blog/```

Create the database

```rake db:create```

And start the server

```rails server```


References:
---------------------------------------------------------------------
### Articles
- [Vagrant: Rails development environment][]
- [Creating the Blog Application][]

### Repositories
- [Railsmn Dev Box][]
- [Red Tide Hobo Surfer][]
- [Salty Vagrant][]
- [SpinUpLabs' Vagrant Dev Box][]

### Software/Tools
- [Apache][]
- [Bundler][]
- [Capistrano][]
- [Chef][]
- [Cygwin][]
- [Git][]
- [MinGW][]
- [MySQL][]
- [Puppet][]
- [Rails][]
- [Vagrant][]
- [VirtualBox][]
- [VMFusion][]
- [YAML][]

### others
- [How to set up SSH (for the beginner)](http://inside.mines.edu/~gmurray/HowTo/sshNotes.html)
- [Solving 'stdin: is not a tty' error](http://tech.karbassi.com/2011/11/09/stdin-is-not-a-tty/)


[Vagrant: Rails development environment]: http://www.spinuplabs.com/posts/vagrant-rails-development-environment
[Creating the Blog Application]: http://guides.rubyonrails.org/getting_started.html#creating-the-blog-application

[Railsmn Dev Box]: https://github.com/railsmn/railsmn-dev-box
[Red Tide Hobo Surfer]: https://github.com/geopet/red-tide-hobo-surfer
[Salty Vagrant]: https://github.com/saltstack/salty-vagrant
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
[Rails]:      http://rubyonrails.org/                "Ruby on Rails"
[Vagrant]:    http://www.vagrantup.com/              "Vagrant"
[VirtualBox]: https://www.virtualbox.org/            "VirtualBox"
[VMFusion]:   http://www.vmware.com/products/fusion/ "VMFusion"
[YAML]:       http://yaml.org/                       "YAML"