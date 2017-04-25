# puphpet-vagrant-magento2

## Prerequisites:
You must have [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads) and [Vagrant](https://www.vagrantup.com/downloads.html) installed to run the `Vagrantfile`
## Installing puphpet-vagrant-magento2:
Create a directory for your project. This example will use "newsite" as the project directory.

**bash.sh**

```
  mkdir newsite
  cd newsite
  git clone git@bitbucket.org:irishtitan/puphpet-vagrant-magento2.git
  vagrant up # this will take a while, get a tasty beverage.
```

Once the ```vagrant up``` command completes, you should see some green text saying 'Success', or if you get red text, look back through the output and resolve any problems. If the build was successful, ssh into the vagrant environment then follow the steps in ```./repo/html/README.md``` to download and install Magento2 using composer:

```
vagrant ssh

[vagrant@magento2] $ cd /var/www/html/magento2 && less README.md.
```