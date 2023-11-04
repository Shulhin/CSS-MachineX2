<p>
	<img src="https://raw.githubusercontent.com/Shulhin/CSS-MachineX/master/app/assets/img/preview.jpg" alt="CSS-MachineX">
</p>
<h2>Обновлено!</h2>
<ul>
	<li>Подключение скриптов теперь в <strong>head</strong>, с использованием <strong>defer</strong></li>
	<li>Хєширование файлов теперь не удаляет <strong>defer</strong>, используем <strong>cache_bust=NUMBERS</strong></li>
	<li>Чтобы не было ошибок, используем плагин <strong>del</strong> версии не выше <strong>6.1.1</strong> и плагин <strong>gulp-imagemin</strong> версии не выше <strong>7.1.0</strong></li>
</ul>

<h2>Начать</h2>
<pre>git clone https://github.com/Shulhin/CSS-MachineX2.git .; rm -rf .gitignore readme.md .git</pre>
<p>Установить значение <strong>gmWatch = false</strong>, если не установлен в систему <strong>graphicsmagick</strong>.</p>
<p>Переименовать файл ht.access в .htaccess</p>

<h2>О сборке</h2>
<p>В сборку включена живая перезагрузка (на <strong>localhost</strong>), <strong>Babel</strong> и <strong>Webpack</strong> для модульности. <strong>JQuery</strong> подключено через <strong>CDN</strong>, при желании можно убрать.</p>
<h3>Что выполняет таскер:</h3>
<ul>
	<li>Добавляет префиксы для стилей</li>
	<li>Сжимает картинки благодаря graphicsmagick</li>
	<li>Включены sourcemaps в режиме работы над проектом</li>
	<li>Собирает sass стили и js скрипты, сжимает их в единый файл</li>
	<li>Объединяет media запросы воедино при сборке проекта</li>
	<li>Добавляет к файлам main.min.css и app.js "? + число" для обновления кэша на стороне клиента при выгрузке проекта на хостинг</li>
</ul>

<h2>Структура проекта</h2>
<p>
	<img src="https://raw.githubusercontent.com/Shulhin/CSS-MachineX/master/app/assets/img/architecture.jpg" alt="Структура проекта">
</p>

<h3>Архитектура стилей <strong>src/sass</strong></h3>
<ul>
	<li><strong>/modules</strong> - папка с версткой отдельных блоков, компонентов или страниц</li>
	<li><strong>mixins.sass</strong> - Миксины для генерации относительных значений в резиновом дизайне. Я часто использую их в работе, но если макет того не требует - можно удалить.</li>
	<li><strong>variables.sass</strong> - Переменные проекта</li>
	<li><strong>fonts.sass</strong> - Подключение шрифтов и шрифтовых иконок вынес в отдельный файл. Можно удалить, если в работе не используются шрифтовые иконки и шрифты подключаются через <strong>Google Fonts</strong>.</li>
	<li><strong>main.sass</strong> - основной файл стилей, где подключаем все стили необходимые для проекта.</li>
</ul>
<p>файл <strong>ht.access</strong> содержит в себе настройки для кэширования файлов на стороне сервера для быстрой загрузки и лучших показателей <strong>Pagespeed</strong>.</p>

<h2>Основные команды</h2>
<ul>
	<li><strong>gulp</strong> - запуск проекта.</li>
	<li><strong>gulp speedDev</strong> - запуск проекта без автопрефикса, более шустрей работает, если очень много исходных файлов стилей.</li>
	<li><strong>gulp build</strong> - финальная сборка проекта.</li>
	<li><strong>npm run update</strong> - установка всех пакетов связанных с проектом.</li>
	<li><strong>npm run clean</strong> - удаление папки node_modules.</li>
</ul>

<h2>Важно! Правила использования сборки в написании стилей</h2>
<p>В сборке используется <strong>mqpacker</strong> - он собирает все медиазапросы в один. Если у Вас используются один подход к написанию стилей, т.к. и должно быть - <strong>mobile first</strong> или <strong>desktop first</strong>, то проблем не возникнет и оно удачно все упакует.<br> Но если у Вас будут использоваться различные медиазапросы - от мобильника, от десктопа и со смежными значениями на один и тот же класс, тогда могут появляться баги при сборке проекта. Стоит учитывать эту деталь при написании стилей.</p>

<h2>Полезные сервисы</h2>
<p><a href="https://realfavicongenerator.net/" target="_blank">Создание и добавление favicon</a></p>
<p><a href="https://onlinefontconverter.com/" target="_blank">Конвертер шрифтов из .ttf в woff2</a></p>
<p><a href="https://www.fontconverter.io/en" target="_blank">Конвертер шрифтов из .ttf в woff2</a></p>
<p><a href="https://image.online-convert.com/ru/convert-to-webp" target="_blank">Компиляция изображений в webp</a></p>
<p><a href="https://compressor.io/" target="_blank">Сжатие изображений</a></p>
<p><a href="https://developers.google.com/speed/pagespeed/insights/?hl=RU" target="_blank">Проверка скорости загрузки сайта и показателей Pagespeed</a></p>
