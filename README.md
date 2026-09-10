<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20&height=180&section=header&text=Yatube%20API&fontSize=70&fontAlignY=35&desc=REST%20API%20on%20Django%20%7C%20Yandex%20Practicum&descAlignY=55&descSize=18" alt="Banner" width="100%">

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

<p><b>Учебный проект в рамках курса «Python-разработчик» от Яндекс Практикума</b></p>

</div>

<hr>

<h2>📖 О проекте</h2>

<p><b>Yatube API</b> — REST API для социальной сети блогов. Пользователи смогут создавать публикации, оставлять комментарии, подписываться на других авторов и объединять посты в сообщества. API строится на <b>Django REST Framework</b>.</p>

<p>На текущем этапе реализованы <b>модели данных</b>, настроена админка, подготовлены маршруты и фикстуры для тестов. Реализация вьюх и сериализаторов — в процессе.</p>

<hr>

<h2>✅ Что уже сделано</h2>

<ul>
  <li>Django-проект с приложением <code>posts</code>.</li>
  <li>Модель <code>Group</code> — сообщества с полями <code>title</code>, <code>slug</code>, <code>description</code>.</li>
  <li>Модель <code>Post</code> — посты с полями <code>text</code>, <code>pub_date</code>, <code>author</code>, <code>image</code>, <code>group</code>.</li>
  <li>Модель <code>Comment</code> — комментарии с полями <code>author</code>, <code>post</code>, <code>text</code>, <code>created</code>.</li>
  <li>Настроена админка Django (Post с поиском, фильтром и кастомным отображением пустых значений).</li>
  <li>Подготовлены фикстуры и заготовки тестов.</li>
  <li>Коллекция Postman для проверки эндпоинтов.</li>
</ul>

<hr>

<h2>🚧 Что в разработке</h2>

<ul>
  <li>Сериализаторы для моделей <code>Post</code>, <code>Comment</code>, <code>Group</code>.</li>
  <li>ViewSet'ы и маршрутизация API.</li>
  <li>Аутентификация и права доступа.</li>
  <li>Эндпоинты для подписок на авторов.</li>
  <li>Пагинация и фильтрация.</li>
</ul>

<hr>

<h2>🗃️ Модели данных</h2>

<div align="center">

<table>
  <thead>
    <tr>
      <th align="left">Модель</th>
      <th align="left">Поля</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Group</b></td>
      <td><code>title</code>, <code>slug</code>, <code>description</code></td>
    </tr>
    <tr>
      <td><b>Post</b></td>
      <td><code>text</code>, <code>pub_date</code>, <code>author</code>, <code>image</code>, <code>group</code></td>
    </tr>
    <tr>
      <td><b>Comment</b></td>
      <td><code>author</code>, <code>post</code>, <code>text</code>, <code>created</code></td>
    </tr>
  </tbody>
</table>

</div>

<hr>

<h2>⚙️ Админка</h2>

<p>Модель <code>Post</code> зарегистрирована с расширенной настройкой:</p>
<ul>
  <li><code>list_display</code> — <code>pk</code>, <code>text</code>, <code>pub_date</code>, <code>author</code>.</li>
  <li><code>search_fields</code> — поиск по тексту поста.</li>
  <li><code>list_filter</code> — фильтр по дате публикации.</li>
  <li><code>empty_value_display</code> — <code>-пусто-</code> для пустых полей.</li>
</ul>

<p>Модели <code>Group</code> и <code>Comment</code> зарегистрированы со стандартными настройками.</p>

<hr>

<h2>🛠️ Технологии</h2>

<div align="center">

<table>
  <thead>
    <tr>
      <th align="left">Технология</th>
      <th align="left">Версия</th>
      <th align="left">Назначение</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><b>Python</b></td><td>3.10+</td><td>Язык разработки</td></tr>
    <tr><td><b>Django</b></td><td>3.2</td><td>Веб-фреймворк</td></tr>
    <tr><td><b>Django REST Framework</b></td><td>3.12.4</td><td>Построение REST API</td></tr>
    <tr><td><b>Pillow</b></td><td>9.3.0</td><td>Работа с изображениями</td></tr>
    <tr><td><b>SQLite</b></td><td>—</td><td>База данных</td></tr>
    <tr><td><b>Pytest</b></td><td>6.2.4</td><td>Тестирование</td></tr>
    <tr><td><b>pytest-django</b></td><td>4.4.0</td><td>Интеграция pytest с Django</td></tr>
    <tr><td><b>Postman</b></td><td>—</td><td>Ручное тестирование эндпоинтов</td></tr>
  </tbody>
</table>

</div>

<hr>

<h2>📂 Структура проекта</h2>

<pre><code>api_yatube/
├── postman_collection/         # Коллекция запросов Postman
├── tests/
│   ├── fixtures/
│   │   ├── __init__.py
│   │   ├── fixture_data.py     # Фикстуры данных (посты, комментарии)
│   │   └── fixture_user.py     # Фикстуры пользователей
│   ├── __init__.py
│   ├── conftest.py             # Общие настройки pytest
│   ├── test_auth.py            # Тесты аутентификации
│   ├── test_comment.py         # Тесты комментариев
│   ├── test_group.py           # Тесты сообществ
│   ├── test_post.py            # Тесты постов
│   └── test_settings.py        # Тесты настроек проекта
├── yatube_api/
│   ├── posts/
│   │   ├── migrations/         # Миграции БД
│   │   ├── __init__.py
│   │   ├── admin.py            # Настройка админки
│   │   ├── apps.py             # Конфигурация приложения
│   │   ├── models.py           # Модели Group, Post, Comment
│   │   ├── urls.py             # Маршруты приложения (заготовка)
│   │   └── views.py            # Вьюхи API (в разработке)
│   ├── yatube_api/             # Настройки проекта (settings, urls, wsgi)
│   └── manage.py               # Управляющий скрипт Django
├── .gitignore                  # Исключения Git
├── README.md                   # Документация
├── pytest.ini                  # Конфигурация pytest
├── requirements.txt            # Зависимости проекта
└── setup.cfg                   # Конфигурация flake8</code></pre>

<hr>

<h2>🚀 Запуск</h2>

<h3>Требования</h3>
<ul>
  <li><b>Python</b> 3.10 или выше.</li>
  <li><b>pip</b> для установки зависимостей.</li>
</ul>

<h3>Шаги</h3>
<ol>
  <li>
    <b>Клонируйте репозиторий:</b>
    <pre><code>git clone https://github.com/DarkSwordman999/api_yatube.git
cd api_yatube</code></pre>
  </li>
  <li>
    <b>Создайте и активируйте виртуальное окружение:</b>
    <pre><code>python -m venv venv

# Windows:
venv\Scripts\activate

# macOS / Linux:
source venv/bin/activate</code></pre>
  </li>
  <li>
    <b>Установите зависимости:</b>
    <pre><code>pip install -r requirements.txt</code></pre>
  </li>
  <li>
    <b>Примените миграции:</b>
    <pre><code>cd yatube_api
python manage.py migrate</code></pre>
  </li>
  <li>
    <b>Запустите сервер разработки:</b>
    <pre><code>python manage.py runserver</code></pre>
  </li>
</ol>

<hr>

<h2>🧪 Тестирование</h2>

<p>Тесты запускаются через <b>pytest</b> с плагином <b>pytest-django</b>. Конфигурация — в <code>pytest.ini</code>.</p>

<pre><code>pytest</code></pre>

<p>Что проверяется:</p>
<ul>
  <li><b><code>test_auth.py</code></b> — регистрация, вход, права доступа.</li>
  <li><b><code>test_comment.py</code></b> — комментарии к постам.</li>
  <li><b><code>test_group.py</code></b> — сообщества.</li>
  <li><b><code>test_post.py</code></b> — посты.</li>
  <li><b><code>test_settings.py</code></b> — настройки API.</li>
</ul>

<p>Фикстуры:</p>
<ul>
  <li><b><code>fixtures/fixture_data.py</code></b> — тестовые данные (посты, комментарии).</li>
  <li><b><code>fixtures/fixture_user.py</code></b> — тестовые пользователи.</li>
  <li><b><code>conftest.py</code></b> — общие настройки pytest.</li>
</ul>

<p>Параметры из <code>pytest.ini</code>:</p>
<ul>
  <li><code>python_paths = yatube_api/</code></li>
  <li><code>DJANGO_SETTINGS_MODULE = yatube_api.settings</code></li>
  <li><code>testpaths = tests/</code></li>
  <li><code>addopts = -vv -p no:cacheprovider</code></li>
</ul>

<hr>

<h2>🧹 Линтинг</h2>

<p>Код проверяется линтером <b>flake8</b>. Настройки — в файле <code>setup.cfg</code>.</p>

<pre><code>flake8 .</code></pre>

<p>Параметры из <code>setup.cfg</code>:</p>
<ul>
  <li><code>max-complexity = 10</code>.</li>
  <li>Игнорируются правила <code>W503</code>, <code>F811</code>.</li>
  <li>Исключены: <code>tests/</code>, <code>*/migrations/</code>, <code>venv/</code>, <code>env/</code>.</li>
  <li>Для <code>settings.py</code> отключено правило <code>E501</code>.</li>
</ul>

<hr>

<h2>📬 Postman</h2>

<p>В папке <code>postman_collection/</code> лежит готовая коллекция запросов. Импортируйте её в Postman, укажите базовый URL <code>http://127.0.0.1:8000</code> и выполняйте запросы к API.</p>

<hr>

<h2>👤 Автор</h2>

<div align="center">

<p><b>DarkSwordman999</b></p>

<a href="https://github.com/DarkSwordman999">
  <img src="https://img.shields.io/badge/GitHub-DarkSwordman999-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
</a>

</div>

<hr>

<div align="center">

<h3>🎓 Проект создан в рамках курса «Python-разработчик» от <a href="https://practicum.yandex.ru/">Яндекс Практикума</a></h3>

<p><i>Учебный проект. Создан в образовательных целях.</i></p>

</div>
