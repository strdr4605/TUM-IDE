# Integrated Development Environments Laboratory Work #1
## Setting server environment. Version Control Systems

For this laboratory as a remote server I will use DigitalOcean.com service. You can find more information about this hosting service on their site [DigitalOcean](https://www.digitalocean.com/). If you want to use first 10$ for free you can register using this [link](https://m.do.co/c/9fd3b727487a). You can see a tutorial about how to create host on their site.

## Connect via ssh
In your profile you can create an SSH key that you will use while connecting to host.  
After droplet was created you will see hosts **IP address**:

![Alt](images/ip_address.png)

- Lets first of all check if we can see the machine. Ping it using ``` ping -c 4 138.68.72.152``` You should get something like this:

![Alt](images/ping.png)

- Now we can easily connect with ssh to our remote server. In linux distributors we type in ```ssh  root@138.68.72.152```. You have to enter passphrase for your ssh key.

![Alt](images/connect_server.png)

- Next we will install fish shell, a smart and user-friendly command line shell for macOS, Linux, and the rest of the family. More information [here](https://fishshell.com/).  
For installing fish we have to run following commands:
  * `sudo apt-add-repository ppa:fish-shell/release-2`
  * `sudo apt-get update`
  * `sudo apt-get install fish`
  * `fish` (to switch to fish shell)
  * `curl -L https://get.oh-my.fish | fish` (to install oh-my-fish. Check it [here](https://github.com/oh-my-fish/oh-my-fish))
  * `omf install simple-ass-prompt` (to install a simple theme)  
Shell should look like:

![Alt](images/fish_shell.png)

- Now we can perform any command from our terminal!

## Set up git

- First of all we have to install git `sudo apt-get install git`
- Configure global user	name `git config --global user.name "str.dr4605"`
- Configure global user	email `git config --global user.email "str.dr4605@gmail.com"`
- Initialize git repo `git init`
- Generate ssh key with `ssh-keygen`
- Set the public key in github
- Now we will add remote to our host `git remote add origin https://github.com/strdr4605/TUM-IDE-labs.git`
- Pull from remote repo to local `git pull origin master`
- Now can work further on this project
