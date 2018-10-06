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
