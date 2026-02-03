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

```
version: "2"

services:
  nexus:
    image: sonatype/nexus3
    volumes:
      - "nexus-data:/sonatype-work"
    ports:
      - "8081:8081"
  
volumes:
  nexus-data: {}
```

<img width="1223" height="546" alt="image" src="https://github.com/user-attachments/assets/f5d3afd8-7c96-4da0-b568-5026c95204a7" />

<img width="1220" height="701" alt="image" src="https://github.com/user-attachments/assets/4bb28519-e604-4ef6-9cc4-472420bdd072" />

<img width="1247" height="148" alt="image" src="https://github.com/user-attachments/assets/d106faa1-61a9-4c3d-a9d5-5f4b3dd129ac" />

<img width="1322" height="820" alt="image" src="https://github.com/user-attachments/assets/57a75240-53f3-4997-9156-97cc8c2268b5" />


Поменяем пароль через следующуу команду

<img width="1060" height="46" alt="image" src="https://github.com/user-attachments/assets/db783bba-ead2-483b-95d9-e4c822d710f8" />

Получаем:

<img width="1312" height="788" alt="image" src="https://github.com/user-attachments/assets/f70506ec-fc22-4f5f-ac3b-8e2f9fcf3a00" />

Настраиваем само проксирование

<img width="1050" height="499" alt="image" src="https://github.com/user-attachments/assets/6302447c-f417-4f50-b6f7-67728a7eb19a" />

<img width="1025" height="319" alt="image" src="https://github.com/user-attachments/assets/d3cdd057-0f77-49a5-924e-51e0278430f6" />

<img width="909" height="164" alt="image" src="https://github.com/user-attachments/assets/1db9650c-a230-4344-9c00-c450d4811dae" />

### Мониторинг

Запускаем контейнеры с prometheus и grafana

<img width="1239" height="607" alt="image" src="https://github.com/user-attachments/assets/3de1608b-93e5-4640-a4e4-463e976cc500" />

Запустил Grafana

<img width="1324" height="814" alt="image" src="https://github.com/user-attachments/assets/f3168851-c2d5-4047-b2bb-c489d0315e09" />

