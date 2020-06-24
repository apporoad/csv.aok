# csv.aok
csv ext plugin for aok, awesome

## just do it

```bash
npm i -g aok.js

mkdir test
cd test

npm i csv.aok

touch test.csv

aok . -x


## post
curl -H "Content-Type: application/json" -X POST -d "{\"name\":\"LiSA\",\"age\":32}" http://localhost:11540/test 
curl -H "Content-Type: application/json" -X POST -d "{\"name\":\"aoer\",\"age\":30}" http://localhost:11540/test 
curl -H "Content-Type: application/json" -X POST -d "{\"name\":\"luna\",\"age\":28}" http://localhost:11540/test 
curl -H "Content-Type: application/json" -X POST -d "{\"name\":\"lily\",\"age\":7}" http://localhost:11540/test 

## get
curl http://localhost:11540/test 

curl http://localhost:11540/test?name=LiSA
curl http://localhost:11540/test?name=/l.*/ 

curl "http://localhost:11540/test?page=1&pageSize=2"
curl http://localhost:11540/test?order=age%20asc

## put
curl -H "Content-Type: application/json" -X PUT -d "{\"remark\":\"update\"}" http://localhost:11540/test?index=2 

## delete

curl -H "Content-Type: application/json" -X DELETE  http://localhost:11540/test?index=2 

curl -H "Content-Type: application/json" -X DELETE  http://localhost:11540/test

```

## ps
dson support in the future