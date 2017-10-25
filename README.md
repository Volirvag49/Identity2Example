# Identity2Example
Можно протестировать тут http://identity2example.azurewebsites.net

# Настройки
### 1. Настройка почтового сервиса

Укажите в файле `web.config` в секции `<appSettings>` данные используемого почтового сервиса.

 Пример:
 ```html
     <add key="mailLogin" value="fakelogin@azure.com" /> <!--Логин отправителя (мэйл)-->
     <add key="mailpass" value="fakepassword" /> <!--Пароль отправителя-->
     <add key="smtpServer" value="smtp.yandex.ru" /> <!--Адрес smtp-сервера-->
     <add key="smtpPort" value="25" /> <!--Порт smtp-сервера-->
```
### 2. Настройка подтверждения телефона

Укажите в файле `web.config` в секции `<appSettings>` данные используемого смс сервиса.

 Пример:
 ```html
      <!--Настройка SmsService-->
    <add key="accountSid" value="fakesid" /><!-- sid акаунта-->
    <add key="authToken" value="faketoken" /><!--Ключ-->
    <add key="twilioPhoneNumber" value="fakephonenumber" /><!--twilio номер-->
```
 В  GET-методе `VerifyPhoneNumber`контроллера `Manage` не забыть убрать строчку 
 "`ViewBag.Code = code;`" тоже самое для его представления "`Ваш код будет: @ViewBag.Code (Для теста)`"
 Данный `ViewBag.Code` отображает код, который будет отправлен по смс пользователю исключительно для теста.
### 3. Администратор по умолчанию

Укажите в файле `web.config` в секции `<appSettings>` логин, пароль и мэйл администратора по умолчанию.

 Пример:
 ```html
 <!--Настройка Администратора.-->
    <!--Если данные не соответствуют условиям, то пользователь не создаётся-->
     <!--Если пользователь уже существует, но данные изменены то данные старого пользователя изменяются-->
    <add key="adminLogin" value="Admin1" /><!--Логин администратора (Должен быть не менее 6 символов)-->
    <add key="adminPass" value="Admin1" /><!--Пароль администратора (Должен быть не менее  6 символов)-->
    <add key="adminMail" value="AdminMail@gmail.com" /><!--Почта администратора (Должна быть не менее  6 символов)-->
```
В отличии от обычных пользователей администратору по умолчанию не надо подтверждать мэйл.
Функцию добавления администратора и ролей по умолчанию можно отключить, закоментив в методе `Configuration` вызов метода  `CreateRolesandUsers();`

