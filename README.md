# MTRPZ_Lab_3_ex_3

Docker version: 20.10.23

Це третє завдання з лабораторної роботи № 3, тут я створив найпростіший сервер за допомогою бібліотеки express.js
Додав докер-файл де загрузив останню версію ноди


```
FROM node
```
Також зробив робочу директорію, скопіював проект та встановив залежності
```
WORKDIR /app

COPY . .

RUN npm install
```
І нарешті прописав запуск та порт на якому буде працювати мій застосунок
```
EXPOSE 3000

CMD ["node","index.js"]
```
 Сама команда запуску
```
// Збір образу
docker build .
// Збір і запуск контейнера
docker run -p 80:3000 <your image id>
```
