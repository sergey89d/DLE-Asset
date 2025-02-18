# DLE-Asset
Модуль для автоматического подключения стилей и скриптов в шаблон DLE

![version](https://img.shields.io/badge/version-2.0.0-red.svg?style=flat-square "Version")
![DLE](https://img.shields.io/badge/DLE-14.x-green.svg?style=flat-square "DLE Version")
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/pafnuty/DLE-Asset/blob/master/LICENSE)

## Назнчение
Модуль предназначен для лёгкого подключения стилей и скриптов к шаблону сайта.

## Преимущества
- Лёгкий в использовании.
- Быстро работает.
- Поддерживает настройки сжатия скриптов в DLE.


## Установка
### DLE 14
- Загрузить через систему плагинов файл dle-asset.xml
- В **main.tpl**, в нужном месте прописать строку подключения модуля:

Вот так:
```smarty
{include file="engine/modules/asset/add.php?folder={THEME}/css/"}
{include file="engine/modules/asset/add.php?folder={THEME}/js/"}
```
Или так:
```smarty
{include file="engine/modules/asset/add.php?folder={THEME}/css/,{THEME}/js/&ignore=main"}
```

## Добавление отдельного файла
Часто необходимо добавить отдельный файл, а не целую папку.
Для таких случаев есть addFile.php:

```smarty
{include file="engine/modules/asset/addFile.php?file={THEME}/js/main.js"}
```
