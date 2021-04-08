# Vas9ka.github.io
Веб-сайт, показывающий погоду в данной геолокации и в любом городе.
* Лабораторная работа 1:  
Сверстать сайт с отображением информации о погоде в соответствии с макетами. Отображение сайта должно гибко адаптироваться при изменении ширины – для примера даны макеты для desktop и mobile. Иконки погоды на макетах сделаны заглушками, замените их на свои. Цветовая схема, шрифты могут отличаться от макета, но общая сетка страницы должна быть соблюдена. В верстке должна соблюдаться семантика.
* Лабораторная работа 2:  
Доработать лабораторную работу 1 для работы с внешним API, позволяющим получить данные о погоде в городе.
При первой загрузке страницы происходит запрос пользователя на получение данных о геолокации с использованием HTML5 Geolocation API. Если пользователь соглашается предоставить данные о геолокации – получаем из внешнего API данные о погоде (API можно выбрать самостоятельно). Если нет – запрашиваем информацию для города по умолчанию (город по умолчанию можно выбрать самостоятельно). Эти сведения отображаются в верхней части страницы – "Погода здесь". Иконка погоды должна соответствовать тем данным о погоде, что были получены из API.
У пользователя есть возможность добавления и удаления городов в избранное. Информация о погоде отображается для всех городов из избранного в соответствии с макетом и реализацией первой лабораторной работы (секция "Избранное"). Список избранных городов сохраняется в LocalStorage. Сами данные о погоде в LocalStorage сохранять не нужно – запрос актуальных сведений происходит при каждой загрузке страницы.
* Лабораторная работа 3:  
Необходимо доработать лабораторную работу №2, добавив реализацию серверной части приложения. Серверная часть реализуется на NodeJS, допустимо использовать фреймворки вроде Express или Sails.  
Приложение в этой работе становится клиент-серверным, запросы данных о погоде к внешнему API и хранение данных об избранных городах переносятся на сервер. Запросы с клиента отправляются только к самостоятельно реализованной серверной части. 
Для получения данных о погоде из внешнего API по городу используется запрос на GET-endpoint /weather/city (например: /weather/city?q=Moscow), по координатам – /weather/coordinates (например: /weather/coordinates?lat=123&long=456). Если город не найден, должен возвращаться соответствующий ответ с 404 статусом.  
Данные об избранных городах хранятся в базе данных, можно использовать любое SQL/NoSQL решение. Для работы с избранными городами на сервере должен быть реализован endpoint /favourites, обрабатывающий POST-запросы на добавление города и DELETE-запросы на удаление конкретного города из списка. GET-запрос на /favourites возвращает список избранных городов.
