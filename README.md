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
Если нужно что бы в блоке открывался только один слойлер добавляем атрибут ```data-one-spoller```
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
#
При инициализации споллера к родительскому .
```html 
<div data-spollers class="spollers">
    <!-- сполер 1 -->
    <!-- сполер 2 -->
    <!-- сполер 3 -->
</div>
```
Будет динамически добавлен класс ```_spoller-init``` .
```html 
<div data-spollers class="spollers _spoller-init">
    <!-- сполер 1 -->
    <!-- сполер 2 -->
    <!-- сполер 3 -->
</div>
```
#
Активный (открытый) споллер.<br>
Заголовок споллера получает класс ```_spoller-active``` .
```html
<button type="button" data-spoller class="spollers__title _spoller-active">Заголовок споллера</button>
```
#
Базовые стили спойлеров 
```css
/* Блок со спойлерами */
.spollers {
    display: grid;
    gap: 15px;
}

/* Спойлер */
.spollers__item {
    font-size: 20px;
}

.spollers__item:not(:last-child) {
	margin-bottom: 5px;
}

/* Заголовок спойлера */
.spollers__title {
    width: 100%;
    cursor: default;
    text-align: left;
    border: 1px solid #eee;
    padding: 20px 15px;
    border-radius: 5px;
    position: relative;
}

._spoller-init .spollers__title {
    cursor: pointer;
}
/* Анимированные стрелки */
._spoller-init .spollers__title::before,
._spoller-init .spollers__title::after {
    content: "";
    position: absolute;
    right: 10px;
    top: 50%;
    background-color: #000;
    height: 2px;
    width: 15px;
    transition: transform 0.5s ease 0s;
}

._spoller-init .spollers__title::before {
    transform: translate(-75%, -50%) rotate(40deg);
}

._spoller-init .spollers__title::after {
    transform: translate(0, -50%) rotate(-40deg);
}

.spollers__title._spoller-active::before {
    transform: translateX(-75%) rotate(-40deg);
}

.spollers__title._spoller-active::after {
    transform: rotate(40deg);
}

/* Контент спойлера */
.spollers__body {
    padding: 20px;
    border-radius: 5px;
    border: 1px solid #eee;
}
```
#
[Смотреть демо](https://beserega.github.io/spollers/) ( _Открыть в новой вклвдке_  **CTRL + ЛКМ**  )
