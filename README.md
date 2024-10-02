### Задание №1. Анализ HTTP-запросов

1. Неверный запрос
    - Какой метод HTTP был использован для отправки запроса? Ответ: POST
    - Какие заголовки были отправлены в запросе?
      ```
      Accept: */*
      Accept-Encoding: gzip, deflate
      Accept-Language: ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7,ro;q=0.6,ca;q=0.5,co;q=0.4,mt;q=0.3,ja;q=0.2,uk;q=0.1
      Connection: keep-alive
      Content-Length: 35
      Content-Type: application/x-www-form-urlencoded; charset=UTF-8
      Host: sandbox.usm.md
      Origin: http://sandbox.usm.md
      Referer: http://sandbox.usm.md/login/
      User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/129.0.0.0 Safari/537.36
      X-Requested-With: XMLHttpRequest
      ```
    - Какие параметры были отправлены в запросе? Ответ: ```username=admin123&password=password```
    - Какой код состояния был возвращен сервером? Ответ: 401
    - Какие заголовки были отправлены в ответе?
      ```
      Server: nginx/1.24.0 (Ubuntu)
      Date: Wed, 02 Oct 2024 19:25:05 GMT
      Content-Type: text/plain;charset=UTF-8
      Transfer-Encoding: chunked
      Connection: keep-alive
      ```
2. Верный запрос
   - Какой метод HTTP был использован для отправки запроса? Ответ: POST
   - Какие заголовки были отправлены в запросе?
      ```
     Accept: */*
     Accept-Encoding: gzip, deflate
     Accept-Language: ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7,ro;q=0.6,ca;q=0.5,co;q=0.4,mt;q=0.3,ja;q=0.2,uk;q=0.1
     Connection: keep-alive
     Content-Length: 32
     Content-Type: application/x-www-form-urlencoded; charset=UTF-8
     Host: sandbox.usm.md
     Origin: http://sandbox.usm.md
     Referer: http://sandbox.usm.md/login/
     User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/129.0.0.0 Safari/537.36
     X-Requested-With: XMLHttpRequest
     ```
   - Какие параметры были отправлены в запросе? Ответ: ```username=admin&password=password```
   - Какой код состояния был возвращен сервером? Ответ: 200
   - Какие заголовки были отправлены в ответе?
     ```
      Server: nginx/1.24.0 (Ubuntu)
      Date: Wed, 02 Oct 2024 19:32:25 GMT
      Content-Type: text/plain;charset=UTF-8
      Transfer-Encoding: chunked
      Connection: keep-alive
     ```

### Задание №2. Составление HTTP-запросов

1. Составьте `GET`-запрос к серверу по адресу `http://sandbox.com`, указав в заголовке `User-Agent` ваше имя и фамилию.
   ```
   GET / HTTP/1.1
   Host: sandbox.com
   User-Agent: Sveatoslav Covas
   ```
2. Составьте `POST`-запрос к серверу по адресу `http://sandbox.com/cars`, указав в теле запроса следующие параметры:
    - `make: Toyota`
    - `model: Corolla`
    - `year: 2020`
   ```
   POST /cars HTTP/1.1
   Host: sandbox.com
   User-Agent: Sveatoslav Covas
   Content-Type: application/json
   model=Corolla&make=Toyota&year=2020
   ```
3. Составьте `PUT`-запрос к серверу по адресу `http://sandbox.com/cars/1`, указав в заголовке `User-Agent` ваше имя и фамилию, в заголовке `Content-Type` значение `application/json` и в теле запроса следующие параметры:
   ```json
   {
     "make": "Toyota",
     "model": "Corolla",
     "year": 2021
   }
   ```
   ```
   PUT /cars/1 HTTP/1.1
   Host: sandbox.com
   User-Agent: Sveatoslav Covas
   Content-Type: application/json
   {
     "make": "Toyota",
     "model": "Corolla",
     "year": 2021
   }
   ```
4. Напишите один из возможных вариантов ответа сервера следующий запрос.
   ```http
   POST /cars HTTP/1.1
   Host: sandbox.com
   Content-Type: application/json
   User-Agent: John Doe
   model=Corolla&make=Toyota&year=2020
   ```
   Ответ:
   HTTP/1.1 201 Created
   Предположите ситуации, когда сервер может вернуть HTTP-коды состояния 200, 201, 400, 401, 403, 404, 500.
   Ответ: 
   200 - в ответ на правильный GET запрос
   201 - в ответ на правильный POST, PUT, DELETE запрос
   400 - в ответ на неправильно составленный запрос
   401 - в случае если пользователь не аутентифицирован на сервере
   403 - в случае если пользователь не обладает правами на выполнение запроса
   404 - в случае если не найден запрашиваемый ресурс
   500 - в случае если запрос не смог быть обработан на сервере
### Задание №3. Дополнительное задание. HTTP_Quest
1. Congratulations, Sveatoslav Covas! You have successfully completed the quest! Here is your secret: OjoKFxEmEAktF1Q3ClcIP0JEVg==
2. secret: OjoKFxEmEAktF1Q3ClcIP0JEVg==
