# MongoDB
___
MongoDB система с одним мастером и репликами, которые обновляются асинхронно. По дефолту MongoDB клиент отправляет все
запросы на чтение и запись мастер ноде, за счет этого достигается strong consistency, но теряется avalability, так как,
если мастер нода выйдет из строя выбор нового мастера занимает несколько секунд, в течение которых система будет не 
доступна. Получается по дефолту MongoDB принадлежит к классу CP систем по теореме.

# Casandra
___
Casandra мастер-мастер система, что дает нам high avalability. В дефолтном режиме, когда запись отправляетя на узел,
тот возвращает успех, как только данные будут на него записаны. Остальные узлы в какой-то момент получается данные,
что говорит о том, что мы имеем только eventuly consistency. AP по CAP теореме.

# MSSQL
___
Реляционная СУБД. Поддержка ACID дает нам strong consistency. А так же синхронная репликация master-master дает нам 
avalability, следовательно MSSQL относится к классу CA по CAP теореме.