# Парсер Авито со считыванием номера телефона
Необходимо задать страницу по которой парсить и сколько страниц в выдаче.
Чтобы не попасть под бан считываю одно объявление раз в три секунды и пробегаю по трем страницам.
Не крашится от объявлений без номера телефона и от объявлений без возможности написания сообщений продавцу

### Описание
```
Использую библиотеку selenium c вебдрайвером на хроме. Крутая штука для автотестирования как я понял. 
```
#### get_item_id(data)

Находит айди объявления по элементу массива из объявлений для того чтобы по нему потом найти кнопку: "показать телефон"
#### crop(location, size,scrolly)

вырезаем из скриншота номер телефона
для того чтобы телефон попал на скриншот - экран надо проскроллить, соответственно чтобы вырезать из скриншота телефон - надо учесть смещение экрана по оси у 

#### phone_extract (driver, table, i)

поиск ячейки с номером, клик по нему, если есть необходимость (Если номер еще скрыт, также проверяется на то, что он вообще существует)

#### sheet_scan(driver, url)

Для сканирования одной страницы, для сканирования неск страниц используем эту функцию в цикле


### Необходимые доработки:
1. Классы переменных в датафрейме преобразовать
2. Подредактировать номера телефонов
3. В идеале подключить прокси и возможность считывания каптчи, отправки ее в один из сервисов по апи и введение ответа, получаемого оттуда для масштабирования
