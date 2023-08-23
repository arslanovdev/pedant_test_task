# Тестовое задание на позицию Middle Frontend Developer
## Личный кабинет с авторизации OTP

Использовать стек Vite, Vue 3 (Composition api), TypeScript. Допустимо использование любых библиотек и препроцессоров. Внешний вид и верстка не принципиальны, 
будем обращать внимание на организацию кода.

Доступ к документации и api будет предоставлен лично.

Необходимо реализовать авторизацию в личный кабинет с помощью одноразового четырехзначного OTP-кода. Использовать наше api: https://account-test.pedant.market/...method.

**Первый этап**. После ввода номера телефона должен производиться запрос к методу [generate-otp](https://account-test.pedant.market/request-docs#POSTapi/generate-otp). 
Метод отправит одноразовый код клиент по СМС.

<img width="400" src="/assets/first-stage.png">

**Второй этап**. После ввода кода, должна проводиться проверка с помощью [verify-otp](https://account-test.pedant.market/request-docs#POSTapi/verify-otp).
Если код верный, метод вернет токен, с которым можно пускать в личный кабинет, иначе выводить соответствующую ошибку в форме.

<img width="400" src="/assets/second-stage.png">

**Третий этап**. Отобразить ФИО и номер телефона пользователя, используя данные, полученные с помощью метода [subscription](https://account-test.pedant.market/request-docs#GETapi/subscriptions).

<img width="400" src="/assets/third-stage.png">

