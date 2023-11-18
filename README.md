Description:
The idea behind this small proejct is address browsing service. 
So it is simple web page that has form inside it.
Type a part of address in input area and then click 'Search' button.
The results will pop out below.

frontend: vuetify-vue 
request: fetch-api
adaptive 2 mods: strech tab if window width less than 768px, show background and tab in cente
if width is greater than 768px.
api key is stored in .env file VITE_API_KEY=******

Install guide:
1) install nodejs and npm cli
2) git clone https://github.com/atmosphere1337/vue_spa_fetch_resp.git
3) go to vue_spa_fetch_resp
4) open cmd in this directory and run:    npm install
5) Go to https://dadata.ru/profile/#info  ,sign up and get api_key in profile.
5) create .env file in this directory (if it doesn't exist) and put the line: VITE_API_KEY=****** 
where ****** is api key. 
6) run command in cmd: npm run dev 
7) open new tab in browser http://localhost:3000

Описание:
Проект представляет собой браузинг адресов.
Пользователь попадает на страницу, в котором есть форма отправки данных.
Введите часть адреса в поле ввода, нажмите кнопку "Search".
Результат выведется ниже.

frontend: vuetify-vue 
request: fetch-api
adaptive 2 mods: растягивает на весь экран форму если ширина дисплея ниже 768px, показывает также и фон и центрирует форму посередине если ширина дисплея выше 768px.
api ключ хранится в  .env файле VITE_API_KEY=******

Установка:
1) установите nodejs и npm cli
2) git clone https://github.com/atmosphere1337/vue_spa_fetch_resp.git
3) перейдите в папку vue_spa_fetch_resp
4) откройте коммандную строку в этой директории и запустите:    npm install
5) перейдите по ссылке  https://dadata.ru/profile/#info  зарегистрируйтесь и получите ключ api в личном кабинете.
5) создайте .env файл в этой директории (если он не создан ранее) и вставьте строку: VITE_API_KEY=****** 
где ****** где api ключ. 
6) запустите команду в командной строке: npm run dev 
7) перейдите по адресу http://localhost:3000
