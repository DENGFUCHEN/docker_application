docker push dengfu24 / unbuntu：tagname
自定義image操作
	docker login 指令登入到 Docker Hub
	1.上傳
		要把 Docker Image Push 到 Docker Hub 上，需要把 Docker Image 加上 tag，如下指令
		docker tag mytomcat jackyohhub/mytomcat 
		使用 docker push 指令把 Docker Image Push 到 Docker Hub 裡，指令如下
		docker push jackyohhub/mytomcat
	2.下載
		從 Docker Hub Pull Docker Image 下來，指令如下
	docker pull jackyohhub/mytomcat
查詢官方image
	docker search
下載官方image
	docker pull nginx
列出所有image
docker image ls     docker images jackyohhub/mytomcat
執行image並進入容器
docker run -t -i ubuntu:14.04 /bin/bash
docker run -t -i ouruser/sinatra:v2 /bin/bash
刪除一個image
docker rmi training/sinatra
將容器啟動
docker start
重新啟動容器
docker restart
終止一個執行中的容器
docker stop
刪除一個處於終止狀態的容器
docker rm  trusting_newton
查看容器訊息
docker ps  docker ps -a

docker commit -m "Added json gem" -a "Docker Newbee" 0b2616b0e5a8 ouruser/sinatra:v2
docker images
docker run -t -i ouruser/sinatra:v2 /bin/bash
mkdir sinatra
cd sinatra
touch Dockerfile
docker build -t="ouruser/sinatra:v2" .
docker tag 5db5f8471261 ouruser/sinatra:devel
docker run ubuntu:14.04 /bin/echo 'Hello world'執行不進入docker
docker run -d ubuntu:14.04 /bin/sh -c "while true; do echo hello world; sleep 1; done"後台執行
