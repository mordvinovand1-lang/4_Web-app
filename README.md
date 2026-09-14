# 4_Web-app
Веб-приложение для управления турами (страны и отели)
Веб-приложение для просмотра списка стран и отелей в выбранной стране. Тема приложения продолжает тему задания N3 Проект создан в рамках учебной практики в университете Синергия с использованием ASP.NET Core (бэкенд) и React (фронтенд).
Технологии и инструменты
Бэкенд
ASP.NET Core Web API
Entity Framework Core
PostgreSQL
pgAdmin
Фронтенд
React
Vite
Tailwind CSS
Инструменты
Visual Studio Code
npm
1. Настройка базы данных
Установите PostgreSQL и создайте базу данных tours_asp.
В файле appsettings.json (tourism_aspnet(development)) укажите строку подключения
"ConnectionStrings": {
  "DefaultConnection": "Host=localhost;Port=5432;Database=tours_asp;Username=ваш_пользователь;Password=ваш_пароль"
}
Примените миграции EF Core:
dotnet ef database update
2. Запуск бэкенда
Перейдите в папку tourism_aspnet
cd tourism_aspnet
dotnet run
сервер запустится на http://localhost:5142
3. Запуск фронтенда
Перейдите в папку tourismAPP
cd ..
cd tourismAPP
npm run dev
приложение будет доступно на http://localhost:5173
Структура проекта
Бэкенд (ASP.NET Core)
Модели:
Country (Страна: Id, Name, Visa)
Hotel (Отель: Id, Name, CountryId)
Контроллеры:
CountriesController (GET /countries)
HotelsController (GET /hotels/{countryId})
Фронтенд (React)
Главная страница отображает список стран.
При выборе страны отправляется запрос к API для получения отелей.
Скриншоты
Интерфейс приложения
Скриншоты
Интерфейс приложения
china

<img width="566" height="392" alt="china_hotels" src="https://github.com/user-attachments/assets/4cfa0e77-0ff2-4217-92c0-3e530b24f863" />

Рисунок 1: Список отелей в Китае
china

<img width="566" height="392" alt="thai_hotels" src="https://github.com/user-attachments/assets/1be47661-da91-4deb-80ed-05311d76f098" />

Рисунок 2: Список отелей в Таиланде


База данных
<img width="1020" height="715" alt="pgAdmin" src="https://github.com/user-attachments/assets/8d40a22e-d4da-4b85-8a69-576fd7be61c7" />
Рисунок 3: Структура базы данных в pgAdmin

Запуск проекта
<img width="1212" height="507" alt="api_succ" src="https://github.com/user-attachments/assets/6a566dd7-77fc-45b5-8132-3ba77d68c176" />
Рисунок 4: Бэкенд успешно запущен

<img width="1198" height="221" alt="react_succ" src="https://github.com/user-attachments/assets/8dd4b758-2ef1-47aa-b55c-748121888414" />
Рисунок 5: Фронтенд собран и готов к работе




