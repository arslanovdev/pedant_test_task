# Тестовое задание на позицию Middle Frontend Developer
## Личный кабинет с авторизации OTP

Использовать стек Vite, Vue 3 (Composition api), TypeScript. Допустимо использование любых библиотек и препроцессоров. Внешний вид и верстка не принципиальны, 
будем обращать внимание на организацию кода.

Доступ к документации и api будет предоставлен лично.

Необходимо реализовать авторизацию в личный кабинет с помощью одноразового четырехзначного OTP-кода. Использовать наше api: https://account-test.pedant.market/...method.

**Первый этап**. После ввода номера телефона должен производиться запрос к методу [generate-otp](https://account-test.pedant.market/request-docs#POSTapi/generate-otp). 
Метод отправит одноразовый код клиент по СМС.

<img width="445" alt="image" src="https://github.com/arslanovdev/pedant_test_task/assets/70380449/74136a6e-0e68-4e6c-a95e-d26696a66976">

**Второй этап**. После ввода кода, должна проводиться проверка с помощью [verify-otp](https://account-test.pedant.market/request-docs#POSTapi/verify-otp).
Если код верный, метод вернет токен, с которым можно пускать в личный кабинет, иначе выводить соответствующую ошибку в форме.

<img width="388" alt="image" src="https://github.com/arslanovdev/pedant_test_task/assets/70380449/78c1dc7e-6819-4234-b23a-6bf07b55bb4b">

**Третий этап**. Отобразить ФИО и номер телефона пользователя, используя данные, полученные с помощью метода [subscription](https://account-test.pedant.market/request-docs#GETapi/subscriptions).

<img width="503" alt="image" src="https://github.com/arslanovdev/pedant_test_task/assets/70380449/f24c297b-89d4-4857-be0a-6b4989e81554">

