# Лабораторна работа №1 по "Веб-програмуванню"
### Розробка веб-застосувань на мові PHP (налагодження середовища розробки, конструкції мови. Строкові функції. Масиви. Робота з файлами).

***
#### Виконала: Вознюк Дарина
##### Група: 6.04.122.012.16.1

***

Хід роботи:<br/>
Завдання 1<br/>
Ознайомлення з програмними засобами<br/>

Для виконання лабораторної роботи 1 використовувався Codeenvy.<br/>
Сайт: https://codenvy.io/dashboard/#/ide/dakkarika/LR1?init=true<br/>
Загальна інформація про Codeenvy:<br/>

Codenvy – це середовище розробки на базі контейнерів. Мета сервісу полягає в усуненні необхідність настройки або підтримки локальної або VM-середовища розробника для своїх проектів.
Codenvy заснований на Eclipse Che і доступна в якості сервісу з підтримкою Java, JavaScript, PHP, Python, Node, Scala, Go, Android і ін.

___
Завдання 2
Ознайомлення з основними конструкціями PHP

Вивід на екран:

```php
<?php   
  echo "Hello World!\n";
?>
```

Результат виконання програми:
 

Робота с масивами (використовуючи цикли, керуючі конструкції, різні типи даних тощо):
---

Задача 2. Створіть масив, заповнений числами від 1 до 10. Знайдіть суму елементів даного масиву.
`<?php
	$arr = range(1, 10);
	$temp=array_sum(range(1, 10));
	echo "Сумма элементов массива: $temp";
?>`

Результат виконання програми:
 

Задача 3. Є список прізвищ студентів. Відсортувати їх по алфавіту та вивести на екран.

`<?php
$surname = array("1" => "Петров", "2" => "Гонцов", "3" => "Буйкова", "4" => "Сидоренко");
asort($surname);
foreach ($surname as $key => $val) {
    echo "$val ";
}`

Результат виконання програми:
 

Задача 4. Є певний номер. По цьому номеру потрібно вивести назву предмета, викладача, мову програмування, що вивчається та кількість лабораторних робіт.

`<?php
$menu=1;

$subject = [
 'name'=>['веб-программирование', 'программирование мобильных устройств'],
 'lector'=>['Алексеев В. О.', 'Поляков А. О.'],
 'progrLang'=>['php', 'kotlin'],
 'labWorks'=>['4', '7'],
];

if($menu==1)
{
    echo "Предмет: ",$subject['name'][0], ". Ведёт: ", $subject['lector'][0],". Изучается язык: ", $subject['progrLang'][0],". Нужно сдать: ", $subject['labWorks'][0],
" лабораторные работы."; 
}
else
{
    echo "Предмет: ",$subject['name'][1], ". Ведёт: ", $subject['lector'][1],". Изучается язык: ", $subject['progrLang'][1],". Нужно сдать: ", $subject['labWorks'][1],
" лабораторные работы."; 
}
?>`

Результат виконання програми:
 

Задача 5. Заповнити масив числами від 1 до 30. Вивести на екран перший та останній елемент масива, при цьому щоб ці значення видаляти з масиву. Додати до масива 2 елементи, порахувати отриману кількість комірок та вивести всі елементи з ключами на екран.

`<?php
	$arr = range(1, 30);
	echo "\nПервый элемент массива: ", array_pop($arr);
	echo "\nПоследний элемент массива: ",array_shift($arr);
	$num = array_push($arr, 100, 200);
	echo "\nКоличество элементов в массиве: $num\n\n";
	print_r($arr);
?>`

 
Результат виконання програми:
 

Задача 6. Використовуючі управляючі конструкції, створити масив та запонити його випадковими числами. Вивести парні числа з масиву.

`<?php
for($i=0;$i<10;$i++){
  $mas[]=rand(0,10);
}
print_r( $mas);

echo "\nЧётные числа: ";
foreach ($mas as $key => $value) {
    if ($value % 2) { 
        continue;
    }
    else 
        {
          echo $mas[$key]," ";
        }
}
?>`
Результат виконання програми:
 

Робота с файлами:
---

Задача 7. Створити файл input.txt та додати до нього якісь дані. Перевірити коректність відкриття файлу.
 

`<?php
$fp = fopen("projects/first/input.txt", "r");
if ($fp)
{
    echo 'Файл открыт';
    fclose($fp); // Закрытие файла
}
?>`

Результат виконання програми:
 
 ___
Завдання 3
Проект на GitHub

Підключення проекту до акаунту на GitHub та дослідження можливостей колаборації Git та Codenvy.
 

 

 

 

 

 

 

 
Вигляд проекту на Github:
 
___
***Висновки:***<br/>
	> Під час виконання лабораторної роботи були отримані первинні практичні навики розробки вебдодатків на мові програмування PHP.
	Я ознайомилася з синтаксисом мови PHP. На прикладі практичних задач я попрактикувала отримані теоретичні знання.
	Окрему увагу, я приділила також особливостям роботи з середою розробки на мові PHP та системі контролю версій GitHub.
	Таким чином, мета лабораторної роботи була досягнута.


