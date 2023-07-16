# Ansible-Keymaster

Ansible-Keymaster - это проект Ansible, предназначенный для автоматизации процесса добавления и удаления SSH-ключей на хостах, указанных в инвентаре.

## Описание

Ansible-Keymaster решает задачу управления SSH-ключами в среде с множеством хостов. Этот проект облегчает процесс добавления и удаления SSH-ключей на всех ваших хостах, что упрощает управление доступом и повышает безопасность вашей инфраструктуры.

## Установка

1. Клонируйте этот репозиторий на вашу локальную машину.
2. Измените файл `inventory.yml.example`, указав детали вашего хоста, и переименуйте его в `inventory.yml`.
3. Обновите переменные в файле `vars/main.yml` в каждом каталоге роли, указав путь к вашим публичным ключам и имена пользователей.

## Использование

Запустите playbook с помощью следующих команд:

```shell
ansible-playbook -i inventory add_key.yml
ansible-playbook -i inventory remove_key.yml
```

## Структура проекта

```
Ansible-Keymaster/
├── roles/
│   ├── add_ssh_key/
│   │   ├── tasks/
│   │   │   └── main.yml
│   │   └── vars/
│   │       └── main.yml
│   └── remove_ssh_key/
│       ├── tasks/
│       │   └── main.yml
│       └── vars/
│           └── main.yml
├── add_key.yml
├── ansible.cfg
├── inventory.yml.example
├── remove_key.yml
├── README.md
└── LICENSE
```

## Лицензия

Этот проект распространяется под лицензией MIT. Подробности можно узнать в файле LICENSE.
