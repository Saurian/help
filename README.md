# Help note

Information only

## Docker:

### Docker compose:

    docker-compose up --build
    docker stop $(docker ps -a -q)  // stop all containers

Docker provides a single command that will clean up any resources — images, containers, volumes, and networks — that are dangling (not associated with a container):

    docker system prune

To additionally remove any stopped containers and all unused images (not just dangling images), add the -a flag to the command:

    docker system prune -a


### Removing Docker Images

Remove one or more specific images

Use the docker images command with the -a flag to locate the ID of the images you want to remove. This will show you every image, including intermediate image layers. When you've located the images you want to delete, you can pass their ID or tag to docker rmi:

List:

    docker images -a

Remove:

    docker rmi Image Image

Run:

    docker exec -it container_name /bin/bash
   

## Chrome:

```
https://remotedesktop.google.com/access
```


## Git

#### project

prod    dev   git

    - ssh -i /home/pavel/.ssh/pavel.paulik_ssh.key pavel.paulik@vps-prod4.pixman.cz
    - ssh -i /home/pavel/.ssh/pavel.paulik_ssh.key pavel.paulik@vps-dev1.pixman.cz
    - ssh -i /home/pavel/.ssh/pavel.paulik_ssh.key pavel.paulik@vps-git1.pixman.cz


remove .git .gitignore

    find web/vendor -name '*.gitignore' -delete
    find web/vendor -name '*.git' -exec rm -rf {} \;

remove file form git

    git rm --cached -r folder-name
    git rm --cached file


## Composer

autoload

    composer dumpautoload -o
    composer dump

## Linux

skupina www-data

    sudo chown -R $USER:www-data /var/www/html/path...
    sudo chgrp -R www-data /var/www/html

        - sudo chmod -R 2775 /var/www/html 
        - sudo chmod -R 2755 /var/www/html


control center (chybějící), settings not found

    sudo apt install gnome-control-center
  
