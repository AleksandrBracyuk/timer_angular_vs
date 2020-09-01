# timer_angular_vs
оболочка VS проект над таймером на Angular

=================

Запуск в Visual Studio 2019 происходит так:

1. в командной строке (-любой) переходим в папку ClienApp нашего проекта и выполняем: npm start
2. в Visual Studio 2019 в окне выбора проекта запуска (- вверху, выпадашка) вместо "IIS Express" выбрать имя проекта и запустить

Данный способ рекомендован в https://docs.microsoft.com/en-us/aspnet/core/client-side/spa/angular?view=aspnetcore-3.1&tabs=netcore-cli в подразделе: 
"Run "ng serve" independently" для ускорения компилляции изменений в коде Angular в работающий сайт при разработке.

Вообще то для запуска проекта созданного по шаблону достаточно в окне выбора проекта запуска (- вверху, выпадашка) вместо "IIS Express" выбрать имя проекта и запустить.
И все работает. 
Но в моем случае вылетает ошибка "The Angular CLI process did not start listening for requests within the timeout period of 50 seconds".
Она означает, что сборка заняла много времени и Angular CLI не стартовал за период в 50 секунд.

=================

Как создан:

1.В Visual Studio 2019 создаю проект с типом (название типа привожу примерно): NET.Core web-application по шаблону Angular.
2.В папке проекта ClienApp удаляю содержимое и выкладываю свой проект Angular, созданный с помощью angular CLI. 
3.Внесено изменение в способ запуска в режиме разработки:  https://docs.microsoft.com/en-us/aspnet/core/client-side/spa/angular?view=aspnetcore-3.1&tabs=netcore-cli в подразделе: "Run "ng serve" independently":
In your Startup class, replace the spa.UseAngularCliServer invocation with the following:
spa.UseProxyToSpaDevelopmentServer("http://localhost:4200");

Т.е. в папку ClientApp ложите любой проект Angular и запускаете. С самим проектом при этом можно работать из-под, например, VSCode и запустить его в терминале командой "npm start".
