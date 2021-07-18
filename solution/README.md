docker pull infracloudio/csvserver:latest
docker run -d infracloudio/csvserver:latest
docker ps -a
docker logs [container-id]
in container logs found /csvserver/inputdata no such file or directory
genereated the random nomber file in opt directory named inputFile. then set then set environment variable and start the container using below command.
echo CSVSERVER_BORDER=Orange > CSVSERVER_BORDER
docker run -d -p 9393:9300 -v /inputFile:/csvserver/inputdata --env-file CSVSERVER_BORDER docker.io/infracloudio/csvserver
docker run -d -p 9393:9300 -v /inputFile:/csvserver/inputdata --env-file CSVSERVER_BORDER docker.io/infracloudio/csvserver >> part-1-cmd




