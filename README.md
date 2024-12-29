[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/-hH64FG6)
## Лабораторная работа: Реализация MapReduce для анализа данных о продажах с ипользованием HADOOP!!!
# Цель работы

Ознакомиться с концепцией распределенных вычислений на примере модели MapReduce. Научиться разрабатывать многопоточную систему для обработки больших данных и применять её для анализа данных о продажах.
# Описание задачи

У вас в репозитории есть несколько CSV-файлов, представляющих данные о продажах, например:

    transaction_id,product_id,category,price,quantity
    1,101,electronics,300.00,2
    2,102,books,15.00,5
    3,101,electronics,300.00,1
    4,103,toys,25.00,4
    5,102,books,15.00,3

Необходимо:

  * Вычислить общую выручку для каждой категории товаров.
  * Подсчитать общее количество проданных товаров по категориям.
  * Отсортировать категории по общей выручке в порядке убывания.

Пример вывода:

    Category      Revenue    Quantity
    electronics   900.00     3
    books         120.00     8
    toys          100.00     4

# Требования
Основная часть:

  * Используем hadoop
  * Написать реализацию MapReduce для обработки CSV-файлов.
  * Реализовать многопоточность в каждой фазе:
      * Map — обработка строк из файлов.
      * Shuffle/Sort — группировка данных по категориям.
      * Reduce — вычисление итоговых значений для каждой категории.
  * Сохранить результат в файл.
  * Обеспечить потокобезопасность при работе с общими данными.
  * Реализовать поддержку одновременной обработки большого количества файлов.

Дополнительные задачи (по желанию):

* Добавить возможность выбора метрики анализа (например, подсчёт средней цены товара в категории).

# Результаты
Результатом работы является сам код, файл с результатами и экспериментальные данные по быстродействию работы написанного кода при изменении числа worker-ов / частей, на которые разбивается файл

# Результаты из csv:
```
clothing            4560302171.99	911487
video games	        4560108307.50	913326
baby products	    4541435362.25	907186
beauty products	    4533874327.85	906417
gardening tools	    4531880837.74	905841
automotive	        4529861310.74	904962
music instruments	4512294466.14	902389
furniture	        4503986763.16	900244
electronics	        4497526631.04	903266
pet supplies	    4488741730.38	896724
stationery	        4481794912.39	898265
home appliances	    4473888361.73	895815
sports equipment	4469387812.34	894287
groceries	        4466915230.97	895470
footwear	        4465574983.36	894424
jewelry	            4463823670.79	893980
office equipment	4463564947.38	892370
toys	            4462453654.12	892741
books	            4457620825.95	890948
health & wellness	4454082892.49	890475
```
