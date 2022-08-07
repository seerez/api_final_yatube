## Описание:
API для приложение yatube. Позволяет получать, изменять и удалять информацию о постах, комментариях и группах
## Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/seerez/api_yatube.git
```
```
cd api_yatube
```
Cоздать и активировать виртуальное окружение:
```
python -m venv venv
```
```
source venv/bin/activate
```
```
python -m pip install --upgrade pip
```
Установить зависимости из файла requirements.txt:
```
pip install -r requirements.txt
```
Выполнить миграции:
```
python manage.py migrate
```
Запустить проект:
```
python manage.py runserver
```
## Пример запросов и ответов
<sub>* для отображения запросов и ответов используем Postman</sub>

POST запрос к ```http://127.0.0.1:8000/api/v1/posts/```
```
{
"text": "Всем привет! Это тестовая запись",
}
```
GET запрос к ```http://127.0.0.1:8000/api/v1/posts/```
```
{
    {
    "id": 1,
    "text": "запись 1",
    "pub_date": "2022-07-26T17:14:23.630745Z",
    "author": "admin",
    "image": null,
    "group": null
    }
}
```