## Структура проекта

В структуру любого проекта входят:

* Файл package.json: хранит метаданные о вашем проекте, а также библиотеки, используемые в качестве зависимостей;
* Файл package-lock.json: хранит точные версии библиотек, используемых в рабочем состоянии вашего проекта;
* Файлы проекта .rt: содержат основные файлы вашего проекта, написанные на RTS;
* Другие файлы проекта.

Чтобы создать новый проект, вы можете использовать встроенный менеджер пакетов RTS со следующими командами:

* `./rts package local`
* `./rts package local <package name>`

Для более подробной информации о командах вы можете использовать:

* `./rts package help`