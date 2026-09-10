<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20&height=180&section=header&text=Yatube%20API&fontSize=70&fontAlignY=35&desc=REST%20API%20on%20Django%20%7C%20Yandex%20Practicum&descAlignY=55&descSize=18" alt="Yatube API Banner" width="100%">

<img src="https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/Django-3.2-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django">
<img src="https://img.shields.io/badge/DRF-3.12.4-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django REST Framework">
<img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite">

<br>

<img src="https://img.shields.io/badge/Pytest-6.2.4-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" alt="Pytest">
<img src="https://img.shields.io/badge/pytest--django-4.4.0-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" alt="pytest-django">
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" alt="Postman">
<img src="https://img.shields.io/badge/Yandex-Practicum-red?style=for-the-badge&logo=yandex&logoColor=white" alt="Yandex Practicum">

<br><br>

<h2>🔌 Yatube API — REST API для социальной сети</h2>

<p>
  <b>Учебный проект в рамках курса «Python-разработчик» от Яндекс Практикума</b>
</p>

</div>

---

## 📖 О проекте

**Yatube API** — REST API для социальной сети блогов, разработанное на **Django REST Framework**.

API предназначено для работы с публикациями, комментариями, сообществами и подписками на авторов.

На текущем этапе проекта реализованы модели данных, настроена административная панель, подготовлены маршруты и тестовая инфраструктура. Реализация сериализаторов, API-вьюх и части функциональности находится в разработке.

---

## ✨ Основные возможности

### 📝 Публикации

Модель `Post` предназначена для хранения публикаций пользователей.

Пост содержит:

* текст публикации;
* дату публикации;
* автора;
* изображение;
* сообщество.

Структура модели:

```text
Post
├── text
├── pub_date
├── author
├── image
└── group
```

### 👥 Сообщества

Модель `Group` используется для объединения публикаций по тематике.

Каждое сообщество содержит:

```text
Group
├── title
├── slug
└── description
```

### 💬 Комментарии

Модель `Comment` позволяет связывать комментарии с конкретными публикациями.

Поля модели:

```text
Comment
├── author
├── post
├── text
└── created
```

### 👤 Пользователи

Публикации и комментарии связаны с пользователями Django через поле `author`.

В дальнейшем API будет использовать систему аутентификации и разграничения прав доступа.

---

## 🗃️ Модели данных

| Модель      | Поля                                           |
| :---------- | :--------------------------------------------- |
| **Group**   | `title`, `slug`, `description`                 |
| **Post**    | `text`, `pub_date`, `author`, `image`, `group` |
| **Comment** | `author`, `post`, `text`, `created`            |

Связи между моделями позволяют организовать структуру социальной сети:

```text
User
 ├── Post
 │    └── Group
 │
 └── Comment
      └── Post
```

---

## ⚙️ Административная панель

Модель `Post` зарегистрирована в Django Admin с дополнительными настройками.

Используются:

| Настройка             | Назначение                                         |
| :-------------------- | :------------------------------------------------- |
| `list_display`        | Отображение `pk`, текста, даты публикации и автора |
| `search_fields`       | Поиск по тексту публикации                         |
| `list_filter`         | Фильтрация по дате публикации                      |
| `empty_value_display` | Отображение `-пусто-` для пустых значений          |

Модели `Group` и `Comment` также зарегистрированы в административной панели со стандартными настройками.

---

## 🧪 Тестовая инфраструктура

В проекте подготовлена инфраструктура для автоматического тестирования.

Используются:

* **Pytest**
* **pytest-django**
* фикстуры тестовых данных;
* фикстуры пользователей;
* отдельные тестовые модули для основных сущностей проекта.

Структура тестов:

```text
tests/
├── fixtures/
│   ├── __init__.py
│   ├── fixture_data.py
│   └── fixture_user.py
│
├── __init__.py
├── conftest.py
├── test_auth.py
├── test_comment.py
├── test_group.py
├── test_post.py
└── test_settings.py
```

### 🔍 Что проверяется

| Тест               | Назначение                     |
| :----------------- | :----------------------------- |
| `test_auth.py`     | Аутентификация и права доступа |
| `test_comment.py`  | Работа с комментариями         |
| `test_group.py`    | Работа с сообществами          |
| `test_post.py`     | Работа с публикациями          |
| `test_settings.py` | Проверка настроек проекта      |

---

## 🚧 В разработке

На текущем этапе реализация REST API ещё продолжается.

Планируется добавить:

* 🔄 Сериализаторы для `Post`, `Comment` и `Group`.
* 🔌 API ViewSet'ы.
* 🔗 Маршрутизацию API.
* 🔐 Аутентификацию пользователей.
* 🛡️ Разграничение прав доступа.
* 👥 Подписки на авторов.
* 📄 Пагинацию.
* 🔍 Фильтрацию данных.
* 🧪 Расширенное тестирование API.

---

## 🔌 REST API

Архитектура проекта строится вокруг **Django REST Framework**.

После завершения реализации API будет предоставлять HTTP-интерфейс для работы с основными сущностями проекта:

```text
Post
Comment
Group
Subscription
```

Предполагаемая логика взаимодействия:

```text
Client
   │
   ▼
REST API
   │
   ├── Posts
   ├── Comments
   ├── Groups
   └── Subscriptions
   │
   ▼
Django ORM
   │
   ▼
SQLite
```

На текущем этапе API-вьюхи и сериализаторы находятся в разработке.

---

## 🛠️ Технологический стек

| Технология                | Версия | Назначение                    |
| :------------------------ | :----- | :---------------------------- |
| **Python**                | 3.10+  | Основной язык разработки      |
| **Django**                | 3.2    | Веб-фреймворк                 |
| **Django REST Framework** | 3.12.4 | Построение REST API           |
| **SQLite**                | —      | База данных                   |
| **Pillow**                | 9.3.0  | Работа с изображениями        |
| **Pytest**                | 6.2.4  | Автоматическое тестирование   |
| **pytest-django**         | 4.4.0  | Интеграция Pytest с Django    |
| **Postman**               | —      | Ручное тестирование API       |
| **Flake8**                | —      | Проверка качества Python-кода |

---

## 📂 Структура проекта

```text
api_yatube/
├── postman_collection/
│   └── # Коллекция запросов Postman
│
├── tests/
│   ├── fixtures/
│   │   ├── __init__.py
│   │   ├── fixture_data.py     # Фикстуры постов и комментариев
│   │   └── fixture_user.py     # Фикстуры пользователей
│   │
│   ├── __init__.py
│   ├── conftest.py             # Общая конфигурация pytest
│   ├── test_auth.py            # Тесты аутентификации
│   ├── test_comment.py         # Тесты комментариев
│   ├── test_group.py           # Тесты сообществ
│   ├── test_post.py            # Тесты публикаций
│   └── test_settings.py        # Тесты настроек
│
├── yatube_api/
│   ├── posts/
│   │   ├── migrations/         # Миграции базы данных
│   │   ├── __init__.py
│   │   ├── admin.py            # Настройка Django Admin
│   │   ├── apps.py             # Конфигурация приложения
│   │   ├── models.py           # Group, Post, Comment
│   │   ├── urls.py             # Маршруты приложения
│   │   └── views.py            # API-вьюхи
│   │
│   ├── yatube_api/
│   │   ├── settings.py         # Настройки проекта
│   │   ├── urls.py             # Главные маршруты
│   │   └── wsgi.py             # WSGI-конфигурация
│   │
│   └── manage.py               # Управляющий скрипт Django
│
├── .gitignore                  # Исключения Git
├── LICENSE                     # Лицензия
├── README.md                   # Документация проекта
├── pytest.ini                  # Конфигурация pytest
├── requirements.txt            # Зависимости проекта
└── setup.cfg                   # Конфигурация Flake8
```

---

## 🚀 Запуск проекта

### 📋 Требования

Перед началом работы убедитесь, что установлены:

* **Python 3.10+**
* **pip**
* **Git**

<details>
<summary><b>1. Клонирование репозитория</b></summary>

```bash
git clone https://github.com/DarkSwordman999/api_yatube.git
cd api_yatube
```

</details>

<details>
<summary><b>2. Создание виртуального окружения</b></summary>

```bash
python -m venv venv
```

**Windows:**

```bash
venv\Scripts\activate
```

**macOS / Linux:**

```bash
source venv/bin/activate
```

</details>

<details>
<summary><b>3. Установка зависимостей</b></summary>

```bash
pip install -r requirements.txt
```

</details>

<details>
<summary><b>4. Переход в Django-проект</b></summary>

```bash
cd yatube_api
```

</details>

<details>
<summary><b>5. Применение миграций</b></summary>

```bash
python manage.py migrate
```

</details>

<details>
<summary><b>6. Запуск сервера разработки</b></summary>

```bash
python manage.py runserver
```

После запуска проект будет доступен по адресу:

```text
http://127.0.0.1:8000/
```

Административная панель:

```text
http://127.0.0.1:8000/admin/
```

</details>

---

## 🧪 Запуск тестов

Для запуска полного набора тестов используется:

```bash
pytest
```

Для подробного вывода результатов:

```bash
pytest -v
```

Конфигурация тестирования находится в:

```text
pytest.ini
```

Основные параметры:

```ini
python_paths = yatube_api/
DJANGO_SETTINGS_MODULE = yatube_api.settings
testpaths = tests/
addopts = -vv -p no:cacheprovider
```

---

## 🧹 Линтинг

Для проверки качества и стиля Python-кода используется **Flake8**.

Конфигурация находится в:

```text
setup.cfg
```

Запуск проверки:

```bash
flake8 .
```

Основные настройки:

```text
max-complexity = 10
```

Игнорируются правила:

```text
W503
F811
```

Из проверки исключены:

```text
tests/
*/migrations/
venv/
env/
```

Для `settings.py` отключено правило `E501`.

---

## 📬 Postman

Для ручной проверки API подготовлена коллекция запросов Postman.

Коллекция находится в:

```text
postman_collection/
```

После запуска Django-сервера в качестве базового адреса можно использовать:

```text
http://127.0.0.1:8000
```

Коллекция предназначена для проверки API-запросов по мере реализации соответствующих эндпоинтов.

---

## 📄 Лицензия

Проект распространяется в соответствии с лицензией, указанной в файле [`LICENSE`](./LICENSE).

---

## 👤 Автор

<div align="center">

### DarkSwordman999

<a href="https://github.com/DarkSwordman999">
  <img src="https://img.shields.io/badge/GitHub-DarkSwordman999-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
</a>

</div>

---

<div align="center">

### ⭐ Понравился проект?

Если **Yatube API** оказался полезным или интересным,
**поставьте ⭐ репозиторию на GitHub** — это лучшая поддержка проекта!

<a href="https://github.com/DarkSwordman999/api_yatube">
  <img src="https://img.shields.io/badge/⭐%20Star%20repository-181717?style=for-the-badge&logo=github&logoColor=white" alt="Star repository">
</a>

<br><br>

<i>Спасибо за интерес к проекту! 🚀</i>

</div>

---

<div align="center">

### 🎓 Yandex Practicum

**Проект создан в рамках курса «Python-разработчик» от Яндекс Практикума.**

<i>Учебный проект. Создан в образовательных целях.</i>

</div>
