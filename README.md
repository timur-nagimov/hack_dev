## Создаем виртуальное окружение и устанавливаем библиотеки:
Команды предполагают использование MacOS/Ubuntu
* `python3 -m venv venv`
* `source venv/bin/activate`
* `pip install -r requirements.txt`
## Поднимаем базу данных:
* Переходим в `/cd backend`
* Через `docker compose up` поднимается контейнер с postgres
## Создаем и применяем миграции
* Находясь в папке `/backend`, прописываем `alembic revision --autogenerate -m 'init'`
* Применяем миграции: `alembic upgrade head`
## Поднимаем модель:
* Находясь в главной папке, прописываем: `streamlit run ml/streamlit_app.py`