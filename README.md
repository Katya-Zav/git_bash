# Работа с git и bash

## ПРАКТИЧЕСКОЕ ЗАДАНИЕ 9.2

### Задача 1

Предварительно создайте файл bash1.txt, в который вы будете добавлять выполненные команды:
**touch bash1.txt**

Открыть домашнюю диреторию через терминал:
**cd**

Определить имя папки, в которой вы находитесь:
**pwd**

Создать внутри этой папки каталог с именем test1:
**mkdir test1**

Перейти в папку test1:
**cd test1**

Создать файл 1,2 и 3 внутри каталога test1:
**touch 1.txt 2.txt 3.txt**

Проверить содержимое каталога test1:
**ls**

Перейти в домашнюю директорию:
**cd**

Создать папку test2 внутри домашней директории:
**mkdir test2**

Удалить папку test2:
**rm -r test2**

Удалить файл 2 из папки test1:
**rm test1/2.txt**

Создать папку в домашней директории test3 и добавить в нее два файла:
**mkdir test3 && touch test3/1.txt test3/2.txt**

Удалить папку test3:
**rm -r test3**

Создать папку test4 в домашней директории:
**mkdir test4**

Переместить файлы 1 и 3 из папки test1 в папку test4:
**mv test1/1.txt test1/3.txt test4**

Добавить в файл 1 три строки со словами line:
**cat > test4/1.txt**
line
line
line
**Ctrl+D**

Посмотреть содержимое файла 1:
**cat test4/1.txt**

Добавьте в файл 3 три строки со словами line:
**cat > test4/3.txt**
line
line
line
**Ctrl+D**

Просмотрите содержимое двух файлов (1 и 3) сразу:
**cat test4/1.txt test4/3.txt**

Используя один из редакторов замените все строки в файле 1:
**nano test4/1.txt**

#### Задача 2

Предварительно создайте файл bash2.txt, в который вы будете добавлять выполненные команды:
**touch bash2.txt**

Зайти в домашнюю директорию через терминал:
**cd**

Создать папку test 3:
**mkdir test3**

Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4:
**cat | tee test3/4 test3/5 test3/6 > /dev/null**
row1
row2
row3
row4
**Ctrl+D**

Найдите строку row2 в файле 5:
**grep row2 test3/5**

Найдите строку row в папке test3:
**grep row test3/***

Посчитайте сколько строк с содержимым row в файле 6:
**grep -c row test3/6**

Найдите файл 5 внутри папки test3:
**find test3 -name 5**

Используя команду find, удалите файл 5:
**find test3 -name 5 -exec rm {} \;**

Используя команду echo, добавьте слово test в файл 4 (без сохранения содержимого):
**echo test > test3/4**

Замените слово test в файле 4 на fail:
**vim test3/4**

Добавьте в файл 4 слово test так, чтобы сохранилось содержимое:
**echo test >> test3/4**

Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе:
**ps aux**

Убейте процесс 666 в консоли (можно не убивать, а просто написать команду):
**kill 666**

Узнайте доступность ресурса rusau.net, используя ping:
**ping rusau.net Ctrl+C**

Отправьте 5 пакетов на сайт rusau.net:
**ping -c 5 rusau.net**

Используя GET и команду curl, получите информацию о зарегистрированных питомцах с любым статусом на https://petstore.swagger.io/:
**curl "https://petstore.swagger.io/v2/pet/findByStatus?status=available&status=pending&status=sold"**

Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/:
curl -X 'POST' \
  'https://petstore.swagger.io/v2/user/createWithList' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '[{
    "id": 57684,
    "username": "cat121",
    "firstName": "Katya",
    "lastName": "Zav",
    "email": "string",
    "password": "string",
    "phone": "string",
    "userStatus": 0
  }]'
