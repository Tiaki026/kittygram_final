# Социальная сеть Kittygram 
## Описание
Kittygram — социальная сеть для обмена фотографиями любимых питомцев. Это полностью рабочий проект, который состоит из бэкенд-приложения на Django и фронтенд-приложения на React. В нем Вы можете разместить фото любимого котика и посмотретить фото котиков других пользователей. Регистрация обязательна.
## Процесс разработки, особенности и трудности
Первый проект развертки на удаленном сервере OS Ubuntu Linux по курсу "Python-разработчик" Яндекс Практикума. 
### Было изучено:
- как подключаться к удаленному серверу
- как "подружить" сервер с аккаунтом на GitHub
- как запустить проект, используя веб-серверы разработки бэкенда и фронтенда.
- что такое WSGI-сервер
- как установить, запустить и настроить автоматизацию Gunicorn
- что такое Веб- и обратный прокси-сервер
- как установить, запустить и настроить автоматизаю Nginx
- как получить доменное имя
- как получить и настроить SSL-сертификат
- как можно мониторить доступность и собирать ошибки на примере UptimeRobot и Sentry
  
  UPD:
- как работать с Docker, Dockerhub, образами и контейнерами
- как автоматизировать загрузку контейнеров на сервер при каждом пуше на Github

### Трудности возникшие в работе
Первое, что можно выделить, это интерфейс. Работа в терминале похожа на фильмы про хакеров, монотонный фон черного (в моем случае) цвета и непонятные команды, к которым привыкаешь, запоминаешь и работаешь более уверенно
Так же в проекте нужно хорошо ориентироваться, в этом, да и в любом другом проекте с терминалом, Вам помогут команды
```
sudo	# Позволяет исполнять команды с правами суперпользователя
ls	# С помощью этой утилиты можно посмотреть, что содержится в папке
ls -al	# Вывести каталог в виде списка и скрытыми файлами
cd	# Меняет текущий каталог, в котором работает терминал на указанный
cd ..	# Подняться по древу каталогов на уровень вверх
mkdir	# Создать папку
touch	# Создать файл
cp	# Копирование
mv	# Перемещение и переименование файла или каталога
rm	# Удалить
```
И многие другие команды, которые Вы можете найти в интернете

Второе - редактор nano. Никакой мыши - только клавиатура и горячие клавиши.
Небольшой список, который поможет редактировать
```
Ctrl+6	# Выделение текста от начальной до конечной точки
Alt+6	# Копирование
Ctrl+K	# Вырезать
Ctrl+U	# Вставить
Ctrl+S	# Сохранить изменения
Ctrl+X	# Выйти
```
UPD:
Автоматизация процесса - сказка!

## Стек технологий
- ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

  Python: Язык программирования
- ![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)

  Django: Фреймворк для создания веб-приложений
- ![DjangoREST](https://img.shields.io/badge/DJANGO-REST-ff1709?style=for-the-badge&logo=django&logoColor=white&color=ff1709&labelColor=gray)

  Django Rest Framework: Расширение для Django, предоставляющее функциональность REST API
- ![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)

  Ubuntu: Операционная система
- ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)

  JavaScript: Язык программирования для создания динамических веб-страниц
- ![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)

  React: JavaScript-библиотека для создания пользовательских интерфейсов
- ![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)

  Nginx: Веб-сервер и обратный прокси-сервер
- ![Gunicorn](https://img.shields.io/badge/gunicorn-%298729.svg?style=for-the-badge&logo=gunicorn&logoColor=white)

  Gunicorn: WSGI-сервер для запуска веб-приложений на Python
- ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
  
  Docker: Платформа для создания, развертывания и управления приложениями в изолированных средах.


## Как воспользоваться проектом
### Клонирование проекта с GitHub на сервер
```
git@github.com:Tiaki026/kittygram_final.git
```
### Настройка бэкенд-приложения
1.	Перейдите в директорию бэкенд-приложения проекта.
2.	Вместо <название_проекта> укажите название проекта, с которым работаете.
```
cd kittygram_final/backend/
```
3.	Создайте виртуальное окружение.
```
python3 -m venv venv
```
4.	Активируйте виртуальное окружение.
```
source venv/bin/activate
```
5.	Установите зависимости.
```
pip install -r requirements.txt
```
6.	Примените миграции.
```
python3 manage.py migrate
```
### Docker
Установите Docker:
 - Для Windows скачиваете программу и устанавливаете как любую другую
 - Для Linux
```
sudo apt update
sudo apt install curl
curl -fSL https://get.docker.com -o get-docker.sh
sudo sh ./get-docker.sh
sudo apt-get install docker-compose-plugin 
```
Создаем Dockerfile

 [ Dockerfile_backend](https://github.com/Tiaki026/kittygram_final/blob/main/backend/Dockerfile)
 
 [ Dockerfile_frontend](https://github.com/Tiaki026/kittygram_final/blob/main/frontend/Dockerfile)

 [ Dockerfile_gateway](https://github.com/Tiaki026/kittygram_final/blob/main/nginx/Dockerfile)

 [ Conf nginx](https://github.com/Tiaki026/kittygram_final/blob/main/nginx/nginx.conf)

Создаем образы backend, frontend, gateway. Каждый из своей директории.
```
docker build -r <ваш user docker>/kittygram_backend .
docker build -r <ваш user docker>/kittygram_frontend .
docker build -r <ваш user docker>/kittygram_gateway .
```
Пушим их на хаб, каждый по отдельности
```
docker push <название образа>
```
Создаем docker-compose.yml

 [ docker-compose](https://github.com/Tiaki026/kittygram_final/blob/main/docker-compose.yml)
 
Команды для проверки docker-compose
```
docker compose up
docker compose exec backend python manage.py migrate
docker compose down
docker compose up --build
```
создаем docker-compose.productiom.yml и main.yml

 [ docker-compose.productiom.yml](https://github.com/Tiaki026/kittygram_final/blob/main/docker-compose.production.yml)
 
 [ main.yml](https://github.com/Tiaki026/kittygram_final/blob/main/kittygram_workflow.yml)

если в файлах все написано верно, то после команды `git push` на github в actions начнется тестирование образов (если имеются тесты), создадутся образы, запушатся на dockerhub, после прилетят на удаленный сервер и запустятся. А так же в телеграм прилетит сообщение от бота, что проект успешно задеплоен.

# Авторы:

  - [Яндекс практикум](https://github.com/yandex-praktikum)
 
  - [Колотиков Евгений](https://github.com/Tiaki026)
      
