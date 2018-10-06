# springboot-docker
#### Linux ทั่วไป

- ดูทั้งหมด
> -a
- ดู permission
> -l

#### Docker command ที่ใช้บ่อย

ลบ ทุก images
>docker rmi $(docker images -q)

บังคับลบทุก images 
> docker rmi -f $(docker images -a -q)


ดูว่ามี contrainer ตัวไหนทำงานบ้าง
>docker ps 

ดู container ทั้งที่ทำงาน แล้วก็ หยุดทำงาน
>docker ps -a

remove ทุก container
>docker stop $(docker ps -a -q)
>docker rm $(docker ps -a -q)

run image mysql
>docker run --name "ชื่อ container" -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=test -e MYSQL_USER="กำหนดชื่อ" -e MYSQL_PASSWORD="กำหนด password" -d mysql:5.6
