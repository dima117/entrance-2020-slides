---

layout: yandex2

style: |
    /* собственные стили можно писать здесь!! */
    
    .xxx {background-color: #999;}
    .xxx img {height: 1120px;margin: 0 auto;}
    .slide.blockquote.yyy h2 {font-size: 95px;}
    .slide.blockquote.yyy>div {right:100px;}


---

# ![](themes/yandex2/images/logo-{{ site.presentation.lang }}.svg){:.logo}

## {{ site.presentation.title }}
{:.title}

### ![](themes/yandex2/images/title-logo-{{ site.presentation.lang }}.svg){{ site.presentation.service }}

{% if site.presentation.nda %}
![](themes/yandex2/images/title-nda.svg)
{:.nda}
{% endif %}

<div class="authors">
{% if site.author %}
<p>{{ site.author.name }}{% if site.author.position %}, {{ site.author.position }}{% endif %}</p>
{% endif %}

{% if site.author2 %}
<p>{{ site.author2.name }}{% if site.author2.position %}, {{ site.author2.position }}{% endif %}</p>
{% endif %}

</div>

## Разобраться в чужом коде и в незнакомом API
{:.blockquote}

## Что нужно сделать
{:.fullscreen .xxx}

![](pictures/0.png)

## Что в репозитории

- {:.next}[TypeScript](https://www.typescriptlang.org/docs/home.html)
- {:.next}[json-to-ast](https://www.npmjs.com/package/json-to-ast)
- {:.next}точка входа — extension.ts
- {:.next}настройки — package.json

## [Webview API](https://code.visualstudio.com/api/extension-guides/webview)<br/><br/>[Language Server](https://code.visualstudio.com/api/language-extensions/language-server-extension-guide)
{:.shout}

## Пробуем запустить
{:.section}

## Сообщения об ошибках
{:.fullscreen .xxx}

![](pictures/run-01.png)

## Cannot find module 'out/extension.js'.
{:.blockquote}

## Ошибка в тайпингах
{:.fullscreen .xxx}

![](pictures/run-02.png)

## Ошибка в тайпингах
{:.fullscreen .xxx}

![](pictures/run-03.png)

## Menu item references a command<br/>'example.showPreviewToSide'<br/>which is not defined<br/>in the 'commands' section.
{:.blockquote .yyy}

## Неправильное название команды
{:.fullscreen .xxx}

![](pictures/run-04.png)

## Запустилось!
{:.fullscreen .xxx}

![](pictures/run-05.png)

## Чиним превью
{:.section}

## Ошибка в CSP
{:.fullscreen .xxx}

![](pictures/preview-01.png)

## Ошибка в CSP
{:.fullscreen .xxx}

![](pictures/preview-02.png)

## [Content Security Policy](https://developer.mozilla.org/ru/docs/Web/HTTP/CSP)
{:.shout}

## Ошибка в CSP
{:.fullscreen .xxx}

![](pictures/preview-03.png)

## Неправильный путь
{:.fullscreen .xxx}

![](pictures/preview-04.png)

## Неправильный путь
{:.fullscreen .xxx}

![](pictures/preview-05.png)

## Неправильный путь
{:.fullscreen .xxx}

![](pictures/preview-06.png)

## Ошибка в стилях
{:.fullscreen .xxx}

![](pictures/preview-07.png)

## Ошибка в стилях
{:.fullscreen .xxx}

![](pictures/preview-08.png)

## Ошибка в стилях
{:.fullscreen .xxx}

![](pictures/preview-09.png)

## Превью открывается два раза
{:.fullscreen .xxx}

![](pictures/preview-10.png)

## Превью открывается два раза
{:.fullscreen .xxx}

![](pictures/preview-11.png)

## Превью открывается два раза
{:.fullscreen .xxx}

![](pictures/preview-12.png)

## Превью работает, линтер не работает
{:.fullscreen .xxx}

![](pictures/preview-13.png)

## Чиним линтер
{:.section}

## Как запускается линтер
{:.fullscreen .xxx}

![](pictures/linter-01.png)

## DEMO: Debugging<br/>Language Server
{:.shout}

## Пустой список ошибок
{:.fullscreen .xxx}

![](pictures/linter-02.png)

## Пустой список ошибок
{:.fullscreen .xxx}

![](pictures/linter-03.png)

## Другие критерии
{:.section}

## Удалить лишнее

Неиспользуемые файлы:
    
- jsonMain.ts
- hash.ts

&nbsp;

<div class="next" markdown="1">
Лишние зависимости:
    
- request-light
- vscode-nls

</div>

## Обоснованные решения

- описан ход мыслей
- атомарные коммиты, понятные сообщения

## Линтер из второго задания

- починить тестовый линтер
- подключить линтер из второго задания в отдельной ветке

## Спасибо! 
{:.contacts}

{% if site.author %}

<figure markdown="1">

### {{ site.author.name }}

{% if site.author.position %}
{{ site.author.position }}
{% endif %}

</figure>

{% endif %}

{% if site.author2 %}

<figure markdown="1">

### {{ site.author2.name }}

{% if site.author2.position %}
{{ site.author2.position }}
{% endif %}

</figure>

{% endif %}

<!-- разделитель контактов -->
-------

<!-- left -->
- {:.skype}dima117a
- {:.telegram}dima117a

<!-- right -->
- {:.mail}dima117a@yandex-team.ru
- {:.github}dima117

<!-- 

- {:.mail}author@yandex-team.ru
- {:.phone}+7-999-888-7766
- {:.github}author
- {:.bitbucket}author
- {:.twitter}@author
- {:.telegram}author
- {:.skype}author
- {:.instagram}author
- {:.facebook}author
- {:.vk}@author
- {:.ok}@author

-->
