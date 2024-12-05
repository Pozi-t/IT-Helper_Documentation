---
title: Функциональные требования
sidebar_position: 1
---

# Функциональные и нефункциональные требования

## 1. Функциональные требования

### Use Case 1: Отправка заявки через веб-интерфейс

**Цель:** Обеспечить возможность сотрудникам отправлять заявки на техническую поддержку через веб-интерфейс.

**Участники:**  
- Сотрудник  
- Система управления IT-обслуживанием  

**Предусловия:** Сотрудник зарегистрирован в системе и авторизован.

**Основной сценарий:**  
1. Сотрудник входит в систему через веб-интерфейс.  
2. В личном кабинете нажимает на кнопку "Создать заявку".  
3. Система отображает форму для создания заявки.  
4. Сотрудник заполняет поля (описание проблемы, категория и приоритет).  
5. Нажимает "Отправить".  
6. Система сохраняет заявку в базу данных и присваивает ей статус "Ожидание обработки".  
7. Система отображает сообщение об успешной отправке заявки.

**Постусловие:** Заявка успешно создана и видна в разделе "Мои заявки" с текущим статусом.

**Приоритет:** Высокий  
**Обоснование:** Это ключевая функциональность, без которой система не сможет выполнять основную задачу — обработку заявок.

---

### Use Case 2: Базовое отслеживание статусов заявок

**Цель:** Позволить сотрудникам отслеживать статус своих заявок.

**Участники:**  
- Сотрудник  
- Система управления IT-обслуживанием  

**Предусловия:** Сотрудник должен быть авторизован в системе и иметь созданные заявки.

**Основной сценарий:**  
1. Сотрудник входит в систему и переходит в раздел "Мои заявки".  
2. Система отображает список всех заявок сотрудника с текущим статусом (Ожидание обработки, В работе, Завершено).  
3. При клике на конкретную заявку отображаются её детали и история изменений статусов.

**Постусловие:** Сотрудник видит актуальный статус каждой своей заявки.

**Приоритет:** Средний  
**Обоснование:** Функциональность отслеживания важна для прозрачности работы системы и информирования сотрудников о ходе выполнения их заявок.

---

### Use Case 3: Распределение задач между IT-специалистами вручную

**Цель:** Обеспечить возможность администратору вручную распределять заявки между IT-специалистами.

**Участники:**  
- Администратор  
- Система управления IT-обслуживанием  
- IT-специалисты  

**Предусловия:** В системе есть нераспределённые заявки и IT-специалисты.

**Основной сценарий:**  
1. Администратор входит в систему и переходит в раздел "Заявки".  
2. Система отображает список всех заявок со статусом "Ожидание обработки".  
3. Администратор выбирает заявку и назначает её на конкретного IT-специалиста.  
4. Система обновляет статус заявки на "В работе" и информирует назначенного IT-специалиста.

**Постусловие:** Заявка назначена IT-специалисту, и он уведомлён.

**Приоритет:** Высокий  
**Обоснование:** Ручное распределение задач необходимо для администрирования и эффективного управления рабочей нагрузкой.

---

### Use Case 4: Простейшая аналитика по заявкам

**Цель:** Позволить администратору видеть основную статистику по заявкам (количество открытых и решённых заявок).

**Участники:**  
- Администратор  
- Система управления IT-обслуживанием  

**Предусловия:** В системе есть заявки в различных статусах.

**Основной сценарий:**  
1. Администратор входит в систему и переходит в раздел "Аналитика".  
2. Система отображает количество открытых и завершённых заявок в виде простого отчёта.

**Постусловие:** Администратор видит основную статистику по заявкам.

**Приоритет:** Низкий  
**Обоснование:** Аналитика важна, но на начальном этапе можно ограничиться простейшими отчётами для общего мониторинга.

---

### Use Case 5: Базовые уведомления для сотрудников и IT-специалистов

**Цель:** Уведомить сотрудников и IT-специалистов о событиях, связанных с заявками (например, о принятии заявки в работу или её завершении).

**Участники:**  
- Сотрудник  
- IT-специалист  
- Система управления IT-обслуживанием  

**Предусловия:** В системе есть заявки, которые меняют статус.

**Основной сценарий:**  
1. Сотрудник создаёт заявку — система отправляет уведомление о том, что заявка успешно принята.  
2. IT-специалист принимает заявку в работу — система отправляет уведомление сотруднику.  
3. По завершении работы IT-специалист завершает заявку — система уведомляет об этом сотрудника.

**Постусловие:** Сотрудники и IT-специалисты своевременно получают уведомления о статусах заявок.

**Приоритет:** Средний  
**Обоснование:** Уведомления позволяют оперативно информировать пользователей, улучшая их взаимодействие с системой.