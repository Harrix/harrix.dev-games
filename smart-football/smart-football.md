---
date: 2013-03-03
categories: [Игра]
tags:
- {Применимость: многоразовая}
- {Что требуется: ручка и бумага}
- {На сколько людей рассчитано: 2}
- {Подвижность: нет}
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
url-src: https://github.com/Harrix/harrix.dev-games/blob/main/smart-football/smart-football.md
url: https://harrix.dev/ru/games/smart-football/
lang: ru
---

# Интеллектуальный футбол на бумаге

![Featured image](featured-image.svg)

Цель игры — загнать «мяч» в ворота противника.

Вначале на листе бумаги рисуется поле **8 на 12**. В центр его рисуется крупная точка — начальное положение мяча, а снизу и сверху три точки посередине границ поля — ворота игроков:

![Игровое поле](img/playing_field.svg)

Начинают играть по жребию. Но стоить помнить, что игрок, начинающий первый имеет небольшое преимущество в игре.

Мяч может находиться **только на углах клеток**.

На **границах поля** мяч находиться **не может**, ибо при попадании на них игрок получает дополнительный ход (мяч отбивается от стенки). Исключение составляет только **момент попадания мяча в ворота**. Мяч со своего места переходит на соседний свободный угол клетки. В общем случае вокруг мяча может быть **до 8 таких углов**.

Рассмотрим **ход игры**. Игрок рисует отрезок с концами на углах клеток: первый — это тот, где находится в данный момент мяч (где противник закончил предыдущий ход), второй — любой соседний (по вертикали или горизонтали), если до этого во время игры два угла не были соединены отрезком (то есть между ними не нарисовано линии).

На рисунке ниже видно, что мяч может попасть в 8 разных позиций из центра поля:

![Мяч находится в центре поля](img/first-move_01.svg)

![Первый ход игрока](img/first-move_02.svg)

Если вы или противник до этого во время игры соединили две уголка клетки, то вы не можете опять их соединить. За игру вы каждые два уголка клетки можете соединить только один раз, то есть **ходить можно там, где еще не ходили**.

На рисунке ниже показаны всевозможные ходы за время всей игры:

![Всевозможные ходы](img/all-game-moves.svg)

Зеленым обозначено начальное положение мяча. Серым обозначены обычные размещения мяча. Красным и синим обозначены ворота и ходы, приводящие к победе.

Обратите внимание, что углы клеток по границе игрового поля (белые с серой границей) **нельзя соединять по вертикали и горизонтали**.

На этом ход игрока заканчивается. Но при соблюдении некоторых условий игрок получает **право дополнительного хода**.

Если игрок своим отрезком **коснулся уголка клетки**, из которого уже нарисованы какие-нибудь другие отрезки, то он может сделать дополнительный ход:

![Ситуация на поле](img/pass_01.svg)

![Игрок своим ходом касается другого отрезка](img/pass_02.svg)

![Дополнительный ход](img/pass_03.svg)

Если игрок своим отрезком **ходом по диагонали пересек** другой уже нарисованный отрезок, то он может сделать дополнительный ход:

![Ситуация на поле](img/pass-2_01.svg)

![Игрок своим ходом пересекает другой отрезок](img/pass-2_02.svg)

![Дополнительный ход](img/pass-2_03.svg)

Если игрок вторым концом своего отрезка **ударился о границу поля**, то он может сделать дополнительный ход:

![Ситуация на поле](img/kick_01.svg)

![Удар о границу поля](img/kick_02.svg)

![Дополнительный ход](img/kick_03.svg)

Первые два случая называются «**пасом**», а третий — «**ударом от борта**».

Если после рисования дополнительного отрезка выполнилось любое из трех условий, то игрок получает **право еще одного дополнительного хода**. Тем самым за ход игрок может сделать очень длинную цепочку.

**Важно! Отрезки рисуются цепочкой!** То есть если нарисованный отрезок вторым концом лег на угол, то следующий отрезок (игрока или противника) должна начинаться с этого же угла.

В конце хода на уголке клетки, где остановился мяч, рисуется точка крупная — там находится теперь мяч. После этого ходит противник.

Если игрок **попал в тупик**, то он **проигрывает**. Попасть в тупик — значит, что игрок вынужден нарисовать отрезок и вторым концом попасть на уголок, с которого хода для другого игрока нет.

Игра заканчивается, когда отрезок вторым концом **попадает в ворота противника**.

На рисунках ниже показано несколько первых ходов:

![Первые ходы игроков](img/game.svg)

Автор: Браништи Влад.