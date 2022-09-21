## spollers ( аккордеон ) _Чистый JavaScripr_

Для родителя слойлеров пишем атрибут  ```data-spollers```<br>
Для заголовков слойлеров пишем атрибут ```data-spoller```<br>
##
Если нужно ```вкл \ выкл``` работу спойлеров на определённых размерах экранов
пишем параметры ширины и типа брейкпоинта.<br>
_Например:_<br>
```data-spollers = "992, max"``` - спойлеры будут работать только на экранах ```меньше``` _или_ ```равно``` _992px_<br>
```data-spollers = "768, min"``` - спойлеры будут работать только на экранах ```больше``` _или_ ```равно``` _768px_
#
Если нужно что бы в блоке открывался болько один слойлер добавляем атрибут ```data-one-spoller```
#
[Смотреть демо](https://beserega.github.io/spollers/) ( _Открыть в новой вклвдке_  **CTRL + ЛКМ**  )
#
#### Базовый html ( работают все споллеры ).
```html
<div data-spollers class="spollers">
    <!-- споллер 1 -->
    <div class="spollers__item">
        <button type="button" data-spoller class="spollers__title">Заголовок споллера</button>
        <div class="spollers__body">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
        </div>
    </div>
    <!-- споллер 2 -->
    <!-- споллер 3 -->
</div>
```
#
#### Базовый html ( работает один споллер ).
```html
<div data-spollers data-one-spoller class="spollers">
    <!-- споллер 1 -->
    <div class="spollers__item">
        <button type="button" data-spoller class="spollers__title">Заголовок споллера</button>
        <div class="spollers__body">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
        </div>
    </div>
    <!-- споллер 2 -->
    <!-- споллер 3 -->
</div>
```
#
#### Включать или выключить работу спойлеров на разных размерах экранов.
```html
<div data-spollers="992,max" class="spollers">
    <!-- споллер 1 -->
    <div class="spollers__item">
        <button type="button" data-spoller class="spollers__title">Заголовок споллера</button>
        <div class="spollers__body">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
        </div>
    </div>
    <!-- споллер 2 -->
    <!-- споллер 3 -->
</div>
```
#
###
[Смотреть демо](https://beserega.github.io/spollers/) ( _Открыть в новой вклвдке_  **CTRL + ЛКМ**  )
