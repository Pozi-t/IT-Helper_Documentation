---
title: Диаграмма использования
sidebar_position: 2
---
## Use Case

```plantuml
@startuml

actor "Сотрудник" as sot
actor "Система" as system
actor "Администратор" as adm
actor "IT-специалист" as spec

usecase "Получить уведомление" as UCamd1
usecase "Добавить пользователя" as UCamd2
usecase "Назначить исполняющего" as UCamd3
usecase "Посмотреть аналитику" as UCamd4
usecase "Посмотреть аналитику по отделу" as UCamd5
usecase "Посмотреть аналитику по сотруднику" as UCamd6

usecase "Выполнить заявку" as UCspec1

usecase "Войти в ЛК" as UCs1
usecase "Просмотреть свои заявки" as UCs2
usecase "Добавить коментарий" as UCs3
usecase "Создать заявку" as UCs6
usecase "Прикрепить файл" as UCs7
usecase "Принять заявку" as UCsys3

usecase "Присвоить статус заявке" as UCsys5

sot <|-- adm
sot <|-- spec

sot -- UCamd1
sot -- UCs6
sot -- UCs1
sot -- UCs2

UCs6 <-- UCs7: extend
UCs2 <-- UCs3: extend

system -- UCsys3
system -- UCsys5

adm -- UCamd2
adm -- UCamd3
adm -- UCamd4

UCamd4 --> UCamd5: include
UCamd4 --> UCamd6: include

spec -- UCspec1

@enduml
```

### Цель диаграммы

"Демонстрация взаимодействий между участниками системы и основными сценариями использования."

### Участники

1. **Название роли 1**: Краткое описание.  
2. **Название роли 2**: Краткое описание.  

### Основные сценарии

- **Название сценария 1**: Описание цели сценария.  
- **Название сценария 2**: Описание цели сценария.  

### Связи между сценариями

- **Extend:** Поясните, какие сценарии расширяются.  
- **Include:** Укажите, какие сценарии включаются в другие.  
