### 1. Вопросы:

1. Как хорошо Вы владеете Python? Оцените свой уровень по шкале от 0 до 10,
где 0 - совсем не знаю, 10 - владею в совершенстве.
Объясните, почему Вы выбрали такой балл.

- У меня есть опыт работы с Python и разработки приложений на нем, но уменя    
все еще есть пробелы в знаниях языка. Так что я оценю свои знания в 6-7 баллов.

2. Насколько хорошо Вы знакомы с Google Sheets? Оцените свой уровень по
шкале от 0 до 10, где 0 - совсем не знаю, 10 - владею в совершенстве.
Объясните, почему Вы выбрали такой балл.

- Я регулярно пользуюсь google sheets, в основном в место ms excel. 
Никогда не использовал скриптовую часть google (apps scripts). Так что я отмечу свои знания на 6 баллов.

### 2. Задачи на логику:
1. Рекламная кампания стартовала вчера с дневным бюджетом 40 $. Половина
бюджета была израсходована к полудню, а 80% оставшегося бюджета было
потрачено между полуднем и временем закрытия. Сколько долларов не было
потрачено?

- Задача довольно простая так что я не буду приводить решение. <br>**Ответ: 4 $**

2. 5 идентичных рекламных кампаний работали 24 дня по 6 часов в день,
потрачено было 120 долларов. Сколько дней они работали бы на 216 долларов,
если бы 9 одинаковых кампаний работали бы по 8 часов в день?

- Сначало найдем сколько одна компания тратит денег на один час работы. 
    <br>
    х = 120 / (5 * 24 * 6) ~ 0,17
    <br>
    Затем посчитаем сколько дней проработали бы 9 таких же компаний с большим бюджетом и рабочим днем.
    <br>
    days = 216 / (9 * 8 * х) ~ 17
    <br>
    **Ответ: 17 дней**

3. Дизайнеры создали 200 рекламных баннеров для двух рекламных кампаний. 80
из них не использовались ни в кампании №1, ни в кампании №2, 60
использовались только в кампании №1. И для каждого рекламного баннера,
который использовался в обеих кампаниях, приходится 3 баннера, которые
использовались только в кампании №2. Сколько баннеров было использовано в
обеих рекламных кампаниях?

- Изначально будем считать что все баннеры использовались обеими компаниями.
    S = 200
    80 баннеров не использовались ни одной: 
    <br> 
    S = 200 - 80 = 120
    <br>
    60 использовались только в компании №1:
    <br>
    S = 120 - 60 = 60
    <br>
    И для каждого рекламного баннера, который использовался в обеих кампаниях, приходится 3 баннера.
    Число баннеров которое использовали обе компании - х, => 
    <br>
    S = x + 3 * x
    <br>
    S = 4 * x
    <br>
    x = S / 4 = 60 / 4 = 15
    <br>
    **Ответ: 15 баннеров**

4. Энн использует Instagram, но не Facebook, а Джон использует Youtube и
Facebook. Кейт использует Youtube, но не Instagram, а Том использует Facebook,
но не Youtube. Если каждый человек использует две из трех социальных сетей,
у кого предпочтения совпадают?


| Name |   Instagram   |   Facebook    |  Youtube  |
|----- | ------------- | ------------- | --------- |
| Ann  |     True      |    False      |    Maybe  |
| John |     Maybe     |    True       |    True   |
| Kate |     False     |    Maybe      |    True   |
| Tom  |     Maybe     |    True       |    False  |

Таблица соответствует условиям задачи, где Maybe отмечает тот факт что неизвестно точное значение. Вопрос к задачи переводит Maybe к тому чтобы стать либо False, либо True

| Name |   Instagram   |   Facebook    |  Youtube  |
|----- | ------------- | ------------- | --------- |
| Ann  |     True      |    False      |    True   |
| John |     False     |    True       |    True   |
| Kate |     False     |    True       |    True   |
| Tom  |     True      |    True       |    False  |

После преобразований, получается что Kate и John имеют одинаковые предпочтения.

**Ответ: Джон и Кейт**

5. Средний итоговый балл стажера по 4 модулям составляет 78 баллов. Сколько
баллов должен получить стажер за 5-й модуль, чтобы средний балл по всему
заданию составил 80?

- Для начала найдем суммарный бал за прошлые модули S:
<br>
S / 4 = 78 => S = 78 * 4 => S = 312
<br>
Зная S, найдем необходимый балл x.
<br>
(S + x) / 5 = 80 => S + x = 80 * 5 => x = 80 * 5 - S => x = 88
<br>
**Ответ: 88 баллов**

6. Заказанные в приложении товары доставляются на автомобиле. Автомобиль
проезжает 260 км со средней скоростью 80 км / ч. На обратном пути машина
движется со средней скоростью 100 км / ч. Насколько быстрее был обратный
путь? Ответ указать в минутах.

- Простая задача, так что только ответ.
<br>
**Ответ: 39 минут**


### 3. Техническое задание

Имеющиеся поля:
* client_id - ID клиента;
* sum – сумма денежных средств;
* status – статус оплаты;
* sale – менеджер, заключивший сделку;
* new/current – статус сделки;
* document – наличие оригинала подписанного договора с клиентом;
* receiving_date – дата получения оригинала договора.

### Задание решались с помощью Google Colab.

#### Вопросы:
1. Вычислите общую выручку за июль 2021 по тем сделкам, приход денежных
средств которых не просрочен.
2. Как изменялась выручка компании за рассматриваемый период?
Проиллюстрируйте графиком.
3. Кто из менеджеров привлек для компании больше всего денежных средств в
сентябре 2021?
4. Какой тип сделок (новая/текущая) был преобладающим в октябре 2021?
5. Сколько оригиналов договора по майским сделкам было получено в июне 2021?

#### Задание:
За каждую заключенную сделку менеджер получает бонус, который рассчитывается
следующим образом.
1. За новые сделки менеджер получает 7 % от суммы, при условии, что статус
оплаты «ОПЛАЧЕНО», а также имеется оригинал подписанного договора с
клиентом (в рассматриваемом месяце).
2. За текущие сделки менеджер получает 5 % от суммы, если она больше 10 тыс.,
и 3 % от суммы, если меньше. При этом статус оплаты может быть любым,
кроме «ПРОСРОЧЕНО», а также необходимо наличие оригинала подписанного
договора с клиентом (в рассматриваемом месяце).
Бонусы по сделкам, оригиналы для которых приходят позже рассматриваемого
месяца, считаются остатком на следующий период, который выплачивается по мере
прихода оригиналов. Вычислите остаток каждого из менеджеров на 01.07.2021.