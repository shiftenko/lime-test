* Некорректное отображение блока новости на  главной странице в chrome dev tools при обновлении страницы после ее первичной загрузки. Проявляется это в том, что нижняя граница градиента внутри блока толщиной примерно в 1px становится прозрачной, а нижняя граница блока скрывается за чем-то. Раньше это поведение было у блока обзора, но потом перешло на блок новости, хоть css блока новости и не менялся. Также один раз было замечено такое поведение на телефоне, но при последующих попытках опять обнаружить такое поведение с помощью обновления страницы разными способами все было нормально
* При переходе с версии сайта для телефона на версию для пк в chrome dev tools выполняется анимация transition для сайдбаров на телефонах и планшетах, имеющих другой вид на пк
* Можно заменить line-height на padding для выравнивания текста в некоторых элементах макета, но это муторно
* Баннер на телефонах и планшетах временно спрятан, так как из-за того, что он находился под кнопкой показа каталога на главной странице, точки, обозначающие навигацию среди баннеров делали дизайн слайдера некрасивым при нахождении в различных местах
* Очень редко в chrome dev tools замечалось, что позиция прокрутки любого сайдбара не сбрасывалась при его закрытии, но такое поведение не было замечено при всевозможных запланированных манипуляциях
* Чтобы корректно обновить кэш svg спрайта надо прервать работу webpack, изменить ревизию кеша в файле, обеспечивающем кеширование svg спрайта в localStorage и запустить webpack, вместо простого изменения ревизии
* Не используется responsive-loader для создания изображений разных размеров на основе единственного изображения, потому что он не поддерживает формат webp
* Не используется DllPlugin для webpack так как слишком непонятно, как его внедрить в проект
* Когда выполняется переход на другую страницу при открытом сайдбаре каталога не воспроизводится анимация его закрытия после перехода, в отличие от сайдбара меню
<!--stackedit_data:
eyJoaXN0b3J5IjpbNjYzOTM2NTA5LC00NjU0NTE5MjFdfQ==
-->