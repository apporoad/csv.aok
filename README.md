# csv.aok
csv ext plugin for aok, awesome

## just do it

```bash

## 1. install aok , it is server plugin
npm i -g aok.js

# 2. make your dir ,here is test
mkdir test
cd test

# 3. install csv.aok now
npm i csv.aok

# 4. use your csv , here is to make an empty csv
touch test.csv

# 5. now run server
aok . -x

# 6. then we can edit data to your csv by webapi 

## add data to csv  : test.csv , post
curl -H "Content-Type: application/json" -X POST -d "{\"name\":\"LiSA\",\"age\":32}" http://localhost:11540/test 
curl -H "Content-Type: application/json" -X POST -d "{\"name\":\"aoer\",\"age\":30}" http://localhost:11540/test 
curl -H "Content-Type: application/json" -X POST -d "{\"name\":\"luna\",\"age\":28}" http://localhost:11540/test 
curl -H "Content-Type: application/json" -X POST -d "{\"name\":\"lily\",\"age\":7}" http://localhost:11540/test 

##  search for data , get
curl http://localhost:11540/test 

## you can filter data like nam = ...
curl http://localhost:11540/test?name=LiSA

## you can alse use regex
curl http://localhost:11540/test?name=/l.*/ 

## page and pageSize
curl "http://localhost:11540/test?page=1&pageSize=2"

## order data
curl http://localhost:11540/test?order=age%20asc

# default page =0  pageSize =10  limit is null
curl http://localhost:11540/test?name=/1.*/&limit=1

## modify your csv data , put
curl -H "Content-Type: application/json" -X PUT -d "{\"remark\":\"update\"}" http://localhost:11540/test?index=2 

curl -X PUT -d "remark=update" http://localhost:11540/test?index=2 

## delete your csv data 
curl -H "Content-Type: application/json" -X DELETE  http://localhost:11540/test?index=2 

curl -H "Content-Type: application/json" -X DELETE  http://localhost:11540/test

```

## ps
dson support in the future
