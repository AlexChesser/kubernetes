#Steps for getting started on a windows machine

Useful links:  
* Getting started <a href="locally.md">locally</a> guide
* Docker <a href="https://www.docker.com/docker-toolbox">toolbox</a>
* <a href="https://www.virtualbox.org/wiki/Downloads">VirtualBox</a>

##Pre-prequisites:

1. Install the <a href="https://www.docker.com/docker-toolbox">Docker toolbox</a>
2. Ensure that you have a copy of <a href="https://www.virtualbox.org/wiki/Downloads">VirtualBox</a> (docker toolbox might not install this automatically)
3. Open `Docker Quickstart Terminal` - this will auto configure your default Docker VM
4. Open PowerShell (`PS`) - it's just nicer than docker terminal, but docker terminal probably still works
5. In PS verify your docker machine is working `docker-machine ls`  
      `NAME      ACTIVE   DRIVER       STATE     URL                         SWARM`  
      `default   *        virtualbox   Running   tcp://192.168.99.100:2376`  

6. Run `docker-machine ssh default` 
7. Verify docker machine config by running `cat /proc/config.gz | gunzip | grep _MEMCG`  
   You should see:
      `CONFIG_MEMCG=y`  
      `CONFIG_MEMCG_SWAP=y`  
      `CONFIG_MEMCG_SWAP_ENABLED=y`  
      `CONFIG_MEMCG_KMEM=y`  
8. Verify docker machine config by running `cat /proc/config.gz | gunzip | grep _RESOURCE`  
      `CONFIG_RESOURCE_COUNTERS=y`  
    Note that this will likely NOT be there. This has been removed by Docker https://github.com/docker/docker/pull/13546
    I don't know what to do about this.
9. 


 
