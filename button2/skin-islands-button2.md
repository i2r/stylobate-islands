---
---

## Более новые кнопки!

Обычная кнопка, используется только один элемент:

    skin: button2

> <a class="button2" href="#x">Кнопка ссылкой</a>
>
> <div class="example:button"></div>

### Параметры кнопки

##### Размеры

У кнопок есть три основных размера: стандартный, маленький и большой. Размер задаётся модификатором `_size_N`, где «N» — нужный размер:

    skin: button _size_s

    skin: button _size_m // тут это дефолт, `_size_m` можно опустить

    skin: button _size_l

> <div>
>     <button type="button" class="small-button2">Маленькая кнопка кнопкой</button>
> </div>
>
> <div class="example:small-button"></div>

> <div>
>     <button type="button" class="big-button2">Большая кнопка кнопкой</button>
> </div>
>
> <div class="example:big-button"></div>

#### Состояния

У кнопок есть несколько состояний: `_hover`, `_active` и `_focus`.

По умолчанию они будут применяться к соответствующим псевдоклассам, но в случае необходимости можно назначать их на любые классы:

    skin: button (_focus '&.test-focus')

Небольшим исключением является состояние фокуса: для его вёрстки нужен дополнительный элемент (по умолчанию — псевдоэлемент `:before`), поэтому если нужно, можно этот элемент сделать обычным (или сменить на `:after`), можно использовать дополнительный параметр `focus-helper`:

    skin: button (_focus '&.test-focus') (focus-helper '&:after')

> <a class="focus-button2 test-focus" href="#x">Кнопка с фокусом</a>
>
> <div class="example:focus-button"></div>

## Другие кнопки

Всё, что написано выше относится как к обычной кнопке (`skin: button2`), так и кнопкам-действиям и псевдокнопкам, являющимися, по факту, отдельными скинами.

### Кнопка-действие

Как бы говорит нам: «Нажми меня!»

    skin: action-button2

> <a class="small-action-button2" href="#x">Маленькая кнопка-действие</a>
>
> <a class="action-button2" href="#x">Обычная кнопка-действие</a>
>
> <a class="big-action-button2" href="#x">Большая кнопка-действие</a>
>
> <div class="example:action-button"></div>

### Псевдокнопка

Визуально та же кнопка, но с прозрачным фоном (так что заметно будет разве что на не-белом фоне), применяется как более лёгкий вариант там, где это оправдано.

    skin: pseudo-button2

> <a class="small-pseudo-button2" href="#x">Маленькая псевдокнопка</a>
>
> <a class="pseudo-button2" href="#x">Обычная псевдокнопка</a>
>
> <a class="big-pseudo-button2" href="#x">Большая псевдо-кнопка</a>
>
> <div class="example:pseudo-button"></div>

