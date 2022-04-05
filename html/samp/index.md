---
title: "`<samp>`"
description: "Программа запущена - что она ответит? Элемент для показа пользователю выходных данных программы."
authors:
  - webdb81
tags:
  - doka
---

## Кратко

Тег `<samp>` используется для оформления вывода данных, которые показываются пользователю в результате выполнения программы. Содержимое этого элемента воспринимается устройствами как простой текст.

## Пример

```html
<p>
  После завершения всех активных сеансов на экране появится сообщение:
  <samp>Теперь питание компьютера можно отключить.</samp>
</p>
```

<iframe title="Базовый пример" src="demos/basic/" height="100"></iframe>

## Как понять

Внутри тега `<samp>` размещается информация, которую пользователь может получить в процессе взаимодействия с программой:

- вывод информации о ходе выполнения программы;
- ошибки, предупреждения и подсказки инструментов разработчика или операционной системы;
- приглашение к вводу данных.

В браузерах текст внутри `<samp>` по умолчанию отображается моноширинным шрифтом.

💡 Если нужно показать пользователю **результат** работы программы в реальном времени, лучше использовать тег [`<output>`](/html/output/), например:

- информация, которую пользователь вводит или изменяет в форме;
- вывод расчётов по данным, которые указал пользователь (калькулятор, гороскоп и т. п.).

## Атрибуты

К тегу `<samp>` применяются все [глобальные атрибуты](/html/global-attrs/).

## Комбинация с `<var>`, `<kbd>` и `<code>`

При оформлении вывода данных `<samp>` часто комбинируют с тегами [`<var>`](/html/var/), [`<kbd>`](/html/kbd/) и [`<code>`](/html/code/):

```html
<div>
  <p>
    В ходе выполнения программы вам будет предложено указать расстояние:
  </p>
  <p>
    <samp>Введите значение для переменной <var>Distance</var>:</samp>
  </p>
</div>

<div>
  <p>Следующая команда выведет в консоли браузера результат сложения двух чисел:</p>
  <pre>
  <code>console.log(2.3 + 2.4)</code>
  <samp>4.699999999999999</samp>
  </pre>
</div>

<div>
  <p>Неправильно введённая команда не будет выполнена и в консоли отобразится ошибка:</p>
  <samp>
    <span class="console-name">user@machine:~$</span> <kbd>ckear</kbd>
    <br>
    ckear: The term 'ckear' unidentified as a name of a cmdlet, function, script file, or executable program.
    <br>
    <span class="console-name">user@machine:~$</span> <span class="console-cursor">_</span>
  </samp>
</div>
```

<iframe title="Пример использования с var и kbd" src="demos/complex/" height="240"></iframe>