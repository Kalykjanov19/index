# Комментарии

Хороший код должен сопровождаться комментариями, хотя и бытует мнение, что прекрасный код вовсе не нуждается в них. Конечно, повсеместно писать комментарии не нужно, а вот ключевые моменты лучше всего сопровождать короткими записками.

Комментарии делают ваш код чище, а также помогают достичь понимания с другими разработчиками, работающими с вашим кодом. Самое главное, чтобы вы сами понимали то, что написали и старались излагать свои мысли максимально кратко, ясно и однозначно.

Если проект, над которым вы работаете используется не только вашим отделом, компанией или внутренним сообществом, то целесообразнее писать комментарии на английском языке. Иначе, если ваш проект применяется только внутри одной компании, в которой официальным языком принят, например, русский язык, то логичнее всего будет использовать именно его.

## Базовый синтаксис

Препроцессор Less поддерживает несколько синтаксисов написания комментариев. Самый очевидный — это стандартный для CSS синтаксис. Если отключена минификация (компрессия, сжатие) кода, то такие комментарии, содержащиеся между `/* */`, будут сохраняться в CSS-файле после компиляции. Поэтому используйте такой вид комментариев с умом.

```less
/* Это стандартный однострочный комментарий для CSS */

/*
 А это стандартный блочный комментарий для CSS.
 При необходимости можно использовать и его.
*/
```

Помимо стандартного синтаксиса предлагается и препроцессорный, но только лишь однострочный вариант записи. Комментарии начинающиеся с `//` не будут сохраняться в CSS-файл после компиляции.

```less
// Это препроцессорный однострочный комментарий
```

## Особые комментарии

Иногда требуется сохранить какие-то комментарии после компиляции и даже минификации кода. Такой подход чаще всего используется для включения в файл информации о лицензии, авторских правах, версии библиотеки и прочих важных сообщений. Как и в CSS для этого используются комментарии, заключённые в `/*! */`.

```less
/*! Комментарий, который будет всегда сохраняться */
```

Также допустима запись `/*! !*/`, но она считается избыточной и применяется крайне редко, если вообще применяется.

```less
/*! Комментарий, который будет всегда сохраняться !*/
```

## Вложенные комментарии

К сожалению, вкладывать комментарии в комментарии, как и CSS, Less не умеет. Однако, допустимо смешивать комментарии, заключённые в `/* */` и однострочные комментарии, начинающиеся с `//`.

```less
/*
  // Смешивание комментариев
*/
```

Можно попытаться вложить комментарии и наоборот:

```less
// /* Этот комментарий вложен в другой комментарий */
```

После компиляции less-файлов, в первом случае комментарий будет отображаться в скомпилированном CSS-файле, а вот втором случае — нет.
