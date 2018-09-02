### Start project
Simple run 
```
cd flask-angular-docker-dev
docker-compose build
docker-compose up
```
### Add some environments 
find in docker-compose.yml file this block, and edit it
![edit environments](https://image.prntscr.com/image/4c1070002ded469bb8a5953ea31fb172.png)

### Edit code
Code in folders `clients`(angular) and `server`(flask) you can edit, and the code will be immediately updated in the container. You do not need to restart the container! 

### Project url`s
(flask app proxy with nginx)
```
127.0.0.1 - flask app
127.0.0.1:4200 - angular
0.0.0.0:5432 - db
```

### Database
When you restart the container, your data will not pass from the database. 

### System packages
If you need to add the system packages to the image, add them in Dockerfile of each project (`./client/Dockerfile` or `./server/Dockerfile`)
example:
![add system packages](https://image.prntscr.com/image/27cf3d33d3a64c65ba6f1f5e4b5cd678.png)

### Nginx config
you can change file `./nginx.conf` and run:
```
docker-compose down
docker-compose build
docker-compose up
```

