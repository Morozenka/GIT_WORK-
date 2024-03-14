# GIT_WORK-
1. Задаю имя и email
````
git config --global user.name "Morozenka"
git config --global user.email "shirinkin07@gmail.com"
````
2. Создание локального репозиторию
````
git init
````
3. Создание .txt
````
echo. > test.txt
````
4. Добавление строк в .txt
````
echo Это первая строка >> test.txt
````
````
git add test.txt
````
закоммитил
````
git commit -m "Это первая строка"
````

![alt text](https://sun9-46.userapi.com/impg/ZEqIgKX7L2BAJcJeS5PcfsVDWv22jozw1DT58Q/GnBM0KtZrBA.jpg?size=374x127&quality=96&sign=692ac332c83e34bcc45a356e867a5ff5&type=album)

5. Посмотрел статус
````
git status
````

![alt text](https://sun9-56.userapi.com/impg/R3KDSZHwALMP3w51-QrvTdpi04S6cKVfFButXA/BUNJowDev_E.jpg?size=342x44&quality=96&sign=ffd2173f4c607617f4cf3c36944886c1&type=album)

6. Создал еще один файл
````
echo. > test2.txt
````

![alt text](https://sun9-41.userapi.com/impg/cJbLf7y-lDh3sC765qQOHUWhxDqoH0JVZDr9FQ/jwoULTZw4Eo.jpg?size=222x28&quality=96&sign=824ef004d00a0a2eea1995bdd4a6ad62&type=album)

7. Создал коммит
````
git commit -m "Это вторая строка"
````

![alt text](https://sun9-74.userapi.com/impg/1t9d9tnhO4yK6xYCWLgh3UJVgD7mmyoBWxsWlg/GZTVtKnkQKc.jpg?size=347x126&quality=96&sign=1172a65f425034dd5f3db3b9ad76420a&type=album)

8. Посмотрел протокол коммитов
````
git log
````

![alt text](https://sun9-48.userapi.com/impg/bmvE4ggsngIuwwmTU43PIS-ofgLkNeQsX00_5g/CGTWG0_drJw.jpg?size=459x173&quality=96&sign=72bef08a89ae17b4356b45c9edd5dfc3&type=album)

9. Посмотрел изменения в файле по сравнению с последним коммитом
````
git checkout -- test.txt
````
10. Убрал изменения относительно последнего коммита из файла
````
git restore test.txt
````
11. Посмотрел существующие ветки
````
git branch
````

![alt text](https://sun9-11.userapi.com/impg/j7d9kyK48wxQGOtm4BH7QyKvq77MjpVyCH5XWA/2qX6cfYSFJw.jpg?size=229x48&quality=96&sign=e92c49ffb16499a92ceaedb09bf0aae1&type=album)


12. Создал новую ветку
````
git branch test_br
````
13. Переключился на другую ветку
````
git checkout test_br
````

![alt text](https://sun9-75.userapi.com/impg/HgpPxZOaAH6F1V1AwREGG0gEXLID4_y4zyKHQw/b7ch4C8tZu8.jpg?size=241x80&quality=96&sign=7cf4c82ed060b9363559b5e13f7cd2e4&type=album)

14. Создал новую ветку и сразу же переключилися на нее
    
````
git checkout test2_br
````

![alt text](https://sun9-65.userapi.com/impg/zk93rv7fJsu9YtOQTsly26Z7hz7-TI2i4iU-Zg/DrVZ-LsF3DA.jpg?size=248x82&quality=96&sign=16361053cc8dede35c98af939d2e065c&type=album)

15. Удалил ветку

````
git branch -d test2_br
````

![alt text](https://sun9-36.userapi.com/impg/FNG-f03mRVdUxm3MdYUJEXIaK0cWXkm1d7t7gA/NZj5HE10WDI.jpg?size=269x141&quality=96&sign=bf33509d4adf8048ae1109b6971068b1&type=album)

16. Добавил merge изменения из указанной ветки в текущую
````
git checkout test_br
git merge master
````

![alt text](https://sun9-25.userapi.com/impg/0mEjT-EOlUiAs1gnaDIiurvb-CHOMViFJP5lkQ/-6m5hnschQg.jpg?size=231x138&quality=96&sign=65d91c463488bb1ee1386aa0c965c933&type=album)

17. Создал конфликт
18. Посмотрел конфликты
````
git status
````
19. Устранил конфликт
````
git add test.txt
git commit -m "Я его устронил"
````

![alt text](https://sun9-27.userapi.com/impg/tk_C8tvKpEqKEIMn_8qye6uvu6h5VjHCDtX5dQ/x-8X_FRNMHg.jpg?size=228x73&quality=96&sign=82ce0fd057e0ec9184ad9f79546dca2e&type=album)

20. Переключился на указанный коммит

````
git checkout 9ba95bf
````

![alt text](https://sun9-6.userapi.com/impg/qdcF-3ezALGig6lvwTSKHN-s6gNPZIfbDMlikg/6OSgBedvrwk.jpg?size=547x310&quality=96&sign=ab1fee58d2bdf3e1f2706826da3ca7d0&type=album)

21. Сделал ребазирование текущей ветки
````
git rebase master
````

![alt text](https://sun9-10.userapi.com/impg/HfKKgMa9kkvRONnM7_daGVHC5TcU_Ni7_3NdNA/fKpEUy4XQow.jpg?size=262x45&quality=96&sign=c6d39faa6a5684208c691af48513507e&type=album)

22. Удалил ветку
````
git branch -d test_br
````

23. Пропустил текущий конфликтный коммит и перешел к следующему
````
git rebase --skip
````

24. Отправил изменения из локального репозитория для указанной ветки в удаленный (дистанционный)

````
git remote add origin https://github.com/Morozenka/GIT_WORK-
git push origin master
````

![alt text](https://sun9-49.userapi.com/impg/XEZ6VcrhloiOJbuTBqQLo2jzB4fEBZk1VU3y4g/0PAUQ37J5DU.jpg?size=493x167&quality=96&sign=2a3e89e2fd6286961b7197e8665aa9c7&type=album)

25. Забрал изменения из репозитория, для которого были созданы удаленные ветки по умолчанию
````
git pull origin master
````

![alt text](https://sun9-77.userapi.com/impg/yFphxgX9-X8sxxROT5pInYOFF0GlgvTHS1Es3A/mhlZbIuKWMg.jpg?size=335x80&quality=96&sign=f148dcda2b09a9aa61f402ba333e5d70&type=album)

26. Забрал изменения удаленной ветки из репозитория основной ветки по умолчанию
````
git checkout -b brtest
echo. > test2.txt
git add test2.txt
git commit -m "хотите расскажу анекдот?"
git push origin brtest
git pull origin brtest:master
````

![alt text](https://sun9-11.userapi.com/impg/-NI4vx6bXypbLM70NB-jqGLxgVC5sAC_3qMo2w/Ve_A8CMO84w.jpg?size=476x334&quality=96&sign=69a37bbdcb564cd0f0e27e8c327e4dd7&type=album)

27. Клонировал репозиторий
````
git clone https://github.com/Morozenka/GIT_WORK-
````

![alt text](https://sun9-27.userapi.com/impg/VWZ5AwYK88AT-bMVda3NjDQXvCc5wAKHhre3UA/4dZ6JntS8Gc.jpg?size=462x144&quality=96&sign=6cc7747a5114b4e3b81b233686ddb1d2&type=album)
