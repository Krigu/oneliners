# Oneliners 

Some small, random but possibly useful snippets for various tasks for oblivious shell users

## Miscellaneous

**Find process that is using a particular port**

    sudo netstat -lpn | grep :8080

## Docker 

**Remove all containers**

    docker rm $(docker ps -a -q)
    
**Remove all images**

    docker rmi $(docker images -q)

