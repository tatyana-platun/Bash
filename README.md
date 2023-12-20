# Bash
Команды Bash позволяют нам выполнять общие задачи, такие как создание, редактирование, удаление файлов и папок, через интерфейс командной строки (CLI).
В рамках задания были изучены следующие возможности: работа с файлами и директориями, редактирование файлов, проверка и завершение процессов, работа с файлами.

### Задание 1.

1. Открыть домашнюю директорию

 cd ~


2. Определить имя папки, в которой вы находитесь

 pwd


3. Создать внутри этой папки каталог  с именем test1

 mkdir test1


4. Перейти в папку test1

 cd test1


5. Создать файл 1,2 и 3 внутри каталога test1


 touch file1 file2 file3


6. Проверить содержимое каталога test1

 ls


7. Перейти в домашнюю директорию

 cd ..


8. Создать папку test2 внутри домашней директории

 mkdir test2


9. Удалить папку test2

 rmdir test2


10. Удалить файл 2 из папки test1

 rm file2


11. Создать папку в домашней директории test3 и добавить в нее два файла

 mkdir test3

 cd test3

 touch file_a file_b


12. Удалить папку test3


 rm -rf test3


13. Создать папку test4 в домашней директории

 mkdir test4


14. Переместить файлы 1 и 3 из папки test1 в папку test4

 mv test1/file1 test1/file3 test4


15. Добавить в файл 1 три строки со словами line

 echo line > file1

 echo line >> file1

 echo line >> file1

Либо второй спососб:

 echo "line
 line
 line" >> file1


16. Посмотреть содержимое файла 1

 cat file1


17. Добавьте в файл 3 три строки со словами line

 echo line > file3

 echo line >> file3

 echo line >> file3

Либо второй способ:

 echo "line
> line
> line" >> file3


18. Просмотрите содержимое двух файлов (1 и 3) сразу

 cat file1 file3


19. Используя один из редакторов замените все строки в файле 1

 nano file1

С помощью команды Ctrl+\ вводим строку, которую нужно изменить, затем вводим строку, на которую необходимо заменить.



### Задание 2

1. Зайти в домашнюю директорию

$ cd ..


2. Создать папку test 3

 mkdir test_3


3. Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4

 cd test_3

 touch file4 file5 file6

echo "row1
row2
row3
row4" >> file4

echo "row1
row2
row3
row4" >> file5

echo "row1
row2
row3
row4" >> file6


4. Найдите строку row2 в файле 5

 grep "row2" file5


5. Найдите строку row в папке test3

 grep -R "row" .


6. Посчитайте сколько строк с содержимым row в файле 6

 grep -с "row" file6


7. Найдите файл 5 внутри папки test3

$ find test_3 -name "file5"
test_3/file5


8. Используя команду find, удалите файл 5

 find test_3  -name "file5" -delete


9. Используя команду echo, добавьте слово test в файл 4

 echo test >> file4


10. Замените слово test в файле 4 на fail

 sed -i 's/test/fail/' ./file4


11. Добавьте в файл 4 слово test так, чтобы сохранилось содержимое

 echo test >> file4


12. Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе

ps aux
      

13. Убейте процесс 666 в консоли

kill 666


14. Узнайте доступность ресурса artsiomrusau.com, используя ping

ping artsiomrusau.com


15. Отправьте 5 пакетов на сайт artsiomrusau.com

ping -c 5 artsiomrusau.com


16. Используя GET и команду curl, получите информацию о зарегистрированных питомцах на https://petstore.swagger.io/

curl https://petstore.swagger.io/v2/pet/petIdcurl -X 'GET'   'https://petstore.swagger.io/v2/pet/findByStatus?status=available'   -H 'accept: application/json'


17. Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/

 curl -X 'POST' \
  'https://petstore.swagger.io/v2/user' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "id": 0,
  "username": "string",
  "firstName": "string",
  "lastName": "string",
  "email": "string",
  "password": "string",
  "phone": "string",
}'"userStatus": 0

