1. Создание нового пользователя:

    docker exec -it mailserver setup email add <name>@ananas.guru <Password>

2. Редактирование пароля пользователя:

   docker exec -it mailserver setup email setpassword <name>@ananas.guru <NewPassword>

3. Удаление пользователя:
    docker exec -it mailserver setup email del <name>@ananas.guru
    
4. Список всех пользователей:
    docker exec -it mailserver setup email list

5. Настройка почтового клиента
    Входящая почта (IMAP):
    Сервер: ananas.guru

    Порт: 993

    Безопасность: SSL/TLS

    Аутентификация: Обычный пароль

    Исходящая почта (SMTP):
    Сервер: ananas.guru

    Порт: 465 (SSL/TLS) или 587 (STARTTLS)

    Безопасность: SSL/TLS или STARTTLS

    Аутентификация: Обычный пароль

    Учетные данные:
    Email: <name>@ananas.guru

    Имя пользователя: <name>@ananas.guru

    Пароль: <Password>

6. Проверка статуса сервера:
    docker exec mailserver supervisorctl status

7. Проверка логов сервера:
    docker logs mailserver

8. Перезапуск сервера:
    Из папки проекта:
    docker-compose restart mailserver

9. Запуск сервера:
    Из папки проекта:
    docker-compose up -d

10. Остановка сервера:
     Из папки проекта:
     docker-compose down

11. Проверка статуса сервера:
        docker exec mailserver supervisorctl status



