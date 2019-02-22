## Компонент кнопок действий корзины `ui-cart-controls`

Компонент служит для вывода формы и кнопок сабмита корзины, а также выводит финальные стоимость и скидки в корзине.
Внутри компонента собираются все товары и при клике по кнопке "Оформить заказ" сабмитятся.

### Пример использования
```
<ui-cart-controls
  discount-caption="Скидка по корзине"
  button-icon="fa fa-shopping-cart"
  button-caption="Оформить заказ"
  total-caption="Итоговая стоимость"
  total-count-caption="Итоговое количество"
  {% if account.quick_checkout.enabled %}
  one-click-caption='Заказать в 1 клик'
  {% endif %}

></ui-cart-controls>
```

### Параметры компонента

 - `one-click-caption` - Подпись для кнопки быстрого заказа
 - `total-caption` - Подпись для суммы общего заказа
 - `button-caption` - Подпись для кнопки оформления заказа
 - `total-count-caption` - Подпись для общего кол-ва товаров в корзине
 - `discount-caption` - Подпись для итоговой скидки
 - `is-one-click` - Включать ли заказ в 1 клик в корзине.

### Темизация
 * `color-sheme` Параметры:
  - `default` - кнопка быстрого заказа с прозрачным фоном.
 * `layouts` Параметры:
  - `default` - Итоговая сумма находится на последней строчке
  - `slot-before-controls`  - Итоговая сумма находится между скидкой и кол-ом товаров.
 * `themes` Параметры:
 - `border-break` - строки итогов корзины разделены горизонтальными линиями, и между ними увеличены расстояния