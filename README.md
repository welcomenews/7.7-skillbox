#### 7.7-skillbox

#### Скачать deb пакеты
https://www.elastic.co/downloads/past-releases/

#### Скачать deb пакет Graylog
https://packages.graylog2.org/debian/pool/stable/4.3/g

---------------------------------------------------------

#### С Graylog работает elasticsearch 7.11 и Filebeat 6.5

#### Для работы Graylog нужно устновить джаву
$ sudo apt install openjdk-8-jre-headless -y

#### filebeat[12825]: Exiting: registry file version 1 not supported
Если при запуске filebeat вылетает эта ошибка, то нужно остановить filebeat и запустить команду sudo rm -rf /var/lib/filebeat/

--------------------------------------------

#### Что нужно сделать
1. Разверните у себя стек ELK или Graylog.
2. Придумайте минимум три таргета для сбора логов (чем больше, тем лучше для вас, это может быть тот же Rsyslog и nginx.log). Произвольно выберите два таргет-файла, один таргет найдите сами, но такой, который можете инициировать руками — как в видео логин-логаут из-под рута, но он уже был, поэтому не принимается)
3. Заведите таргеты в ELK или Graylog.
4. Прикрутите alerts или выполнение кастомных скриптов при срабатывании какого-либо события. Каналы уведомлений можно не настраивать, достаточно сконфигурированного и отработавшего алерта или ивента.
5. Инициируйте таргет и зафиксируйте его скриншотом, алертом или ивентом.

#### Рекомендации
- Если вы не знаете, что можете трекать, напишите утилиту на Bash или Python, которая будет в фоне писать что-то наподобие lorem ipsum в вымышленный лог-файл.
- Под таргетом во втором случае подразумевается сообщение о каком-то событии в лог-файле. Подумайте, что у вас происходит в системе и как вы можете на это влиять.

--------------------------------------------

https://docs.graylog.org/docs/ubuntu

https://losst.ru/ispolzovanie-elasticsearch#2_Список_индексов_Elasticsearch

https://docs.graylog.org/docs/elasticsearch

https://serverspace.ru/support/help/ustanovka-graylog-na-ubuntu-18-04/

https://logz.io/blog/filebeat-tutorial/#configurefilebeat

#### SSL
https://www.elastic.co/blog/configuring-ssl-tls-and-https-to-secure-elasticsearch-kibana-beats-and-logstash#step-2-4

https://www.elastic.co/guide/en/beats/filebeat/current/configuration-ssl.html

https://discuss.elastic.co/t/metricbeat-certificate-signed-by-unknow-authority/288391

https://www.elastic.co/guide/en/kibana/8.3/kibana-encryption-keys.html

#### Настройка elasticsearch
https://stackoverflow.com/questions/50609417/elasticsearch-error-cluster-block-exception-forbidden-12-index-read-only-all#:~:text=This%20happens%20when%20Elasticsearch%20thinks,many%20gigabytes%20of%20free%20space.

https://kb.objectrocket.com/elasticsearch/how-to-fix-the-forbidden-12-read-only-api-error-in-elasticsearch-282

