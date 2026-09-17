markdown
# 📓 DevDiary

![Status](https://img.shields.io/badge/status-active-green)
![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-yellow)

**DevDiary** — это *лёгкое* консольное приложение для ведения заметок разработчика.
Поддерживает **Markdown**, **теги** и **поиск** по записям.

![Скриншот DevDiary](https://www.henrymr.com/digest/89-sales-analitic)

## 📋 Оглавление

- [Возможности](#-возможности)
- [Установка](#-установка)
- [Использование](#-использование)
- [Пример заметки](#-пример-заметки)
- [Архитектура](#-архитектура)
- [Roadmap](#-roadmap)
- [Лицензия](#-лицензия)

## 🚀 Возможности

- Создание заметок в формате Markdown
- Теги и категории для организации записей
- Полнотекстовый поиск по всем заметкам
- Экспорт в HTML и PDF
- Тёмная тема оформления
- Автосохранение и резервное копирование

## 📦 Установка

1. Установите Python 3.10 или выше
2. Клонируйте репозиторий
3. Установите зависимости

```bash
git clone https://github.com/user/devdiary.git
cd devdiary
pip install -r requirements.txt


## 💻 Использование

```bash
devdiary add "Заголовок" --tag python --tag async
devdiary list --tag python
devdiary search "asyncio"

json 
{
  "id": 1,
  "title": "Изучение asyncio",
  "content": "Разобрался с event loop и корутинами",
  "tags": ["python", "async"],
  "created_at": "2024-01-15T10:30:00",
  "updated_at": "2024-01-15T11:00:00"
}


## 🏠 Архитектура ┌─────────────┐     ┌─────────────┐     ┌──────────────┐
│   CLI       │────▶│   Ядро      │────▶│  Хранилище   │
│ (argparse)  │     │ (логика)    │     │ (JSON/SQLite)│
└─────────────┘     └─────────────┘     └──────────────┘

Вложенная цитата:

Это позволяет тестировать ядро независимо от интерфейса.