# Nevatrip-3.1

Тестовое задание https://bitbucket.org/nevatrip/test-task/src/master/

Это тестовое задание не имеет никаких технических ограничений. Ты можешь использовать любые инструменты.

1. Билеты на событие
После успешной покупки билетов на событие, данные попадают в список заказов. Список заказов сохраняется в таблице phpMyAdmin

Где:

id - инкрементальный порядковый номер заказа

event_id - уникальный ид события. У каждого события есть свое название, описание, расписание, цены и свой уникальный event_id соответственно

event_date - дата и время на которое были куплены билеты

ticket_adult_price - цена взрослого билета на момент покупки

ticket_adult_quantity - количество купленных взрослых билетов в этом заказе

ticket_kid_price - цена детского билета на момент покупки

ticket_kid_quantity - количество купленных детских билетов в этом заказе

barcode уникальный штрих код заказа

equal_price - общая сумма заказа

created - дата создания заказа


Вопросы:

1. Некоторые события нужно продавать с дополнительными типами билетов - льготный и групповой, у которых будут свои цены и название. Имеется информация, что вероятно, будут другие типы билетов, которые нужно будет добавить. Нужно уметь сохранять при заказе 2 дополнительных типа билета, льготный и групповой в бд. Задача - Показать конечный вид таблицы с добавленными типами билетов. Объяснить свое решение.

2. Часто посетители из одного заказа приходят не одновременно на события. Возникает необходимость чекинить их по отдельности. Для этого у каждого билета должен быть свой баркод. Если в одном заказе было куплено несколько билетов, 2 взрослых, 3 детских, 4 льготных - то должно быть 9 баркодов для каждого билета соответственно. Задача - Показать конечный вид таблицы, где у каждого билета свой баркод. Объяснить свое решение.

Решение:

1. id	event_id	event_date	type_of_ticket_id	type_of_ticket_price	type_of_ticket_quantity	barcode	user_id	equal_price	created
1	3	21.08.2021 13:00	1	700	1	11111111	451	700	11.01.2021 13:22
2	6	29.07.2021 18:00	2	800	2	22222222	364	1600	12.01.2021 16:52
3	3	15.08.2021 17:00	1	700	4	33333333	15	2800	13.01.2021 10:08
4	3	15.08.2021 17:00	2	450	3	44444444	15	1350	13.01.2021 10:08
									
									
id	type_of_ticket								
1	adult								
2	kid								
3	benefit								
4	group for adult								
5	group for kid								
![image](https://user-images.githubusercontent.com/104136183/197403878-667789c9-e9ac-4086-b7b0-f2673078c2b1.png)

