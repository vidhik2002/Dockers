### Dockerizing a simple-nodejs-application


##### Steps
Build the image
```sh
docker build . -t <your username>/<name-of-node-application>
```
Incase of network timeout error
```sh
docker build . -t <your username>/<name-of-node-application> --network=host
```
To see the images listed by Dockers
```sh
docker images
```
Run the image
```sh
docker run \
    -it \
    --rm \
    -v ${PWD}:/app \
    -v /app/node_modules \
    -p 3001:3000 \
    -e CHOKIDAR_USEPOLLING=true \
    <your username>/<name-of-node-application>
```
Print app output 
```sh
 docker logs <container id>
```
To get container-id
```sh
docker ps
```
To call app using curl
```sh
curl -i localhost:49160
```
