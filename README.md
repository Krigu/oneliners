# Onelinres 

Some small, random but possibly useful snippets for various tasks for oblivious shell users

## Docker 

**Remove all containers**
    docker rm $(docker ps -a -q)
    
**Remove all images**
    docker rmi $(docker images -q)

