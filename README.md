# levushkin.a-itmo-megaolymp-devops-2026

### Контроль доступа пользователей:

Добавить группы: sudo groupadd -g 1001 developers
sudo groupadd -g 1002 admins

Добавил через файл /etc/sudoers группу admins, чтобы можно было использовать пользователям из этой группы команды без sudo

Создал пользователей через: sudo adduser developer1, sudo adduser admin1

Добавил пользователя в группу к админу
sudo usermod -a -G admins admin1

Добавил пользователя в группу к разработчикам
sudo usermod -a -G developers developer1

Добавил админа в группу docker: sudo usermod -a -G docker admin1

### Контейнеризация

Установил Docker и docker-compose:

sudo apt update
sudo apt install docker.io
sudo apt install docker-compose

Добавил в автозапуск docker через: sudo systemctl enable docker

