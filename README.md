## Домашнее задание к занятию 2 «`Кластеризация и балансировка нагрузки`» - `Игонин В.А.`

# Задание 1
  1. Запустите два simple python сервера на своей виртуальной машине на разных портах
  2. Установите и настройте HAProxy, воспользуйтесь материалами к лекции по ссылке
  3. Настройте балансировку Round-robin на 4 уровне.
  4. На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.

# Решение 1
<details> 

![alt text](https://github.com/Sayward-k8/sflt-hw-02/blob/main/img/1.png)
![alt text](https://github.com/Sayward-k8/sflt-hw-02/blob/main/img/1.2.png)

[haproxy.cfg](https://github.com/Sayward-k8/sflt-hw-02/blob/main/1/haproxy.conf)

</details>  

# Задание 2

  1. Запустите три simple python сервера на своей виртуальной машине на разных портах
  2. Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
  3. HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
  4. На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

# Решение 2
<details> 

![alt text](https://github.com/Sayward-k8/sflt-hw-02/blob/main/img/2.png)
![alt text](https://github.com/Sayward-k8/sflt-hw-02/blob/main/img/2.2.png)
Запросы не по порядку, но имеют необходимые веса

[haproxy.cfg](https://github.com/Sayward-k8/sflt-hw-02/blob/main/2/haproxy.conf)

  
</details>  

# Задание 4

  1. Запустите 4 simple python сервера на разных портах.
  2. Первые два сервера будут выдавать страницу index.html вашего сайта example1.local (в файле index.html напишите example1.local)
  3. Вторые два сервера будут выдавать страницу index.html вашего сайта example2.local (в файле index.html напишите example2.local)
  4. Настройте два бэкенда HAProxy
  5. Настройте фронтенд HAProxy так, чтобы в зависимости от запрашиваемого сайта example1.local или example2.local запросы перенаправлялись на разные бэкенды HAProxy
  6. На проверку направьте конфигурационный файл HAProxy, скриншоты, демонстрирующие запросы к разным фронтендам и ответам от разных бэкендов.

# Решение 4
<details> 
  
![alt text](https://github.com/Sayward-k8/sflt-hw-02/blob/main/img/4.png)
![alt text](https://github.com/Sayward-k8/sflt-hw-02/blob/main/img/4.1.png)

[haproxy.cfg](https://github.com/Sayward-k8/sflt-hw-02/blob/main/4/haproxy.conf)

</details>
