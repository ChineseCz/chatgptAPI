# devops

docker container cp Nginx:/etc/nginx/nginx.conf G:\JavaProject\chatgpt\nginx\conf
docker container cp Nginx:/etc/nginx/conf.d/default.conf G:\JavaProject\chatgpt\nginx\conf\conf.d\default.conf

docker container cp Nginx:/usr/share/nginx/html/index.html G:\JavaProject\chatgpt\nginx\html

docker run \
--restart always \
--name Nginx \
-v G:\JavaProject\chatgpt\nginx\html:/usr/share/nginx/html \
-v G:\JavaProject\chatgpt\nginx\conf\nginx.conf:/etc/nginx/nginx.conf \
-v G:\JavaProject\chatgpt\nginx\conf\conf.d:/etc/nginx/conf.d \
-p 80:80 \
--privileged=true 
-d