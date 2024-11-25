Flask API з SQLAlchemy
Це REST API для управління магазинами та товарами, розроблений за допомогою Flask і SQLAlchemy для роботи з базою даних.

Основні можливості
Магазини: додавання, перегляд та видалення магазинів.
Товари: додавання, перегляд та видалення товарів, що прив’язані до магазинів.
Вимоги до проекту
Python 3.x
Flask
Flask-SQLAlchemy
Flask-Smorest
Marshmallow
Інструкція з встановлення
Клонування репозиторію

git clone https://github.com/Eichant/API_Flask_SQLAlchemy.git
cd flask-api
Створення віртуального середовища

python -m venv venv
Активація віртуального середовища

Windows:
venv\Scripts\activate
macOS/Linux:
source venv/bin/activate
Встановлення залежностей

pip install -r requirements.txt
Запуск додатку

python -m flask run
API буде доступне за адресою: http://127.0.0.1:5000/

API Ендпоінти
Магазини
GET /stores — отримати список всіх магазинів.
GET /stores/<int:store_id> — переглянути магазин за ID.
POST /stores — створити новий магазин.
DELETE /stores/<int:store_id> — видалити магазин за ID.
Товари
GET /item/<int:item_id> — отримати товар за ID.
POST /item — створити новий товар.
DELETE /item/<int:item_id> — видалити товар за ID.
Приклади використання
Додавання магазину
POST /stores

{
  "name": "Техно Магазин"
}
Додавання товару
POST /item

{
  "name": "Ноутбук",
  "price": 1200.99,
  "store_id": 1
}
Структура проекту
app.py — основний файл програми, що відповідає за налаштування Flask та підключення ендпоінтів.
models/ — містить моделі SQLAlchemy:
store.py — модель магазину.
item.py — модель товару.
resources/ — логіка обробки HTTP-запитів:
store.py — ендпоінти для магазинів.
item.py — ендпоінти для товарів.
schemas.py — серіалізація та валідація даних за допомогою Marshmallow.
db.py — конфігурація підключення до бази даних SQLAlchemy.
requirements.txt — залежності проекту.
Автор
Черняхівський Володимир Анатолійович
Група I-23
