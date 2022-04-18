# Redis

Для начала поставим redis через docker и запустим redis-insight.

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic1.png?raw=true)

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic2.png?raw=true)

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic3.png?raw=true)

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic4.png?raw=true)

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic5.png?raw=true)

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic6.png?raw=true)

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic7.png?raw=true)

С помощью python сгенерируем данные и загрузим в redis.

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic10.png?raw=true)

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic8.png?raw=true)

Измерим время вставки данных, 40 Мб данных вставилось за 3.928 сек.

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic9.png?raw=true)

Измерим время получения элемента (ключ в конце) -- 23 мс 

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic11.png?raw=true)

Измерим время получения элемента (ключ в середине) -- 16 мс

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic12.png?raw=true)

Измерим время получения элемента (ключ в начале) -- 13 мс

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic13.png?raw=true)

Далее создал конфигурационные файлы для каждого узла, отличие каждого заключается только в номере порта.

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/conf.png?raw=true)

Далее запускаем образы наших будущих нод через докер.

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic14.png?raw=true)

И мы видим, что STATUS EXITED(1), что означает, что образы не запущены, значит где-то произошла ошибка, я не пойму где.

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic15.png?raw=true)

Далее попытки запустить cluster create тщетны.

![alt text](https://github.com/AkshaevNikita/Redis/blob/main/pic16.png?raw=true)
