# 🧩 Домашнее задание 3: Работа с пакетами (Composer Package)

## 🎯 Цель

Научиться создавать собственные PHP-пакеты и подключать их в проекты с помощью Composer как внешние зависимости.

## 📦 Описание

В рамках задания необходимо:

1. Создать собственный PHP-пакет.
2. Оформить структуру согласно стандарту [PSR-4 Autoloading Standard](https://www.php-fig.org/psr/psr-4/).
3. Опубликовать пакет на GitHub или в Packagist.
4. Подключить пакет к тестовому проекту через `composer require`.

## 📂 Структура проекта (пример)

```
project-root/
├── docker/
│   └── Dockerfile
├── src/
│   └── MyPackage.php
├── composer.json
├── docker-compose.yml
└── README.md
```

## 📥 Установка

Подключение вашего пакета должно быть возможно с помощью одной из следующих команд:

```bash
composer require vendor/package-name
# или, если через GitHub
composer require vendor/package-name:dev-main --prefer-source
```

## 📐 Требования к выполнению

* ✅ Пакет должен подключаться через Composer.
* ✅ Структура и автозагрузка соответствуют PSR-4.
* ✅ Пример composer.json, показывающий подключение пакета, приложен к PR.

## 🧪 Проверка

* [ ] Пакет устанавливается без ошибок
* [ ] Классы доступны через автозагрузку
* [ ] Подключение работает как из Packagist, так и напрямую из GitHub (по желанию)

## 🐳 Рекомендованное окружение (Docker)

Рекомендуется выполнять разработку в Docker-контейнере для повторяемости и изоляции:

```yaml
version: '3.8'

services:
  php:
    image: php:8.2-cli
    volumes:
      - ./:/app
    working_dir: /app
    command: bash
```
