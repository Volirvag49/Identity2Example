# Тестовое задание (.Net) 
### Задание: 
Необходимо написать веб-приложение для регистрации и аутентификации пользователей. Требования к функциональности: 

• Форма логина на сайт

 • Регистрация пользователя
 
 • Форма восстановления пароля
 
 • После логина пользователь должен попадать на персональную страницу, которая доступна только ему 
 
• Пользователь должен иметь возможность изменять данные о себе

 • Необходимо высылать пользователю e-mail для: подтверждения регистрации, восстановления пароля 
 
### Обязательные требования к реализации:  

• Использовать С#

 • Использовать СУБД на Ваше усмотрение
 
 • Использовать ООП принципы 
 
• Соблюдение MVC Паттерна

• Все настройки должны храниться в одном файле

 • Проверки всех форм должны быть выполнены и на клиентской стороне (JavaScript) и на серверной (С#) 
 
• Приложение должно иметь расширяемую структуру, чтобы добавление какого-то модуля не вызывало проблем
# Настройки
### Настройка почтового сервиса

Укажите в файле `web.config` в секции `<appSettings>` данные используемого почтового сервиса.
 Пример:
 ```html
     <add key="mailLogin" value="fakemail@yandex.ru" /> <!--Логин отправителя (мэйл)-->
     <add key="mailpass" value="fakepassword" /> <!--Пароль отправителя-->
     <add key="smtpServer" value="smtp.yandex.ru" /> <!--Адрес smtp-сервера-->
     <add key="smtpPort" value="25" /> <!--Порт smtp-сервера-->
```
