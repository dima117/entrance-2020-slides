В этом репозитории находится Jekyller - генератор слайдов для [Shower](https://github.com/shower/shower) на основе контента на языке Markdown. Также здесь подключена тема оформления слайдов с корпоративным стилем Яндекса.

**[Пример презентации](https://github.yandex-team.ru/pages/presentation/jekyller/)**

### Оглавление

- [Установка](#Установка)
- [Использование](#Использование)
  - [Добавление слайдов](#Добавление-слайдов)
  - [CSS классы](#css-классы)
  - [Изображения](#Изображения)
  - [Постепенное появление элементов слайда](#Постепенное-появление-элементов-слайда)
  - [Размеры и позиционирование](#Размеры-и-позиционирование)
- [Дополнительно](#Дополнительно)
  - [Как сконвертировать в PDF](#Как-сконвертировать-в-pdf)
  - [Материалы для презентаций](#Материалы-для-презентаций)
  - [Контакты](#Контакты)

## Установка

Jekyll Shower работает в GitHub Pages и для его использования не нужно ничего устанавливать на свой компьютер.

-  Форкните [этот репозиторий](https://github.yandex-team.ru/presentation/jekyller)
-  Внесите необходимые изменения (например укажите информацию о презентации и добавьте свой контент для слайдов). Кстати, это можно делать через web-интерфейс GitHub.
-  Сделайте Commit и Push своих изменений. GitHub автоматически запустит генерацию слайдов и через несколько минут презентация будет доступна на GitHub Pages по адресу: [https://github.yandex-team.ru/pages/<ваш-логин>/jekyller](https://github.yandex-team.ru/pages/presentation/jekyller).

Обратите внимание, генерация слайдов запускается при выполнении операции Push – это значит, что в первый раз слайды будут сгенерированы при первой операции Push, а не при создании форка репозитория.

## Использование
Для создания презентации с помощью Jekyller вам потребуется изменить два файла в этом репозитории: указать информацию о презентации в файле [_config.yml](_config.yml) и добавить свой контент в файл [index.md](index.md).

Откройте `_config.yml` Здесь вы можете изменить основной шаблон презентации: название и авторов презентации, соотношение сторон для слайдов — default_ratio (доступны варианты `4x3`, `16x9`, `16x10`) и язык для логотипа Яндекса — presentation:lang (`ru`, `en`).

Для работы со слайдами откройте файл `index.md`. На основе этого файла и будут сгенерированы слайды. По умолчанию в файле находится контент-заглушка с оформлением слайдов разных типов, используйте его в качестве примера. Также обращайте внимание на пояснения в комментариях.


### Добавление слайдов

Чтобы добавить в презентацию новый слайд, начните редактировать файл `index.md`. 
Выберите место для нового слайда и вставьте заголовок второго уровня с помощью символов ##: 

```md
## Название слайда
```

Текст заголовка будет использоваться как название слайда.

### CSS-классы

Вы можете назначать элементам презентации произвольные CSS-классы. Для этого укажите название класса на следующей строке после элемента:

```md
<!-- картинка справа-->
![](themes/yandex2/images/image-right.svg)
{:.image-right}
```

Вы также можете указать несколько классов через пробел:

```md
## Название слайда
{:.images .two}
```

В текущей теме презентации уже определено несколько классов, которые можно использовать для оформления слайдов. Примеры таких классов можно увидеть в файле `index.md`. 

Описать новые CSS-классы можно в верхней части файла `index.md`.

### Изображения

Чтобы создать слайд с изображениеми, выберите один из примеров в файле `index.md`. При этом старайтесь, чтобы размеры изображений соответствовали размерам, указанным на изображениях-заглушках.

Вы можете использовать пиктограммы (небольшие схематические изображения размером 240x200 пикселей) — есть несколько примеров слайдов с классом `icons`. Сами пиктограммы можно брать из [библиотеки пиктограмм Яндекса](https://patterns.yandex-team.ru/presentations?typeIn=icons). 

Также вы можете выбрать фотографию на фотостоке [istockphoto.com](http://www.istockphoto.com/ru) и прислать нам ссылку, мы купим её для вас.

Фотографии также можно выбрать из [библиотеки изображений Яндекса](https://patterns.yandex-team.ru/photos) или на фотостоке [istockphoto.com](http://www.istockphoto.com/ru). Чтобы получить изображение с фотостока, пришлите нам ссылку на [presentation@](presentation@yandex-team.ru) — и мы купим его для вас.

### Последовательное появление элементов слайда

Если вы хотите, чтобы элементы слайда (например, строки списка) появлялись по очереди, используйте CSS-класс `next`. Отмеченные им элементы будут появляться по очереди, в том же порядке, в котором они расположены в файле index.md. 

Пример разметки для последовательности картинок:

```md
![](image-1.svg)
{:.next}

![](image-2.svg)
{:.next}

![](image-3.svg)
{:.next}
```

Пример разметки для последовательности строк списка:

```md
1. {:.next}Нумерованный список
2. {:.next}Нумерованный список
3. {:.next}Нумерованный список
```

### Размеры и позиционирование элементов

Если необходимо задать размеры для элементов, указывайте значения в пикселях. При масштабировании слайдов элементы будут масштабироваться автоматически. Ширина слайда по умолчанию равна 1920px.

Если нужно разместить элемент в нестандартном месте (например, прижать к правому или нижнему краю слайда), используйте абсолютное позиционирование. 

По умолчанию стили для слайдов написаны так, чтобы контент был выровнен по сетке с шагом 30px. При выборе размеров и положения элементов старайтесь, чтобы они тоже соответствовали сетке. 

Чтобы включить отображение сетки на слайде, добавьте для него css класс `grid`:

```md
## Название слайда
{:.grid}
```

## Дополнительно

### Как сохранить презентацию в PDF

Чтобы получить презентацию в формате PDF, используйте любой браузер на основе Chromium. Откройте страницу для просмотра слайдов в режиме списка слайдов (не в режиме просмотра отдельного слайда) и выведите её на печать. В качестве принтера выберите Сохранить как PDF.

### Материалы для презентаций

Полная библиотека материалов для презентаций от лица Яндекса — примеры оформления слайдов с графиками, диаграммами, таблицами, картами, схемами, гаджетами, пиктограммы, иллюстрации и фотографии — находится по адресу [patterns.yandex-team.ru/presentations](https://patterns.yandex-team.ru/presentations).

### Контакты

Если у вас возникли вопросы, напишите нам на рассылку [presentation@](presentation@yandex-team.ru). 

Если вы хотите, чтобы мы проверили вашу презентацию, отправьте её на [prescheck@](prescheck@yandex-team.ru).
