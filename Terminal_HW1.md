# Terminal_HW1

| Задание | Команды |
|---------|---------|
|1. Посмотреть где я|`pwd`|
|2. Создать папку|`mkdir` Terminal_hw1|
|3. Зайти в папку|`cd` Terminal_hw1|
|4. Создать 3 папки|`mkdir` dir{1..3}|
|5. Зайти в любоую папку|`cd` dir1|
|6. Создать 5 файлов (3 txt, 2 json)|`touch` t{1..3}.txt j{1..2}.json|
|7. Создать 3 папки|`mkdir` poddir{1..3}|
|8. Вывести список содержимого папки|`ls -l` (-la еще скрытые) |
|9. Открыть любой txt файл|`vim` t1.txt |
|10. Написать туда что-нибудь, любой текст.| Режим редактировния вызывается клавишей `i`, ввести текст и выйти из режима редактирования `esc`|
|11. Сохранить и выйти.|`:` > `wq` > `enter` (q - выйти без сохранения) |
|12. Выйти из папки на уровень выше|`cd ..`|
|13. Переместить любые 2 файла, которые вы создали, в любую другую папку.|`mv` *.json ../dir2  (* - все, или ставить число 2, а если папка не в              род.директории, то указывать полный путь - директории через / )|
|14. Скопировать любые 2 файла, которые вы создали, в любую другую папок|`cp` t1.txt t2.txt ../dir2 |
|15. Найти файл по имени|`find ./ -name` t1.txt  (перед этим выйти в гол.директорию cd ..|
|16. Просмотреть содержимое в реальном времени |`tail -f` ~/AppData/Local/Temp/|
|17. Вывести несколько первых строк из текстового файла|`head` -n -3 ~/Local/1.txt|
|18. Вывести несколько последних строк из текстового файла|`tail -n` -4 1.txt - покажет последние 4 строки файла `tail` ~/Local/Customer - покажет последние 10 строк файла `tail - f` ~/Local/Customer - будет показывать 10 строк и поступающие изменения файла, `ctrl c` - закончить просмотр|
|19. Просмотреть содержимое длинного файла (команда less) изучите как она работает.|`less` ~/Local/Customer `less -N` ~/Local/Customer - покажет также номера строк,`less /текст` ~/Local/Customer - поиск текста в файле по направлению к концу, а ?текст - к началу файла|
|20. Вывести дату и время|`date`|
|21. Отправить http запрос на сервер.|`cURL` http://162.55.220.72:5005/terminal-hw-request|


## Script

 > Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
 
    #!/bin/bash
    cd Terminal_hw1
    mkdir dir{4..6} 
    cd dir4
    touch file{3,4}.json file{6..8}.txt
    mkdir poddir{4..6}
    ls
    cp file3.json file7.txt ../dir5
    echo "script is work"

