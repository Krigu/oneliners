# Oneliners 

Some small, random but possibly useful snippets for various tasks for oblivious shell users

## Miscellaneous

**Output unique lines of a text file**

    cat diff.txt | sed "s/^[ \t]*//" | sort | uniq

**Find process that is using a particular port**

    sudo netstat -lpn | grep :8080
    
**Scan wifi channels**

    sudo iwlist wlan0 scan | grep \(Channel

**List of packages installed locally**

    dpkg -l
    
**List files from package(s).**
    
    dpkg -L <packagename>

**Restart Pulse Audio**
    
    pulseaudio -k && sudo alsa force-reload

## Docker 

**Remove all containers**

    docker rm $(docker ps -a -q)
    
**Remove all images**

    docker rmi $(docker images -q)

