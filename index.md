---

layout: yandex2

style: |
    /* собственные стили можно писать здесь!! */
    
    .xxx {background-color: #555;}
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

![](pictures/run2-00.png)

## Types of property 'textDocumentSync' are incompatible.
{:.blockquote}

## Сообщения об ошибках
{:.fullscreen .xxx}

![](pictures/run2-01.png)

## [TextDocumentSyncKind](https://microsoft.github.io/language-server-protocol/specification)
{:.shout}

## Property 'loc' does not exist on type 'AstIdentifier'.
{:.blockquote}

## Сообщения об ошибках
{:.fullscreen .xxx}

![](pictures/run2-02.png)

## Сообщения об ошибках
{:.fullscreen .xxx}

![](pictures/run2-03.png)

## Запустилось!
{:.fullscreen .xxx}

![](pictures/run2-04.png)

## Чиним превью
{:.section}

## Regex
{:.fullscreen .xxx}

![](pictures/preview2-01.png)

## Regex
{:.fullscreen .xxx}

![](pictures/preview2-02.png)

## Regex
{:.fullscreen .xxx}

![](pictures/preview2-03.png)

## Отладка Webview
{:.fullscreen .xxx}

![](pictures/preview-01.png)

## URL SCHEME
{:.fullscreen .xxx}

![](pictures/preview2-04.png)

## URL SCHEME
{:.fullscreen .xxx}

![](pictures/preview2-05.png)


## SELECTORS
{:.fullscreen .xxx}

![](pictures/preview2-06-1.png)

## SELECTORS
{:.fullscreen .xxx}

![](pictures/preview2-06-2.png)

## FIXED
{:.fullscreen .xxx}

![](pictures/preview2-07.png)

## Превью работает, линтер не работает
{:.fullscreen .xxx}

![](pictures/preview-13.png)

## Чиним линтер
{:.section}

## Как запускается линтер
{:.fullscreen .xxx}

![](pictures/linter-01.png)

## Debugging Language Server
{:.fullscreen .xxx}

![](pictures/debug-01.png)

## Debugging Language Server
{:.fullscreen .xxx}

![](pictures/debug-02.png)

## Ошибка парсинга JSON
{:.fullscreen .xxx}

![](pictures/linter2-01.png)

## Ошибка парсинга JSON
{:.fullscreen .xxx}

![](pictures/linter2-02.png)

## Пустой список ошибок
{:.fullscreen .xxx}

![](pictures/linter-02.png)

## Пустой список ошибок
{:.fullscreen .xxx}

![](pictures/linter-03.png)

## Не исчезает последняя ошибка
{:.fullscreen .xxx}

![](pictures/linter-04.png)

## Не исчезает последняя ошибка
{:.fullscreen .xxx}

![](pictures/linter-05.png)

## Не исчезает последняя ошибка
{:.fullscreen .xxx}

![](pictures/linter-06.png)

## SEVERITY
{:.fullscreen .xxx}

![](pictures/severity-01.png)

## SEVERITY
{:.fullscreen .xxx}

![](pictures/severity-02.png)


## Другие критерии
{:.section}

## Линтер из второго задания

- починить тестовый линтер
- подключить линтер из второго задания в отдельной ветке

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

## Исправить code style

Мы добавили нарушения codestyle:

- отступы
- лишние пробелы и переносы строк
- кавычки
- точки с запятой

## Обосновать принятые решения

- описан ход мыслей
- атомарные коммиты, понятные сообщения

## Спасибо! 
{:.contacts}

{% if site.author %}

<figure markdown="1">

### {{ site.author.name }}

{% if site.author.position %}
{{ site.author.position }}, Яндекс.Директ
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
