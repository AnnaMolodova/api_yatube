# api_yatube
### _CRUD для Yatube_

Инструменты и стек:
- python
- Django
- Django REST
 ### Реализовано API для всех моделей приложения

В репозитории — социальная сеть Yatube, но не самой последней версии и не весь, а только его бэкенд: приложения, модели.

Для взаимодействия с ресурсами настроены эндпоинты:
- api/v1/api-token-auth/ (POST): передаём логин и пароль, получаем токен.
- api/v1/posts/ (GET, POST): получаем список всех постов или создаём новый пост.
- api/v1/posts/{post_id}/ (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем пост по id.
- api/v1/groups/ (GET): получаем список всех групп.
- api/v1/groups/{group_id}/ (GET): получаем информацию о группе по id.
- api/v1/posts/{post_id}/comments/ (GET, POST): получаем список всех комментариев поста с  id=post_id или создаём новый, указав id поста, который хотим прокомментировать.
- api/v1/posts/{post_id}/comments/{comment_id}/ (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем комментарий по id у поста с id=post_id.

## Запуск проекта:
- Клонировать репозиторий и перейти в него
```sh
git clone git@github.com:AnnaMolodova/api_yatube.git
```
```sh
cd api_yatube
```
- Cоздать и активировать виртуальное окружение
```sh
python3 -m venv venv
```
```sh
source venv/bin/activate
```
- Установить зависимости из файла requirements.txt
 ```sh
pip install -r requirements.txt
```
- Выполнить миграции
```sh
python3 manage.py migrate
```
- Запустить проект
```sh
python3 manage.py runserver
```
Автор: Молодова Анна
