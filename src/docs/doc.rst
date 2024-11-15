********************************
Docs-as-Code. Выбор инструментов
********************************

 Внедрение принципа docs as code, выбор интрументов: легковесные разметки и генераторы статических сайтов, особенности, "+" и "-".

 Доп. вопросы:
 1. Разграничение доступа к документации. 
 2. Хранение скриншотов. Ваше мнение о проблеме и решении, обсуждаемые в статье: https://habr.com/ru/companies/alfa/articles/745776.

Определитесь с требованиями к инструменту
=========================================

- Выходной формат: HTML, DOCX, PDF или другие
- Если нужен HTML, то какие фичи должны быть в статическом сайте
- Требования к оформлению
- Перевод на другие языки
- Переиспользование контента
- Будет ли описание API?
- ГОСТ?
- Отечественный инструмент?
- От кого разграничивать доступ?
- Команда внедрения и бюджет?

И надо ответить на вопрос "А нам точно нужен Docs-as-Code?".

Мой опыт
========

Требования к разработке документации от команды проекта:

- Симпатичный сайт с документацией
- Перевод на другие языки
- Встраивание в сборку самого продукта
- Документация API
- Сборка DOCX

Требования к разработке документации от меня:

- Переиспользование контента
- Условия для сборки разных версий
- Сборка HTML, DOCX и PDF
- Тестирование
- Удобная работа с таблицами

Sphinx закрыл все эти требования.

Язык разметки
=============

Markdown
--------

Самый простой язык, но без спецификации, и с большим количеством диалектов:

- https://daringfireball.net/projects/markdown/syntax
- https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

ReStructuredText
----------------

Язык разметки с единой спецификацией. 

- https://docutils.sourceforge.io/rst.html
- https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html
- https://www.writethedocs.org/guide/writing/reStructuredText/

AsciiDoc
--------

Язык разметки, специально разработанный для документирования: https://asciidoc.org/

- https://t.me/asciidoctor
- `Antora <https://antora.org/>`_
- `AsciiDoc & doc-as-code Best Practices <https://bcouetil.gitlab.io/academy/BP-asciidoc.html>`_
- https://habr.com/ru/articles/550086/
- https://newpodcast2.live/podcast/vanya-and-asiidoc/
- https://habr.com/ru/users/fiddle-de-dee/publications/articles/

Сравнение движков
=================

Таблица из доклада Анжелы Андроновой (Rustore) на TechWriter Days #1:

.. image:: ssg_table.png

Свежее сравнение от Александра Яковлева (Яндекс): https://alexjameson.github.io/ssg-comparison/

Какие еще инструменты посмотреть
--------------------------------

- https://foliant-docs.github.io/
- https://gram.ax/
- https://docsify.js.org/

Опыт других компаний
====================

- https://habr.com/ru/articles/824866/
- https://habr.com/ru/companies/vk/articles/826904/
- https://habr.com/ru/companies/moysklad/articles/854708/
- https://habr.com/ru/companies/cloud_ru/articles/686050/
- https://habr.com/ru/companies/cloud_ru/articles/767014/

Разграничение доступа к документации
====================================

Обычно SSG не имеют встроенных инструментов для авторизации пользователей.

С помощью генератора можно из одного источника, репозитория, собрать несколько вариантов-версий документации, например:

- для неавторизованных пользователей и клиентов, купивших продукт;
- для простого пользователя и администратора.

Варианты решения задачи:

- купить Enterprise-версию Gramax;
- попросить админа настроить nginx, открывающий только один порт и с авторизацией;
- если документация для внутреннего пользователя, то в приватном репозитории создать вики и расшаривать только сотрудникам;
- прикрутить инструмент авторизации, например, https://auth0.com/.

Полезные ссылки
===============

- https://jamstack.org/generators/
- https://github.com/myles/awesome-static-generators
- https://squidfunk.github.io/mkdocs-material/alternatives/
- https://t.me/technicalwriters
- https://t.me/docsascode
- https://t.me/foliantdocs
- https://t.me/gramax_chat
- https://t.me/diplodoc_ru
- https://t.me/asciidoctor