# Modal
Библиотека модального окна на чистом JS


## ДЕМО
 [Демо плагина](http://emorozov.top/ )

## Работать с библиотекой
Поместите в ваш проект html разметку:
```html
<button data-modal-path="first">Modal</button>

<div class="modal" data-modal-wrap="modal">
    // first modal
    <div class="modal__item" data-modal-target="first">
        <button class="modal__close" aria-label="Закрыть попап"></button>
        <h3 class="modal__title">Title</h3>
        <div class="modal__content">
            <p>
              Your content
            </p>
        </div>
    </div>
    // first modal
</div>
```

## Инициализация
```javascript
const modal = new Modal();
```

## Параметры
Применяется для всех модальных окон и для конкретного
Name | Type | Default | Description | Extra options |
--- | --- | --- | --- | --- |
animation | string | show | Анимация появления | fadeIn, fadeInUp, fadeInDown, fadeInLeft, fadeInRight |
position | string | center | Позиция относительно окна браузера | top, top-left, top-right, center, center-left, center-right, bottom, bottom-left, bottom-right |
width | string | 600px | Ширина модального окна | px, %, vh, rem, em, pt, cm, mm, pc, in |
height | string | null | Высота модального окна | px, %, vh, rem, em, pt, cm, mm, pc, in |
speed | number | 250 | Скорость анимации | --- |

| Таблицы       | Это                | Круто |
| ------------- |:------------------:| -----:|
| столбец 3     | выровнен вправо    | $1600 |
| столбец 2     | выровнен по центру |   $12 |
| зебра-строки  | прикольные         |    $1 |
## Пример
Для всех
```javascript
const modal = new Modal({
    isOpen: ()=>{console.log('open')},
    isClose: (modal)=>{console.log(modal)},
    animation: 'random',
    speed: 500,
    position: 'top-right'
});
```
Для конкретного
```html
<button 
    data-modal-path="first" 
    data-modal-animation="fadeInLeft"
    data-modal-width="50%">
    Modal 3
</button>
```
## Параметры
Применяется для всех модальных окон
Name | Type | Default | Description | Extra options 
--- | --- | --- | --- | --- 
isOpen | function | --- | Определяет, открыто ли модальное окно | --- 
isClose | function | --- | Определяет, закрыто ли модальное окно | --- 
posFixed | boolean | true | Убрать скролл со страницы при открытом модальном окне | --- 
## Пример
```javascript
const modal = new Modal({
    isOpen: ()=>{console.log('open')},
    isClose: (modal)=>{console.log(modal)},
    posFixed: false
});
```


