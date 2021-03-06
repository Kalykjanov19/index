# Селектор атрибутов [attribute*='value']

Селектор атрибутов `[attribute*='value']` выбирает элементы, которые имеют атрибут со значением, содержащим заданную подстроку.

## Синтаксис

```js
$("[attribute*='value']")
```

Добавлен в версии jQuery 1.0

## Пример

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Использование jQuery селектора атрибутов [attribute*='value']</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>
    <script>
      $(document).ready(function() {
        $("p[title*='подсказка']").css('color', 'red') // выбираем все HTML элементы <p>, которые имеют атрибут со значением, содержащим заданную подстроку и устанавливаем цвет текста - красный
      })
    </script>
  </head>
  <body>
    <p title="подсказка">Простой абзац</p>
    <p title="подсказка-1">Простой абзац</p>
    <p title="Подсказка">Простой абзац</p>
    <p title="-подсказка подсказка">Простой абзац</p>
    <p title="-подсказка">Простой абзац</p>
  </body>
</html>
```

В этом примере с использованием селектора атрибутов `[attribute*='value']` мы выбрали все элементы `<p>` в документе, которые содержат глобальный атрибут `title` со значением, содержащим заданную подстроку, и стилизовали их с использованием CSS свойства `color` (цвет текста)

Результат:

![Пример использования jQuery селектора атрибутов (значение содержит определенную подстроку).](950.png)

Пример использования jQuery селектора атрибутов `[attribute*='value']` (значение содержит определенную подстроку).
