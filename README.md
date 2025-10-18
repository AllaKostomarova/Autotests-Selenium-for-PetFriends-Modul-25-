# selenium_25modul
Selenium UI tests — PetFriends

Набор автотестов на Selenium + PyTest для проверки страницы со списком питомцев на сайте PetFriends.

Что проверяем

присутствуют все питомцы пользователя;

у ≥ 50% питомцев есть фото;

у каждого питомца указаны имя, порода, возраст;

имена питомцев уникальны;

в списке нет дубликатов питомцев.

Дополнительно:

в тестах карточек — используются неявные ожидания (implicit waits);

в тестах таблицы — явные ожидания (explicit waits, WebDriverWait).

Технологии

Python, PyTest

Selenium WebDriver

webdriver-manager (по желанию)

Как запустить
# создать и активировать venv (рекомендуется)
python -m venv venv
# Windows: venv\Scripts\activate
# macOS/Linux: source venv/bin/activate

pip install -r requirements.txt
pytest -v

Структура
selenium_25modul/
├── tests/
│   ├── test_selenium_petfriends.py      # два теста: all pets / my pets
│   └── conftest.py                       # фикстура браузера, размеры окна
├── requirements.txt
└── README.md

Примечания

Тесты используют авторизацию на PetFriends и обращаются к страницам:

главная со списком всех питомцев,

страница «Мои питомцы».

Данные/учётные записи — тестовые.

Версии браузера и ОС не фиксированы; рекомендуется актуальный Chrome/Chromedriver.
