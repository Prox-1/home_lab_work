<h1 align="center"><a href="#" target="_blank">Kurganov Daniils lab</a></h1>
<hr>

<h2 align="center">Задание</h2>
<p>Вася написал программу на языке Python. Он ожидает, что его программа читает по очереди 
целые числа из файла, удваивает каждое значение и выводит в новый файл значения, которые 
больше определенного значения. Однако каждый раз Василий получает не то, что ожидает. 
Помогите Василию разобраться с проблемой, используя pdb.</p>
<p>Пример корректной работы:</p>
<p>[In]: </p>
<p> 5</p>
<p> 10</p>
<p> 15</p>
<p> 20</p>
<br>
<p>[Out]:</p>
<p> 20</p>
<p> 30</p>
<p> 40</p>
<p> Оформите результат отладки в виде лабораторной работы. Каждый шаг отладки 
зафиксируйте в работе.</p>
<hr>
<h3 align="center">Выявление ошибок</h3>
<p>Для начала необходимо выяснить работает ли данная программа вовсе, и если работает то каков ее результат</p>
<img src="https://github.com/Prox-1/home_lab_work/blob/41f71db9b9d6448540d52aae63a3f33d12d38ddf/img/1.png">
<p>Видно что программа выполняется без каких либо синтаксических ошибок, однако она выдает неверный вывод: </p>
<p> ' 5'</p>
<p> ' 5'</p>
<p> ' 10'</p>
<p> ' 10'</p>
<p> '15'</p>
<p> '15'</p>
<p> ' 20' ' 20'</p>
<hr>
<h3 align="center">Выявление причин</h3>
<p>Для процесса отладки будет использоваться модуль ipdb, который предоставляет удобные для данного процесса инструменты.</p>
<p>Проверка функции чтения файла: </p>
<img src="https://github.com/Prox-1/home_lab_work/blob/41f71db9b9d6448540d52aae63a3f33d12d38ddf/img/2.png">
<p>После вывода результатов функции становится ясно что причиной некорректной работы является неправильное чтение данных.</p>
<p>ИСПРАВИМ!</p>
<hr>
<h3 align="center">Исправление ошибок</h3>
<p>Необходимо скорректировать функцию 'load_data': </p>
<img src="https://github.com/Prox-1/home_lab_work/blob/41f71db9b9d6448540d52aae63a3f33d12d38ddf/img/3.png">
<p>Был изменен вывод, в генерации списка к каждому элементу мы применяем метод strip() который отбрасывает все пустые значения в строке, а затем приводим это значение к int</p>
<p>После сохранения изменений получаем следующий вывод: </p>
<p>10203040</p>
<p>Необходимо скорректировать функцию обработки данных: </p>
<img src="https://github.com/Prox-1/home_lab_work/blob/41f71db9b9d6448540d52aae63a3f33d12d38ddf/img/4.png">
<p>А так же функцию сохранения данных в новый файл: </p>
<img src="https://github.com/Prox-1/home_lab_work/blob/41f71db9b9d6448540d52aae63a3f33d12d38ddf/img/5.png">
<hr>
<h3 align="center">Программа работает корректно</h3>
