#### Concepts:

1. Explain continuous integration. How is it used on a project?
Continuous Integration (CI) makes the life of a developer easier. With CI, the developers can automatically build, test and analyze a software change for every commit that was done to the repository. 
It can be used on a project where every developer can commit their changes for a code update or a code that is new in itslef. With CI in it, with every commit the whole project would be tested and would check if it breaks anywhere, if broken anywhere it would accordingly prompt. 
One famous combination of it is Github + Jenkins. With every Git hub push by a project memeber, the jenkins hook would be called and the testing would be done. The status report of every commit can be seen on Jenkins Server.

2. Why should developers use configuration management tools to manage their software programs? What can go wrong if they don't?
When an application has t be run on a server, there are several dependenicies involved with it. For example it should have Pyhton installed and that too of the latest version or it needs to clone a certain repo where the code exists for the application. Managing it all manually is possible but not very time friendly. Also when the number of servers would increase (typically in an environment like data centers where there would be a lot of servers and every server has to e configured), it would become difficult to keep a track of the task. And the real pain would be when one of the utilities has to be upgraded. GOing through all the servers all over again is a nightmare for the person assigned the task. There comes a hero of Configuration Management. Where the developer just has to create a simple formatted file (yaml for ansible) with key and value pairs of all the config it needs on the servers and then just run it. The playbook would do it all. There are many Configuration tools like Ansible, Puppet, CHef, Salt are  pretty famous these days.
If the developer doesn't use Configuration Management, the developer might do a goof up with the dependencies since it would be difficult to keep a track of all of it. Also if a certain part of code got updated and it needs a higher version of the dependency, it would again have to do it manually (maybe even uninstall and install it). It's better to use Configuration management since it reduces the human error part by a good amount.


#### Running Ansible and Playbook:
The Ansible version used is 2.5.1
1. The ansible playbook does configuration management on a VM from local host. 
   - The VM is made using vagrant.
   - 'Vagrantfile' is present in the repository. Create a VM using that vagrant file.
   - Run the ansible playbook from local host.
   
2. Run the playbook as a root user or run it by appending sudo to the command:
   - If root user: ansible-playbook -i inventory hw4.yml
   - If non-root user: sudo ansible-playbook -i inventory hw4.yml
   
#### Link to Screencast:
https://drive.google.com/file/d/1QJWOUKKvqy1ln61GVAD-JfDA8KKpEVlr/view?usp=sharing
