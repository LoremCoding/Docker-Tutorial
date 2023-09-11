```yml
docker pull <img_name> : this will download the <img_name> from dockerhub to my local machine .

docker images : this will get display list of all downloaded images on my local machine . 

docker ps : command shows you all containers that are currently running.

docker ps -a : will list all conatiners and thier state Exited or up and the history of conatiners used also thier commands . 

docker run -it <img_name> sh : this will run the container in interactive mode .

docker run -d ...  : will run print the id of the conatiner then run it in the background ( deteched mode )

docker run -w <working dir> -it <img_name> sh : this example of starting conatiner where the working dir is <working dir>

docker run ... --name <new_name_for_container>  ... : this will make the container run with name <new_name_for_container>  , usefull when to make distiguache the conatiner running ... see docker ps under name colone .

docker ps -q -a  : (-q =  Only display container IDs) (-a = all conatiners cause (default shows just running))

docker ps -q  : will show the ids of runing conatiners ids . 

docker run ... --env VAR0=VALUE --env VAR1=VALUE  .... : Set environment variables

docker run ...  --env-file <file0.sh> --env-file <file1.sh> .... : Read in a file of environment variables

docker run --rm ... : this will delete the image after Exited , and it will not be appeared in docker images .

docker run .... --entrypoint "command to run "  ... : overide entry point of image , is usefull to run command inside conatiners then exit <ith out runing the main entry point .

docker stop $(docker ps -q) : thsi command will shut down all ruining conatiners . 

docker save <img_id> -o <output_file.tar> : this will save the image into file 

docker load -i <path_to_image_file> : this will loat the image on docker images list 

docker rmi $(docker images -aq ) : will remve all installed docker images .

docker rmi -f  $(docker images -aq) : this will force every image to be deleted even loaded and current ruining . 

docker stop  $(docker ps -aq) : this will stop all runing containers .

docker exec -w <working dir> <container_id> <command> : execute command in runing container with in path 

docker exec -d -w <working dir> <container_id> <command> : execute command in runing container with in path as deteached mode . 

docker build -t <image_name>:<version> .  && docker run -it  --name <conatiner_name> <image_name>:<version> sh  : this will build an image then start conatiner with named name 

docker cp mycontainer:/app/myfile.txt /my/local/path/ : copy local file to container 

docker cp /my/local/file.txt mycontainer:/app/ : copy file from container to local 

docker run -it <imm>:<tag>  bash : will start container of image in bash mode 

docker kill $(docker ps -aq) && docker rmi -f  $(docker images -aq) : will clean the local machine from any thing 


```
