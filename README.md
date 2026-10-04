# Ansible Роль: vector-role

[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![Ansible Role](https://img.shields.io/badge/ansible%20role-MindMaze74.vector--role-blue.svg)](https://galaxy.ansible.com/MindMaze74/vector-role)
[![GitHub tag](https://img.shields.io/github/tag/MindMaze74/vector-role.svg)](https://github.com/MindMaze74/vector-role/tags)

Роль устанавливает и настраивает агент [Vector](https://vector.dev) для сбора логов и отправки их в ClickHouse.
## Требования

- Ansible >= 2.10
- Доступ к репозиторию `yum.vector.dev` (для установки пакета Vector)

## Переменные роли

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Имя | Значение по умолчанию | Описание |
| --- | --- | --- |
| `vector_version` | `0.39.0` | Версия пакета Vector для установки. |
| `clickhouse_host` | `hostvars[groups['clickhouse'][0]]['ansible_host']` | IP-адрес или хост ClickHouse, куда Vector будет отправлять логи. |

## Пример использования

```yaml
- hosts: vector
  roles:
    - vector-role
```

## Зависимости
Нет.

## Лицензия
MIT

## Информация об авторе
Эта роль была создана в рамках домашнего задания по Ansible.
