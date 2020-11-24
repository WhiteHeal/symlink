create symlink

    cd docker
    ln -s ../somefile index.html

docker build, change context and run 

    docker build -t test -f ../docker/Dockerfile  ../ 
    docker run -it --rm -d -p 8080:80 --name web test


How to check?
curl 127.0.0.1:8080 from your PC than change content in original file and curl 127.0.0.1:8080 again

    docker exec -it web bash
    ls -al /home/docker
    echo 1 > /home/somefile
    
clean up

    docker rm -f web
    docker rmi test