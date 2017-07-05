# Oneliners 

Some small, random but possibly useful snippets for various tasks for oblivious shell users

## Miscellaneous

**Output unique lines of a text file**

    cat diff.txt | sed "s/^[ \t]*//" | sort | uniq
    
**Find content in file recursive**
    
    grep --include=*.sql -rnw . -e "pattern"
    
**Concat the content of all alphabetically orderd txt files**    
    
    find . -type f -name '*.txt' | sort | xargs cat 0 >> concat.txt
    
**Find all filenames recursive and print them sorted**

    find . -exec ls -dl \{\} \; | awk '{print $9}' | sort    
    
**Replace file content**

    sed -i -e 's/foo/bar/g' filename
    
**Find all entities not in persistence.xml**    

    egrep -lir --include=*.java "@Entity" . | awk -F"/" '{print $NF}' | awk -F"." '{print $1}' | while read -r file ; do     
        if ! grep -q "$file" src/main/resources/META-INF/persistence.xml ;
        then
        echo "Missing entity $file"
        fi
    done    

## System

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

