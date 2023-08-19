## 도커 컴포즈 백그라운드 실행법
docker-compose up -d

## 디비 더미 데이터
```sql

CREATE TABLE person(
	id INT PRIMARY KEY,
	name VARCHAR(100)
);

INSERT INTO person(id, NAME) VALUES(1, 'ssar');

SELECT * FROM person;
```