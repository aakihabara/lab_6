<p align = "center">МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ<br>
РОССИЙСКОЙ ФЕДЕРАЦИИ<br>
ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ<br>
ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ<br>
«САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</p>
<br><br><br><br><br><br>
<p align = "center">Институт естественных наук и техносферной безопасности<br>Кафедра информатики<br>Коньков Никита Алексеевич</p>
<br><br><br>
<p align = "center">Лабораторная работа №6<br>«Модель DOM»<br>01.03.02 Прикладная математика и информатика</p>
<br><br><br><br><br><br><br><br><br><br><br><br>
<p align = "right">Научный руководитель<br>
Соболев Евгений Игоревич</p>
<br><br><br>
<p align = "center">г. Южно-Сахалинск<br>2022 г.</p>
<br><br><br><br><br><br><br><br><br><br><br><br>

<h1 align = "center">Введение</h1>

<p> <b>HTML</b> (или же HyperText Markup Language) - стандартизированный язык разметки документов для просмотра веб-страниц в браузере. Веб-браузеры получают HTML документ от сервера по протоколам HTTP/HTTPS или открывают с локального диска, далее интерпретируют код в интерфейс, который будет отображаться на экране монитора. </p>
<p> <b>JavaScript</b> – мультипарадигменный язык программирования. Поддерживает объектно-ориентированный, императивный и функциональный стили. Является реализацией спецификации ECMAScript (стандарт ECMA-262).JavaScript обычно используется как встраиваемый язык для программного доступа к объектам приложений. Наиболее широкое применение находит в браузерах как язык сценариев для придания интерактивности веб-страницам.</p>

<p> <b>DOM</b> (Document Object Model — «объектная модель документа») — это независящий от платформы и языка программный интерфейс, позволяющий программам и скриптам получить доступ к содержимому HTML-, XHTML- и XML-документов, а также изменять содержимое, структуру и оформление таких документов. </p>

<h1 align = "center">Цели и задачи</h1>

<p>1. Сделайте alert по нажатию на кнопку.</p>

<p>2. Сделайте изменение текста в input по нажатию кнопки.</p>

<p>3. Сделайте вывод содержимого input по нажатию кнопки.</p>

<p>4. Сделайте кнопку по нажатию на нее, она выводит alert содержимое input,возведенное в квадрат.</p>

<p>5. Сделайте кнопку по нажатию, она осуществляет обмен содержимым между двумя input.</p>

<p>6. Сделайте кнопку по нажатию на нее поменяется ее текст.</p>

<p>7. Сделайте кнопку по нажатию на нее, она меняет цвет текста в input, используя свойства CSS.</p>

<p>8. Сделайте кнопки по нажатию на них, одна из них блокирует input с помощью атрибута disabled, а другая разблокирует.</p>

<p>9. Сделайте кнопку при наведении на нее появляется alert.</p>

<p>10. Сделайте кнопку при двойном на нее появляется alert.</p>

<p>11. Сделайте область с помощью div при наведении на нее появляется alert.</p>

<p>12. Сделайте кнопку и картинку, при нажатии кнопки картинка меняется.</p>

<p>13. Сделайте alert по нажатию на кнопку. Используя this.</p>

<p>14. Сделайте изменение текста в input по нажатию кнопки. Используя this.</p>

<p>15. Сделайте кнопку, при нажатии кнопки кнопка блокируется.</p>

<p>16. Сделайте кнопку, при нажатии кнопка считает количество нажатий на нее.</p>

<p>17. Сделайте кнопку, при нажатии курсор мышки должен измениться.</p>

<p>18. Используя JavaScript, сделайте так, чтобы при клике на кнопку исчезал элемент с id=&quot;hide&quot</p>

```js
<!DOCTYPE HTML>
<html>
<head>
    <meta charset="utf-8">
</head>
<body>
    <input type="button" id="hider" value="Нажмите, чтобы спрятать текст"/>
    <div id="hide">Текст</div>
<script>
    /* ваш код */
</script>
</body>
</html>

```

<p>19. Создайте кнопку, при клике на которую, она будет скрывать сама себя.</p>

<p> 20.	Напишите простой калькулятор.</p>

<p>21. <a href = "https://www.codewars.com/kata/the-coupon-code"> The Coupon Code</a></p>
<p>22. <a href = "https://www.codewars.com/kata/unlucky-days"> Unlucky Days</a></p>
<p>23. <a href = "https://www.codewars.com/kata/angle-between-clock-hands"> Angle Between Clock Hands</a></p>
<p>24. <a href = "https://www.codewars.com/kata/my-language-skills"> My language skills</a></p>
<p>25. <a href = "https://www.codewars.com/kata/run-length-encoding"> Run-length encoding</a></p>
<p>26. <a href = "https://www.codewars.com/kata/walk-the-object-path"> Walk the Object path</a></p>
<h1 align = "center">Решение</h1>  

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        button, input, span{
            font-size: 24px;
            width: 250px;
        }

        div{
            width: 200px;
            height: 100px;
            border: 2px solid black;
        }
    </style>
</head>
<body>
    <script>

        var countz16 = 0;
        var active = 0;
        function zad1 (){
            alert("Вы нажали на кнопку!")
        }

        function zad2 (){
            document.getElementById('zad2').value = "Я поменялся";
        }

        function zad3 (){
            let res = document.getElementById('zad3').value;
            document.getElementById('zad3m').innerHTML="Вы ввели: " + res;
        }

        function zad4 (){
            let str = document.getElementById('zad4').value;
            if(Number(str)){
                alert(Number(str)**2)
            }
        }

        function zad5 (){
            let str1 = document.getElementById('zad5.1').value;
            let str2 = document.getElementById('zad5.2').value;
            document.getElementById('zad5.1').value = str2;
            document.getElementById('zad5.2').value = str1;
        }

        function zad6 (){
            document.getElementById('zad6').innerHTML = "Я поменялся";
        }
        
        function zad7 (){
            document.getElementById('zad7').style = "color:pink";
        }

        function zad81 (){
            document.getElementById('zad8').disabled = true;
        }

        function zad82 (){
            document.getElementById('zad8').disabled = false;
        }

        function zad12 (){
            document.getElementById('pics').src = "mops2.jpg"
        }

        function zad13 (obj){
            alert(obj.value);
        }

        function zad14 (obj){
            obj.value = "Пока";
        }

        function zad15 (){
            document.getElementById('zad15').disabled = true;
        }

        function zad16 (){
            document.getElementById('zad16').innerHTML = countz16++;
        }

        function zad17 (obj){
            obj.style.cursor = "not-allowed"
        }

        function zad18 (){
            document.getElementById('zad18').hidden = true;
        }

        function zad19 (obj){
            obj.hidden = true;
        }

        function summ(){
            if(Number(document.getElementById('first').value) && Number(document.getElementById('second').value))
            {
                document.getElementById('result').value = Number(document.getElementById('first').value) + Number(document.getElementById('second').value);
            }
            else
            {
                alert('Вам необходимо ввести 2 числа')
            }
        }

        function razn(){
            if(Number(document.getElementById('first').value) && Number(document.getElementById('second').value))
            {
                document.getElementById('result').value = Number(document.getElementById('first').value) - Number(document.getElementById('second').value);
            }
            else
            {
                alert('Вам необходимо ввести 2 числа')
            }
        }
        
        function proiz(){
            if(Number(document.getElementById('first').value) && Number(document.getElementById('second').value))
            {
                document.getElementById('result').value = Number(document.getElementById('first').value) * Number(document.getElementById('second').value);
            }
            else
            {
                alert('Вам необходимо ввести 2 числа')
            }
        }

        function del(){
            if(Number(document.getElementById('first').value) && Number(document.getElementById('second').value))
            {
                document.getElementById('result').value = Number(document.getElementById('first').value) / Number(document.getElementById('second').value);
            }
            else
            {
                alert('Вам необходимо ввести 2 числа')
            }
        }

        function first (){
            active = 1;
        }

        function second (){
            active = 2;
        }

        function input (a){
            let where = 0;
            switch(active)
            {
                case 1:
                    document.getElementById('first').value += a;
                    break;
                case 2:
                    document.getElementById('second').value += a;
                    break;
                default:
                    break;
            }
        }

        function empty(){
            document.getElementById('first').value = ""
            document.getElementById('second').value = ""
            document.getElementById('result').value = ""
        }
    </script>

<button onclick="zad1()">Задание 1</button> <br><br>
<button onclick="zad2()">Задание 2</button> <input type="text" name="zad2" id="zad2"> <br><br>
<button onclick="zad3()">Задание 3</button> <input type="text" name="zad3" id="zad3"> <span id="zad3m"></span> <br><br>
<button onclick="zad4()">Задание 4</button> <input type="text" name="zad4" id="zad4"> <br><br>
<button onclick="zad5()">Задание 5</button> <input type="text" name="zad5.1" id="zad5.1"> <span>Обмен</span> <input type="text" name="zad5.2" id="zad5.2"> <br><br>
<button id="zad6" onclick="zad6()">Задание 6</button> <br><br>
<button onclick="zad7()">Задание 7</button> <input type="text" name="zad7" id="zad7"> <br><br>
<button onclick="zad81()">Задание 8 (Заблокировать)</button> <button onclick="zad82()">Задание 8 (Разблокировать)</button> <input type="text" name="zad8" id="zad8"> <br><br>
<button onmouseover="alert('Ты направил на 9 кнопку')">Задание 9</button> <br><br>
<button ondblclick="alert('А это сейчас двойной щелчок сработал')">Задание 10</button> <br><br>
<div onmouseover="alert('Пока')"> Привет! </div>
<button onclick="zad12()">Задание 12</button> <br><br>
<img id="pics" src="mops.jpg" alt="pic"><br><br>
<input disab value="Привет" onclick="zad13(this)" type="text" name="zad13" id="zad13"> <br><br>
<input value="Привет" onclick="zad14(this)" type="text" name="zad14" id="zad14"> <br><br>
<button id="zad15" onclick="zad15(this)">Задание 15</button> <br><br>
<button id="zad16" onclick="zad16(this)">Задание 16</button> <span id="zad16m"></span> <br><br>
<button onclick="zad17(this)">Задание 17</button>  <br><br>
<button onclick="zad18()">Задание 18</button> <input value="А вот это надо скрыть" type="text" name="zad18" id="zad18"> <br><br>
<button onclick="zad19(this)">Она сейчас скроется</button> <br><br>
<button onclick="zad20()">Вычислить</button> <br><br>
<button onclick="empty()">Очистить</button><br><br>
<button onclick="summ()">Сумма</button><button onclick="razn()">Разность</button><button onclick="proiz()">Произведение</button><button onclick="del()">Частное</button><br><br>
<input disabled type="text" name="first" id="first"> <input disabled type="text" name="second" id="second"> <span> = </span> <input disabled type="text" name="result" id="result"><br><br>
<button onclick="input(1)">1</button><button onclick="input(2)">2</button><button onclick="input(3)">3</button><br><br>
<button onclick="input(4)">4</button><button onclick="input(5)">5</button><button onclick="input(6)">6</button><br><br>
<button onclick="input(7)">7</button><button onclick="input(8)">8</button><button onclick="input(9)">9</button><br><br>
<button onclick="first()">Первое число</button><button onclick="input(0)">0</button><button onclick="second()">Второе число</button><br><br>
</body>
</html>
```

<h1 align = "center">CODEWARS</h1>

<p>21. The Coupon Code</p>

```js
function checkCoupon(enteredCode, correctCode, currentDate, expirationDate){
  let currD = new Date(currentDate);
  let lastD = new Date(expirationDate);
  if((enteredCode === correctCode) && (currD <= lastD))
    return true;
  else
    return false;
}
```

<p>22. Unlucky Days</p>

```js
function unluckyDays(year){
  let res = 0;
  for (let i = 0; i < 12; i++) {
    if(new Date(year, i, 13).getDay() == 5)
      res++
  }
  return res;
}
```

<p>23. Angle Between Clock Hands</p>

```js
function handAngle (date) {
  let hr = date.getHours() % 12;
  let min = date.getMinutes() % 60;
  let minA = min * 6;
  let hrA = hr * 30 + (min / 2);
  let An = Math.abs(hrA - minA);
  if(An > 180){
    An = 360 - An;
  }
  return An / 180 * Math.PI;
}
```

<p>24. My language skills</p>

```js
function myLanguages(results) {
  const sortarr = Object.entries(results).sort((a,b) => b[1] - a[1])
  const res = []
  for(let x of sortarr){
    if(x[1] >= 60) 
      res.push(x[0])
  }

  return res;
}
```

<p>25. Run-length encoding</p>

```js
var runLengthEncoding = function(str){
  let resarr = [];
  let countnum = 1;
  for(let i = 1; i < str.length + 1; i++){
    if(str[i - 1] == str[i]){
      countnum++;
    }
    else
      {
        resarr.push([countnum, str[i - 1]]);
        countnum = 1;
      }
  }
  return resarr;
}
```

<p>26. Walk the Object path</p>

```js
function find(object, path) {
  let properties = path.split('.');
  let toFind = object;

  for (let i = 0; i < properties.length; i++) {
      if (toFind.hasOwnProperty(properties[i])) {
          toFind = toFind[properties[i]];
      } else {
          return undefined;
      }
  }

  return toFind;
}
```

<h1 align = "center">Вывод</h1>
Опираясь на материал с сайта w3school, со сторонних сайтов, Я вспомнил некоторые базовые инструменты html, продолжил решать задачи на codewars.
