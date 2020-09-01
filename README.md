# timer_angular_vs
оболочка VS проект над таймером на Angular

=================
Создание:
1.В Visual Studio 2019 Создаю проект с типом (название типа привожу примерно): NET.Core web-application по шаблону Angular.
2.В папке ClienApp удаляю содержимое и выкладываю свой проект Angular, созданный с помощью angular CLI. 

Запуск:
Для запуска проекта созданного по шаблону достаточно в окне выбора проекта запуска (- вверху, выпадашка) вместо "IIS Express" выбрать имя проекта и запустить.
И все работает. Но в моем случае вылетает ошибка "The Angular CLI process did not start listening for requests within the timeout period of 50 seconds".
Она означает, что сборка заняла много времени и Angular CLI не стартовал за период в 50 секунд.

Поэтому запуск в Visual Studio 2019 происходит так:

1. в командной строке (-любой) переходим в папку ClienApp нашего проектаи и выполняем: npm start
2. в окне выбора проекта запуска (- вверху, выпадашка) вместо "IIS Express" выбрать имя проекта и запустить

Данный способ рекомендован в https://docs.microsoft.com/en-us/aspnet/core/client-side/spa/angular?view=aspnetcore-3.1&tabs=netcore-cli
"Run "ng serve" independently".


