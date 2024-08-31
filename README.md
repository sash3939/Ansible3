# Домашнее задание к занятию 3 «Использование Ansible»

## Подготовка к выполнению

1. Подготовьте в Yandex Cloud три хоста: для `clickhouse`, для `vector` и для `lighthouse`.

   <img width="984" alt="Screen1" src="https://github.com/user-attachments/assets/27c265dc-e0b7-46d3-9f5e-a22217c3f70d">

3. Репозиторий LightHouse находится [по ссылке](https://github.com/VKCOM/lighthouse).

## Основная часть

1. Допишите playbook: нужно сделать ещё один play, который устанавливает и настраивает LightHouse.
2. При создании tasks рекомендую использовать модули: `get_url`, `template`, `yum`, `apt`.
3. Tasks должны: скачать статику LightHouse, установить Nginx или любой другой веб-сервер, настроить его конфиг для открытия LightHouse, запустить веб-сервер.
Запущенный сервис nginx на Lighthouse
<img width="608" alt="nginx" src="https://github.com/user-attachments/assets/3379c567-0cbb-48f4-8727-e03e863d293d">

Web-интерфейс Lighthouse
<img width="1218" alt="Lighthouse" src="https://github.com/user-attachments/assets/526aec84-f6d9-4c2a-bbc9-1f3f73ae6b36">

4. Подготовьте свой inventory-файл `prod.yml`.

Добавляем таску с параметрами соединения к Lighthouse, и IP адресом ВМ в ЯО
<img width="584" alt="Screen4" src="https://github.com/user-attachments/assets/566b6e9c-5b43-4747-8ac2-47fc54204333">

5. Запустите `ansible-lint site.yml` и исправьте ошибки, если они есть

Проверка на ошибки
   
<img width="528" alt="Screen5" src="https://github.com/user-attachments/assets/84a4acdc-77c3-4c6a-bf7c-e8227a3ead22">
   
6. Попробуйте запустить playbook на этом окружении с флагом `--check`.

<img width="916" alt="Screen6" src="https://github.com/user-attachments/assets/08869fcb-3f5d-4eac-9642-237df14c397d">

7. Запустите playbook на `prod.yml` окружении с флагом `--diff`. Убедитесь, что изменения на системе произведены.

<img width="897" alt="Screen7" src="https://github.com/user-attachments/assets/743cb0d5-2e94-4905-9cfe-5e42b6814911">

8. Повторно запустите playbook с флагом `--diff` и убедитесь, что playbook идемпотентен.

<img width="897" alt="Screen8" src="https://github.com/user-attachments/assets/d3da0ca3-3009-45df-a891-492c10dbaccf">
    
9. Подготовьте README.md-файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги.
10. Готовый playbook выложите в свой репозиторий, поставьте тег `08-ansible-03-yandex` на фиксирующий коммит, в ответ предоставьте ссылку на него.

---

