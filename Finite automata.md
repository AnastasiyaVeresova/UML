Конечные автоматы Постройте конечный автомат по работе с состояниями датчиков для города Х. Кейс прикреплен в материалах к семинару 1\.

1. Составление таблицы переходов состояний.

●	Начальное состояние. Датчики в режиме ожидания. ●	Датчик обнаруживает дым. ●	Датчик обнаруживает подъем температуры. ●	Датчик отправляет оповещение о пожаре в центр управления. ●	Центр управления принимает оповещение ●	Центр управления связывается с пользователем. ●	Центр управления не подтверждает пожар, после связи с пользователем. ●	Центр управления подтверждает пожар после связи с пользователем. ●	Центр управления передает оповещение в пожарную часть. ●	Центр управления передает оповещения зарегистрированным пользователям. ●	Получения оповещения о пожаре пожарной частью. ●	Пожарная часть приняла меры.

### **Таблица переходов состояний:**

| Текущее состояние | Событие | Следующее состояние |
| ----- | ----- | ----- |
| Ожидание | Датчик обнаруживает дым | Обнаружение дыма |
| Ожидание | Датчик обнаруживает подъем температуры | Обнаружение подъема температуры |
| Обнаружение дыма | Датчик отправляет оповещение о пожаре в центр управления | Ожидание подтверждения |
| Обнаружение подъема температуры | Датчик отправляет оповещение о пожаре в центр управления | Ожидание подтверждения |
| Ожидание подтверждения | Центр управления принимает оповещение | Проверка оповещения |
| Проверка оповещения | Центр управления связывается с пользователем | Ожидание подтверждения от пользователя |
| Ожидание подтверждения от пользователя | Центр управления не подтверждает пожар | Ожидание |
| Ожидание подтверждения от пользователя | Центр управления подтверждает пожар | Подтверждение пожара |
| Подтверждение пожара | Центр управления передает оповещение в пожарную часть | Ожидание реакции пожарной части |
| Подтверждение пожара | Центр управления передает оповещения зарегистрированным пользователям | Ожидание реакции пользователей |
| Ожидание реакции пожарной части | Получение оповещения о пожаре пожарной частью | Ожидание мер пожарной части |
| Ожидание мер пожарной части | Пожарная часть приняла меры | Ожидание |

![диаграмма][2.png]