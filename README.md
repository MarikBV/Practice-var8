# Practice
 
## Вариант 8 
	
### Задачи
 * Описание проекта, построение схемы взаимодействия компонентов системы и поднятие ИС. 
 * Работа с БДУ ФСТЭК, построение модели угроз 
 * Разработка сценариев с матрицей Mitre ATT&CK
 * Работа с БДУ ФСТЭК, построение модели нарушителя ИБ 

### Описание проекта:
#### Решаемые бизнес-процессы:
1. Создание и Управление Контентом: Flatpress предназначен для создания блогов и управления контентом. Это позволяет бизнесу поддерживать актуальные новости, обновления и другую информацию на своем веб-сайте.
2. Взаимодействие с Посетителями: Посредством комментариев и обратной связи Flatpress обеспечивает взаимодействие с посетителями блога, что может быть важным элементом коммуникации для бизнеса.
#### Роли пользователей и варианты доступа:
1. Автор блога: Основные создатели контента. Они публикуют посты, редактируют их, добавляют изображения и управляют контентом блога. Не имеют доступа к функциям управления пользователями и другими настройками блога.
2. Администратор блога: Это самый высокий уровень доступа, который даёт полный контроль над всеми аспектами блога, включая управление пользователями, настройку и публикацию контента, управление плагинами и темами, а также управление настройками безопасности.
3. Модераторы: Эти пользователи могут управлять комментариями, одобряя или отклоняя их, а также удаляя спам. Модераторы могут редактировать или удалять учетные записи пользователей, управлять их правами доступа. Могут удалять или редактировать контент, созданный другими пользователями, чтобы обеспечивать соответствие правилам и политике сайта.
4. Пользователь:  Этот уровень доступа обычно позволяет только комментировать посты и страницы блога. Пользователи могут оставлять комментарии, но не могут создавать или редактировать контент. Могут подписываться на обновления блога, получая уведомления о новых записях.
5. Гости: Посетители блога, которые могут читать записи и оставлять комментарии (если это разрешено администратором). Обычно у них нет возможности оставлять комментарии или выполнять другие действия.
6. Редактор: Этот пользователь имеет права на редактирование и публикацию контента блога, но не имеет полного административного доступа. Он может управлять постами и страницами.
7. Дизайнеры: Ответственные за кастомизацию внешнего вида блога, изменение тем и стилей. Они могут создавать и редактировать шаблоны и стили, разрабатывать собственные темы для сайта, что позволяет владельцам сайта выбирать разные дизайны для своих страниц. Дизайнеры могут вносить изменения в HTML, CSS и JavaScript код сайта, чтобы улучшить его производительность и функциональность. Права дизайнеров могут быть настроены администратором или владельцем сайта, и они могут варьироваться в зависимости от конкретной роли пользователя. 
8. Техническая поддержка: Пользователи, которые могут помогать другим пользователям с техническими вопросами, такими как проблемы с настройкой или ошибками. Поддержка может предоставлять советы и помощь по установке, настройке и использованию плагинов и тем для FlatPress. Права этих пользователей могут варьироваться в зависимости от конкретной ситуации и политики разработчиков или владельцев веб-сайта.
#### Структурные элементы системы: 
1.	Сервера системного программного обеспечения (СПО):
*   Веб-сервер (Apache) - отвечает за обработку запросов и предоставление веб-страниц пользователю.
*	Базы данных (MySQL/ SQLite) - хранят информацию о блоге, пользователях, комментариях и других данных.
*	Веб-браузеры - позволяют пользователям просматривать и взаимодействовать с блогом.
2.	Приложения:
*	FlatPress - является центральным приложением и представляет собой движок для ведения блога. Он предоставляет интерфейс для создания, редактирования и отображения записей, управления пользовательскими аккаунтами и другими параметрами блога.
3.	СУБД (Система управления базами данных):
*	FlatPress поддерживает работу с различными СУБД, такими как MySQL или SQLite. СУБД отвечает за хранение и управление данными, используемыми FlatPress.
4.	Прикладное программное обеспечение (ППО):
*	Редакторы контента - позволяют пользователям создавать и редактировать посты блога.
*	Различные плагины и темы - FlatPress поддерживает расширяемость с помощью плагинов и тем, которые позволяют добавлять новые функции и изменять внешний вид блога.

#### Взаимодействие структурных элементов:
1.	Когда пользователь заходит на блог, его запрос обрабатывается веб-сервером.
2.	Веб-сервер передает запрос в FlatPress, который обращается к СУБД для получения необходимой информации о блоге.
3.	При получении данных от СУБД, FlatPress генерирует HTML-страницу с содержимым блога. Сгенерированная страница отправляется обратно веб-серверу.
4.	Веб-сервер отвечает на запрос пользователя и отправляет HTML-страницу обратно веб-браузеру.
5.	Веб-браузер отображает страницу пользователю и позволяет взаимодействовать с блогом (например, комментировать записи или создавать новые).
   ![image](https://github.com/MarikBV/Practice-var8/assets/126908924/c3e50a73-272b-493e-9b79-51a1ecf6a93b)

#### Информация о ЦОД:
Информация о Центре Обработки Данных (ЦОД) зависит от того, где размещен сервер с установленным Flatpress. Это может быть внутренний сервер компании или хостинг-провайдер с соответствующей инфраструктурой и мерами безопасности.
Интеграция Flatpress и использование могут быть адаптированы в соответствии с потребностями бизнес-процессов и требований безопасности.

### Описание условного места установки системы: 
#### Частная фирма. 
Система Flatpress, как генератор блогов, может быть установлена в небольшой частной фирме, занимающейся производством и продажей украшений ручной работы.

В этой фирме система Flatpress используется для ведения корпоративного блога, где публикуются статьи о процессе создания продукции, творческом процессе, историях успеха и вдохновении.

Можно выделить следующие категории информации, которые обрабатываются системой :
* Общедоступная информация: Блог может содержать общедоступные статьи о методах работы, процессе создания продукции, обзоры новых товаров, истории успеха компании. Это доступно для всех посетителей сайта.
* Персональные данные: В случае, если в блоге размещаются интервью или истории сотрудников, их фотографии, имена или иные личные данные. Эта информация может быть рассмотрена как персональные данные.
* Коммерческая тайна: Хотя большая часть информации в блоге будет общедоступной, уникальные методы работы или информация о поставщиках, которая не предназначена для публичного распространения, могут быть рассмотрены как коммерческая тайна. При невнимательном отношении к публикуемой информации, могут быть раскрыты персональные данные сотрудников или конфиденциальные детали производства.


