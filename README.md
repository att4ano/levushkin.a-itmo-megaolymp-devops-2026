# levushkin.a-itmo-megaolymp-devops-2026

Добавить группы: sudo groupadd -g 1001 developers
sudo groupadd -g 1002 admins

Добавил через файл /etc/sudoers группу admins, чтобы можно было использовать пользователям из этой группы команды без sudo

Создал пользователей через sudo adduser developer1, sudo adduser admin1
