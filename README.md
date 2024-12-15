Задание №1
0. Вводная
В ходе выполнения задания выполнен первый и вторый необходимый уровень для сдачи.
1. Проектирование
- Приложение было принято разделить на микрофронтеды для повышения масштабируемости кода, отказоустойчивости и гибкого управления;
- Разделение было выполнение с использованием вертикальной нарезки и разделения на домены (DDD);
- В качестве выбранной технологии для разделения на микрофронтенды был использован Webpack Module Federation, так как приложение использует только один фреймворк на базе React и не планируется использование других фреймворков.
2. Планирование изменений
Микрофронтенды были разделены следующим образом:
- host 
Микрофронтед - главное приложение, которое отвечает за координирование и связку работы с остальными микрофронтендами. 
Были вынесены следующие функции из главного приложения:
	- Header
	- Footer
- auth-microfrontend. 
Микрофронтенд отвечает за идентификацию, аутентификацию и авторизацию пользователей. Следовательно, весь функционал, связанный с управлением этим процессом, был вынесен в отдельный микрофронтенд.
Были вынесены следующие функции из главного приложения:
	- Login
	- Register
- profile-microfrontend.
Микрофронтенд отвечает за редактирование информации в профиле пользователя. Поэтому, весь функционал, связанный с внесением изменений в профиль пользователя, был вынесен в отдельный микрофронтенд.
Были вынесены следующие функции из главного приложения:
	- EditAvatarPopup 
	- EditProfilePopup
	- InfoToolTip
- cardsfunc-microfrontend
Микрофронтенд отвечате за основную функциональность приложения - сбор и учет лайков под фото. В связи с этим, данный функционал был вынесен в отдельный микрофронтенд.
Были вынесены следующие функции из главного приложения:
	- AddPlacePopup
	- Card
	- ImagePopup
