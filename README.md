# Лабораторна работа №1 по "Веб-програмуванню"
### Розробка веб-застосувань на мові PHP (налагодження середовища розробки, конструкції мови. Строкові функції. Масиви. Робота з файлами).

***
#### Виконала: Вознюк Дарина
##### Група: 6.04.122.012.16.1

***

<p align="center"><bold>
	Хід роботи:
	</bold></p>
	
	
***Завдання 1<br/>
   Вивчити особливостей протоколу HTTP.<br/>***

Загальна інформація про HTTP:


HTTP (HyperText Transfer Protocol) - це основний протокол, на якому працює Всесвітня павутина.

Як працює HTTP?

При відкритті браузера для доступу до веб-сайту на веб-сервер надходить запит HTTP, веб-сервер повертає браузеру відповідь HTTP. Як правило, одночасно надходить кілька запитів і відповідей, що містять всі дані, необхідні для відображення запитуваної веб-сторінки.

У чому різниця між HTTP і HTTPS?

Розширення протоколу HyperText Transfer Protocol, HTTPS використовує SSL (Secure Sockets Layer) для шифрування даних, що передаються між вашим комп'ютером і веб-сервером. Використання захищеного з'єднання при спілкуванні з веб-сайтом допомагає забезпечити захист інформації від сторонніх зловмисних осіб.

На додаток до переваг безпеки, HTTPS також працює значно швидше, ніж HTTP. Це означає, що елементи веб-сайту часто завантажуються набагато швидше, ніж якби сайт використовував HTTP. У деяких випадках швидкість рендеринга веб-сторінок за допомогою HTTPS збільшується на 70%.


Для практичного ознайомлення з протоколом передачі даних використовувався сайт: http://code.tutsplus.com/tutorials/a-beginners-guide-to-http-and-rest--net-16340

![Практичне ознайомлення з протоколом передачі даних](http1.png)

___

***Завдання 2<br/>
   Ознайомлення з програмними засобами<br/>***

Для виконання лабораторної роботи 1 використовувався Codeenvy.<br/>
Сайт: https://codenvy.io/dashboard/#/ide/dakkarika/LR1?init=true<br/>

Загальна інформація про Codeenvy:<br/>

Codenvy – це середовище розробки на базі контейнерів. Мета сервісу полягає в усуненні необхідність настройки або підтримки локальної або VM-середовища розробника для своїх проектів.
Codenvy заснований на Eclipse Che і доступна в якості сервісу з підтримкою Java, JavaScript, PHP, Python, Node, Scala, Go, Android і ін.


Етапи створення першої програми в Codenvy:
![Етапи створення першої програми в Codenvy](/Codenvy.png)

___

***Завдання 3***

***Ознайомлення з основними конструкціями PHP.***

_Задача 1. Вивід на екран:_

```php
<?php   
  echo "Hello World!\n";
?> 
```

Результат виконання програми:</br>
 ![Результат виконання програми](/Result_1.png)
 

Робота с масивами (використовуючи цикли, керуючі конструкції, різні типи даних тощо):
---

_Задача 2. Створіть масив, заповнений числами від 1 до 10. Знайдіть суму елементів даного масиву._

```php
<?php
	$arr = range(1, 10);
	$temp=array_sum(range(1, 10));
	echo "Сумма элементов массива: $temp";
?>
```

Результат виконання програми:

  ![Результат виконання програми](/Result_2.png)

_Задача 3. Є список прізвищ студентів. Відсортувати їх по алфавіту та вивести на екран._

```php
<?php
	$surname = array("1" => "Петров", "2" => "Гонцов", "3" => "Буйкова", "4" => "Сидоренко");
	asort($surname);
	foreach ($surname as $key => $val) {
        echo "$val ";
}
```

Результат виконання програми:

 ![Результат виконання програми](/Result_3.png)
 

*Задача 4. Є певний номер. По цьому номеру потрібно вивести назву предмета, викладача, мову програмування, що вивчається та кількість лабораторних робіт.*

```php
<?php
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
?>
```

Результат виконання програми:

  ![Результат виконання програми](/Result_4.png)
  

_Задача 5. Заповнити масив числами від 1 до 30. Вивести на екран перший та останній елемент масива, при цьому щоб ці значення видаляти з масиву. Додати до масива 2 елементи, порахувати отриману кількість комірок та вивести всі елементи з ключами на екран.

```php
<?php
	$arr = range(1, 30);
	echo "\nПервый элемент массива: ", array_pop($arr);
	echo "\nПоследний элемент массива: ",array_shift($arr);
	$num = array_push($arr, 100, 200);
	echo "\nКоличество элементов в массиве: $num\n\n";
	print_r($arr);
?>
```

 
Результат виконання програми:

 ![Результат виконання програми](/Result_5.png) 
 

_Задача 6. Використовуючі управляючі конструкції, створити масив та запонити його випадковими числами. Вивести парні числа з масиву.

```php
<?php
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
?>
```
Результат виконання програми:

 ![Результат виконання програми](/Result_6.png)

Робота с файлами:
---

Задача 7. Створити файл input.txt та додати до нього якісь дані. Перевірити коректність відкриття файлу.

Створення файлів:

  ![Результат виконання програми](Files.png)
 
```php
<?php
	$fp = fopen("projects/first/input.txt", "r");
	if ($fp)
	{
	    echo 'Файл открыт';
	    fclose($fp); // Закрытие файла
	}
?>
```

Результат виконання програми:

  ![Результат виконання програми](/Result_7.png)

___

***Завдання 4***

***Проект на GitHub***

Підключення проекту до акаунту на GitHub та дослідження можливостей колаборації Git та Codenvy. 

 
Вигляд проекту на Github:

  ![Вигляд проекту на Github](Git.png)
 
___

***Висновки:***

	Під час виконання лабораторної роботи були отримані первинні практичні навики розробки вебдодатків на мові програмування PHP.
	Я ознайомилася з синтаксисом мови PHP. На прикладі практичних задач я попрактикувала отримані теоретичні знання.
	Окрему увагу, я приділила також особливостям роботи з середою розробки на мові PHP та системі контролю версій GitHub.
	Таким чином, мета лабораторної роботи була досягнута.


