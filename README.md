# springboot-docker
#### Linux ทั่วไป

ดูทั้งหมด
> -a 
ดู permission
> -l
force
> -f

#### Docker command ที่ใช้บ่อย

ลบ ทุก images
>docker rmi $(docker images -q)

ดูว่ามี contrainer ตัวไหนทำงานบ้าง
>docker container ps 

ดู container ทั้งที่ทำงาน แล้วก็ หยุดทำงาน
>docker container ps -a

remove ทุก container
>docker stop $(docker ps -a -q)
>docker rm $(docker ps -a -q)

ดูรายละเอียด container
>docker inspect "ชื่อหรือไอดีคอนเทรนเนอร์"

run image mysql
>docker run --name "ชื่อ container" -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=test -e MYSQL_USER="กำหนดชื่อ" -e MYSQL_PASSWORD="กำหนด password" -d mysql:5.6

เข้าถึง container mysql
>docker exec -it "ชื่อ container" bash

build project spring boot
>docker build -f Dockerfile -t "ชื่อโปรเจค" .

run container spring boot
>docker run -p port:port "ชื่อโปรเจค"

run real logs
>docker logs -f  "containerId"

# docker-compose

ในการ config คำสั่ง docker-compose 
- จะไม่สามารถใช้คำสั่ง tab ในการเขียนไฟล์ .yml ได้จะเกิด error '\t' 
- ในการระบุชื่อ หรือคำสั่งต่างๆหลังจาก ':' ต้องมีการเว้นวรรคเสมอ



