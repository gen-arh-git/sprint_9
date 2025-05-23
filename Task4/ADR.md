﻿### <a name="_b7urdng99y53"></a>**Название задачи: Передача ставок в кол-центр** 
### <a name="_hjk0fkfyohdk"></a>**Автор: Степанов Г.А.** 
### <a name="_uanumrh8zrui"></a>**Дата: 04.05.2025** 
### <a name="_3bfxc9a45514"></a>**Функциональные требования**  

|**№**|**Действующие лица или системы**|**Use Case**|**Описание**|
| :-: | :- | :- | :- |
| 1 | Сотрудник бэк-офиса, АБС, Сервис депозитов                         | Работа со списками и ставками на депозит.     | Сотрудник бэк-офиса в АБС работает (изменяет, утверждает и публикует) со списками и ставками на депозит для категорий клиентов. Обновленные списки и ставки передаются в сервис депозитов.|
| 2 | Сервис депозитов, SFTP-сервер                                      | Передача списка и ставок на депозит.          | В сетевую папку сохраняються файлы для SFTP-сервера.|
| 3 | SFTP-сервер, Система партнерского кол-центра                       | Получение списка и ставок на депозит.         | SFTP-сервер передает файлы внешнему партнеру. Внешний партнер получает и обрабатывает файлы. Загружает списки и ставки на депозит в систему партнерского кол-центра.|
| 4 | Сервис депозитов, Система кол-центра                               | Передача списка и ставки на депозит.          | Система кол-центра получает и обновляет списки и ставки на депозит.|
| 5 | Клиент, Сотрудник кол-центра, Система кол-центра, Сервис депозитов | Просмотр актуального списка и ставок на депозит. Подача заявки. | Клиент звонит в кол-центр. Сотрудник кол-центра помогает клиенту разобраться с актуальными списками и ставками на допозит. Клиент сообщает ФИО + Телефон + Сумма депозита + Офис банка. Сотрудник подтверждает заявку.|
| 6 | Клиент, Сотрудник партнерского кол-центра, Система партнерского кол-центра, SFTP-сервер | Просмотр актуального списка и ставок на депозит. Подача заявки. | Клиент звонит в кол-центр. Сотрудник кол-центра помогает клиенту разобраться с актуальными списками и ставками на депозит. Клиент сообщает ФИО + Телефон + Сумма депозита + Офис банка. Сотрудник подтверждает заявку. Созданный файл отправляется на SFTP.|
| 7 | SFTP-сервер, Сервис депозитов                                      | Получение заявок на депозит.                 | SFTP-сервер получает файлы от внешнего партнера.|
| 8 | Сервис депозитов, АБС                                              | Передача заявок на депозит.                  | Создаются заявки на открытие депозита в АБС.|

### <a name="_u8xz25hbrgql"></a>**Нефункциональные требования**

|**№**|**Требование**|
| :-: | :- | 
| 1 | Распределение телефонных вызовов с подключением партнерского кол-центра |
| 2 | Партнерский кол-центр также должен работать с актуальными списками и ставками на депозит |
| 3 | Доступность SFTP сервера 24/7 |
| 4 | Логирование и мониторинг сервисов |

### <a name="_qmphm5d6rvi3"></a>**Решение**

 - Диаграмма контекста Context.puml, Context.png 
 - Диаграмма контейнера Container.puml, Container.png 

### **Недостатки, ограничения, риски**

 - Нет контроля успешной и своевренной актуализации ставок на стороне системы партнерского кол-центра
 - Нет ограниченного доступа (только к части акутальных списков и ставок на депозит) сотруникам партнерского кол-центра к системе кол-центра банка
 
### **RoadMap**
 
 - MVP на горизонте 6 месяцев, начиная с 01.06.2025 RoadMap_bank_Standart_MVP.drawio
 - Целевое решения на горизонте года RoadMap_bank_Standart.drawio
 
 
 
 

