# MySQL 도커파일 생성방법

```docker
FROM mysql

ENV MYSQL_USER=ssar
ENV MYSQL_PASSWORD=ssar1234
ENV MYSQL_ROOT_PASSWORD=root1234
ENV MYSQL_DATABASE=ssardb

CMD [ "--character-set-server=utf8mb4", "--collation-server=utf8mb4_unicode_ci" ]  
```

## UTF 8 설정 확인
```sql
show variables like 'c%';
show variables like 'character_set_%';
```

## volumn 연결
- pwd로 volume 경로 확인
- 도커 볼륨 리스트 보기
```docker
docker volume ls
```

- docker 실행시 -v 옵션 추가(볼륨 옵션)
```docker
docker run -d -v D:/dockerwork/docker_lab/ex05/mysql-volumn:/var/lib/mysql -p 3308:3306 --name mysql-container mysql-image
```

- 이름이 있는 볼륨 사용법
```docker
docker run -d -v mysql-volumn:/var/lib/mysql -p 3308:3306 --name mysql-container mysql-image
```




