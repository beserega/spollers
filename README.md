# spollers (аккардион)
### Чистый JavaScripr
Для родителя слойлеров пишем атрибут  [ **data-spollers** ]<br>
Для заголовков слойлеров пишем атрибут [ **data-spoller** ]<br>

Если нужно включать \ выключать работу спойлеров на разных размерах экранов
пишем параметры ширины и типа брейкпоинта.
_Например:_

data-spollers = " 992, **max** " - спойлеры будут работать только на экранах **меньше или равно** _992px_<br>
data-spollers = " 768, **min** " - спойлеры будут работать только на экранах **больше или равно** _768px_

Если нужно что бы в блоке открывался болько один слойлер добавляем атрибут [ **data-one-spoller** ]
#
###
[Смотреть демо](https://beserega.github.io/spollers/) ( _Открыть в новой вклвдке_  **CTRL + ЛКМ**  )
#
#### Базовый html (работают все споллеры).
<pre>
&ltdiv data-spollers class="spollers"&gt
    &lt!-- споллер --&gt
    &ltdiv class="spollers__item"&gt
        &ltbutton type="button" data-spoller class="spollers__title"&gtЗаголовок споллера&lt/button&gt
        &ltdiv class="spollers__body"&gt
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
        &lt/div&gt
    &lt/div&gt
    &lt!--  --&gt
&lt/div&gt
</pre>

#
#### Базовый html (работает один споллер).
<pre>
&ltdiv data-spollers data-one-spoller class="spollers"&gt
    &lt!-- споллер --&gt
    &ltdiv class="spollers__item"&gt
        &ltbutton type="button" data-spoller class="spollers__title"&gtЗаголовок споллера&lt/button&gt
        &ltdiv class="spollers__body"&gt
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
        &lt/div&gt
    &lt/div&gt
    &lt!--  --&gt
&lt/div&gt
</pre>

#
#### Включать или выключить работу спойлеров на разных размерах экранов.
<pre>
&ltdiv data-spollers="992,max" class="spollers"&gt
    &lt!-- споллер --&gt
    &ltdiv class="spollers__item"&gt
        &ltbutton type="button" data-spoller class="spollers__title"&gtЗаголовок споллера&lt/button&gt
        &ltdiv class="spollers__body"&gt
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
        &lt/div&gt
    &lt/div&gt
    &lt!--  --&gt
&lt/div&gt
</pre>

```
<div data-spollers class="spollers">
    <!-- споллер -->
    <div class="spollers__item">
        <button type="button" data-spoller class="spollers__title">Заголовок споллера</button>
        <div class="spollers__body">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
        </div>
    </div>
    <!--  -->
</div>
```
