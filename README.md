# Getting Started

### Reference Documentation
mvn clean install
docker build -t titusvijay1/docker-demo-1
docker push titusvijay1/docker-demo-1
docker run -p 8080:8080 -dt titusvijay1/docker-demo-1 /bin/bash

c:\Projects\docker-demo>docker image ls
REPOSITORY                  TAG       IMAGE ID       CREATED          SIZE
titusvijay1/docker-demo-1   latest    747706ab6dd9   12 seconds ago   501MB

c:\Projects\docker-demo>docker container ls
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

c:\Projects\docker-demo>docker run -p 8080:8080 -dt 747706ab6dd9 /bin/bash
7368b0be25a68dd0ed13fef5e01eabc855aca4944becc8df14fe9d9fb1329917

c:\Projects\docker-demo>docker container ls
CONTAINER ID   IMAGE          COMMAND                  CREATED         STATUS         PORTS                    NAMES
7368b0be25a6   747706ab6dd9   "java -jar playjava.…"   9 seconds ago   Up 8 seconds   0.0.0.0:8080->8080/tcp   elegant_shirley

Run another instance of the container
c:\Projects\docker-demo>docker run -p 8081:8080 -dt 747706ab6dd9 /bin/bash
1e4b5ff1498c20170699b1f79d37989a904ea91e6aef19a3e470288608bfaf02

c:\Projects\docker-demo>docker container ls
CONTAINER ID   IMAGE          COMMAND                  CREATED         STATUS         PORTS                    NAMES
1e4b5ff1498c   747706ab6dd9   "java -jar playjava.…"   6 seconds ago   Up 5 seconds   0.0.0.0:8081->8080/tcp   unruffled_swartz
7368b0be25a6   747706ab6dd9   "java -jar playjava.…"   2 minutes ago   Up 2 minutes   0.0.0.0:8080->8080/tcp   elegant_shirley