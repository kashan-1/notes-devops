## This file contains the commands on how to upload the images to docker hub

1. To commit the image
``` bash
docker commit image_ID
```

2. second step is to tag the locally build image 
order: `image_ID -> username/repository_name:build_name`
``` bash
docker tag f03e4a2e7119 kashan1/k-owncloud:v1
```
3. login to `docker hub` and provide credentails (SSH or login with user)

``` bash
docker login
```

4. Push an image to docker hub
order: `username/repository_name:build_name`

``` bash
docker push kashan1/k-owncloud:v1
```

Run the previously pushed docker image

``` bash
docker run -p 80:80 kashan1/k-owncloud:v1
```

