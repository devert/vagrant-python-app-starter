Vagrant Python App Starter
==========================

A Python project starter, utilizing a Vagrant VM (default: Ubuntu 12.04 Precise Pangolin 32-bit) provisioned with Chef Solo.

Cookbooks included:

* [build-essential](https://github.com/opscode-cookbooks/build-essential)
* [python](https://github.com/opscode-cookbooks/python)
* [yum](https://github.com/opscode-cookbooks/yum)
* [vim](https://github.com/opscode-cookbooks/vim)

## Dependencies

* [VirtualBox](https://www.virtualbox.org/)
* [Ruby](http://www.ruby-lang.org/en/)
* [Vagrant](http://vagrantup.com/)
* [Vagrant Librarian-Chef](https://github.com/jimmycuadra/vagrant-librarian-chef)

## Usage

Clone it into your project folder.

```bash
$ git clone https://github.com/devert/vagrant-python-app-starter [proj-name]
$ rm -rf .git
```

Open the vagrant/Vagrantfile and modify *proj-name* instances to the name of your project. Modify the Python version you would like installed in the *chef.json* attributes. See chef cookbook [python](https://github.com/opscode-cookbooks/python) documentation for more details on python configuration.

```bash
$ vagrant plugin install vagrant-librarian-chef
$ cd vagrant
$ vagrant up
$ vagrant ssh
$ cd proj-name
$ python -m SimpleHTTPServer 3000
```

After running the above commands you should be able to browse to http://locahost:3000/ and see "Hello World!" on your host machine. Changes to files via the host machine will immediately be updated on the guest VM as well. 

Now get in there and build something awesometronic with Python!

## Optional (But Pretty Great)

#### Vagrant
* Keep Vagrant VM's VirtualBox Guest Additions up to date with [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest) plugin. Install this on the host machine.

    ```bash		
    $ vagrant plugin install vagrant-vbguest
    ```

