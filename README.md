<!DOCTYPE html>
<head>
    <title>Зоомагазин "Все для питомцев"</title>
    <link  href="style.css" rel="stylesheet" type="text/css">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tooltipster/dist/css/tooltipster.bundle.min.css">
    <script src="https://cdn.jsdelivr.net/npm/tooltipster/dist/js/tooltipster.bundle.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.7.14/dist/vue.min.js"></script>

    <style>
        table{
            border-collapse:separate;
            table-layout: fixed;
            border: 2px solid rgb(244, 164, 177);
        }
        #mysyk {
            border: 2px solid rgb(211, 86, 107) !important; 
        }
        canvas {
            position: absolute;
            z-index: 1;
        }
        svg {
            position: absolute;
            z-index: 0;
        } button {
    background-color: #ffc0cb;
    border: 2px solid #ff69b4; 
    color: white; 
    font-size: 12px; 
    font-family: Arial, sans-serif;
    padding: 10px 20px;
    border-radius: 8px;
    cursor: pointer; 
    transition: background-color 0.3s, transform 0.2s;
    }
title, h1,h2,h3, p {
    color: rgb(162, 20, 89);
}
a:link {
    color: rgb(86, 40, 40);
    text-decoration: none;
}
a:hover {
    color: green; 
    text-decoration: underline; 
}
a:visited {
    color: rgb(128, 6, 0); 
}
a:active {
    color: red; 
}
ul{
    list-style-type: square;
    padding-left: 20px;
}

ul{
    margin: 5px 0;
}
body{
    background: linear-gradient(rgb(255, 170, 187), rgb(196, 195, 255), rgb(255, 170, 187), rgb(196, 195, 255), rgb(255, 170, 187));
    background-repeat: repeat;
    background-position: top
}
h1{
    font-family: "Monotype Corsiva";
    font-style:oblique;
}
#zabota {
    font-family: "Monotype Corsiva";
    font-style:oblique;
    font-size: larger;
}
div.menu {
    position: relative;
    border: 1px solid rgb(244, 164, 177);
    margin-left: 3cm;
    margin-right: 1cm;  
    margin-top: 0;
    margin-bottom: 2cm; 
    text-indent: 1.5cm; 
    background-color: #edfff1; 
    font-family: "Times New Roman";
    font-size: 14pt; 
    line-height: 1.5;
}
div.menu::first-letter {
    font-size: 18pt;
    font-weight: bold;
}
#ani{
    width: 100%;
    border-collapse: collapse;
}
#ani th{
    text-align: center;
    background-color: #ffe4e1;
    padding: 10px;
}

#ani td{
    padding: 10px;
    border: 1px solid rgb(244, 164, 177); 
}

#ani td:first-child {
    text-align: justify;
}

#ani td:nth-child(2) {
    text-align: center;
}
#ani td:nth-child(odd) {
    background-color: white; 
}

#ani td:nth-child(even) {
    background-color: #ffe4e1;
}
#ani{
    box-shadow: 1px 8px 20px rgba(0, 0, 0, 0.3);
    border-radius:8px; 
}
.img {
    float: right;
    margin-right: 15px; 
    margin-bottom: 10px;
}
.tov {
    text-align: justify;
    font-family: Arial, sans-serif;
    font-size: 16px;
}
img[src$=".jpg"] {
    border: 8px dotted #ffceeb;
}
    </style>
</head>
<body bgcolor="#f8f0e3" text="#333333">
    <nav>
        <div class="menu">
            <table id="ani" width="100%" border="1" cellpadding="10">
                <tr>
                    <td><a href="#cats">Товары для кошек</a></td>
                    <td><a href="#dogs">Товары для собак</a></td>
                    <td><a href="#birds">Товары для птиц</a></td>
                    <td><a href="#animals">Другие животные</a></td>
                    <td><a href="#contacts">Контакты</a></td>
                </tr>
            </table>
        </div>
        <button id="change-font">Изменить шрифт</button>
        </nav>
        <svg width="800" height="400">
            <circle cx="750" cy="100" r="30" fill="yellow">
                <animate 
                    attributeName="r" 
                    from="30" 
                    to="40" 
                    dur="2s" 
                    begin="0s; s.end" 
                    fill="freeze" 
                    id="g" />
                <animate 
                    attributeName="r" 
                    from="40" 
                    to="30" 
                    dur="2s" 
                    begin="g.end" 
                    fill="freeze" 
                    id="s" />
            </circle>
        </svg>
        <canvas id="canvas" width="1500" height="400"></canvas>
    <header id="head">
        <table width="100%" border="0" bgcolor="#ffebcd" cellpadding="10">
            <tr>
                <td align="center">
                    <h1>Зоомагазин "Все для питомцев"</h1>
                    <img src="яяя.JPEG" height="150" alt="Добро пожаловать">
                    <p id="zabota"><strong>Мы заботимся о ваших любимцах!</strong></p>
                </td>
            </tr>
        </table>
    </header>
    <section id="cats">
        <div>
            <table id="mysyk" width="100%" border="0" cellpadding="10">
                <tr>
                    <td align="center" bgcolor="#faf0e6">
                        <h2 class="tov" id="mys">Товары для кошек</h2>
                        <img class="img" src="кошки (1).jpg" height="300" width="300" alt="Кошки">
                        
                        <ul id="catItems">
                            <li><span>Корм для кошек:</span> <strong>от 1500 тг.</strong></li>
                            <li><span>Игрушки для кошек:</span> <strong>от 1000 тг.</strong></li>
                            <li><span>Когтеточки:</span> <strong>от 1500 тг.</strong></li>
                        </ul>
                        <button onclick="sor()">Сортировать товары</button>
                        <h2>Хотите добавить товар?</h2> 
                        <button onclick="kos()">Добавить товар</button>
                        
                    </td>
                </tr>
            </table>
        </div>
    </section>
    <section id="dogs">
        <div id="ch">
            <table width="100%" border="0" cellpadding="10">
                <tr>
                    <td align="center" bgcolor="#faf0e6">
                        <h2 class="tov">Товары для собак</h2>
                        <img class="img" src="собаки.jpg" height="300" width="300" alt="Собаки">
                        <ul>
                            <li><a href="file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/%D0%BA%D0%BE%D1%80%D0%BC%D0%B0.html">Корм для собак: </a><strong>от 2000 тг.</strong></li>
                            <li><a href="file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/toy.html">Игрушки для собак: </a><strong>от 1400 тг.</strong></li>
                            <li><a href="file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/acc.html">Поводки и ошейники: </a><strong>от 3000 тг.</strong></li>
                        </ul>
                        <button @click="chooseProduct">Выбор товара</button>
                    </td>
                </tr>
            </table>
        </div>
    </section>   
    <section id="birds">
        <div> 
            <table width="100%" border="0" cellpadding="10">
                <tr>
                    <td align="center" bgcolor="#faf0e6">
                        <h2 class="tov">Товары для птиц</h2>
                        <img class="img" src="птицы (1).jpg" height="300" width="300">
                        <button id="add">Добавить элемент</button>
                        <button id="removen">Удалить элемент</button>
                        <ul>
                            <li><a href="file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/acc.html">Клетки для птиц: </a><strong>от 8000 тг.</strong></li>
                            <li><a href="file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/%D0%BA%D0%BE%D1%80%D0%BC%D0%B0.html">Корм для птиц: </a><strong>от 1000 тг.</strong></li>
                            <li><a href="file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/toy.html">Игрушки для птиц:</a><strong>от 800 тг.</strong></li>
                        </ul>
                    </td>
                </tr>
            </table>
        </div>
    </section>
    <section id="animals">
        <div>
            <table id="tab" width="100%" border="0" cellpadding="10">
                <tr>
                    <td align="center" bgcolor="#faf0e6">
                        <h2>Товары для других животных</h2>
                        <table>
                            <tr>
                                <td>
                                    <h3>1. Кролики</h3>
                                <img src="кролики (1).jpg" height="300" width="300">
                                <p>Корм, клетки и игрушки для кроликов</p>
                            </td>
                            <td>
                                <h3>2. Хомяки</h3>
                                <img src="хомяк.jpg" height="300" width="300">
                                <p>Корм, клетки и игрушки для хомяков</p>
                            </td>
                            <td>
                            <h3>3. Морские свинки</h3>
                            <img src="свинки (1).jpg" height="300" width="300">
                            <p>Корм и аксессуары для морских свинок</p>
                            </td>
                            </tr>
                            <tr>
                            <td>
                            <h3>4. Черепахи</h3>
                            <img src="черепаха.jpg" height="300" width="300">
                            <p>Аквариумы и корм для черепах</p>
                            </td>
                            <td>
                            <h3>5. Ящерицы</h3>
                            <img src="ящерица (1).jpg" height="300" width="300">
                            <p>Террариумы и корм для ящериц</p>
                            </td>
                            <td>
                            <h3>6. Змеи</h3>
                            <img src="змея (1).jpg" height="300" width="300">
                            <p>Террариумы и корм для змей</p>
                            </td>
                            </tr>
                            <tr>
                            <td>
                            <h3>7. Рыбы</h3>
                            <img src="рыбы (1).jpg" height="300" width="300">
                            <p>Аквариумы и корм для рыб</p>
                            </td>
                            <td>
                            <h3>8. Фретки</h3>
                            <img src="фретки (1).jpg" height="300" width="300">
                            <p>Корм и аксессуары для фреток</p>
                            </td>
                            <td>
                            <h3>9. Лягушки</h3>
                            <img src="лягушки (1).jpg" height="300" width="300">
                            <p>Террариумы и аксессуары для лягушек</p>
                            </td>
                            </tr>
                            <tr>
                            <td>
                            <iframe name="i" src="file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/%D0%BA%D0%BE%D1%80%D0%BC%D0%B0.html" width="400" height="200"></iframe></td>
                            <td>
                            <iframe name="in" src="file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/toy.html" width="400" height="200"></iframe></td>
                            <td>
                            <iframe name="inf" src="file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/acc.html" width="400" height="200"></iframe></td>
                            </tr>
                        </table>
                    </td>
                </tr>
            </table>
        </div>
    </section>
    <canvas id="canvas" width="800" height="400" align="center"></canvas>
    <table width="100%" border="1" cellpadding="10" bgcolor="#ffe4e1">
        <tr>
            <td align="center">
                <h2 id="contacts">Контакты</h2>
                <p>Адрес: ул. Жибек жолы, 12, г. Усть-Каменогорск</p>
                <p>Телефон: +7 771 133 1348</p>
                <p>Email: zoomagazin@mail.ru</p>
            </td>
        </tr>
    </table>
    <h2 align="center">Закажите товары для ваших питомцев</h2>
<div id="box" >
<form id="orderForm" action="#" method="post" align="center">
    <label for="type">Тип животного:</label><br>
    <select id="type" name="type" required>
        <option value="cat">Кошка</option>
        <option value="dog">Собака</option>
        <option value="bird">Птица</option>
        <option value="hamster">Хомяк</option>
        <option value="rabbit">Кролик</option>
        <option value="fish">Рыба</option>
        <option value="reptile">Рептилия</option>
        <option value="snake">Змея</option>
        <option value="ferret">Фретка</option>
        <option value="guinea_pig">Морская свинка</option>
    </select>
    <br><br>

    <label for="produc">Выберите товар:</label><br>
    <input type="text" id="product" name="product" placeholder="Название товара" required>
    <br><br>

    <label for="quantity">Количество:</label><br>
    <input type="number" id="quantity" min="1" placeholder="1" required>
    <br><br>

    <label for="address">Адрес доставки:</label><br>
    <input type="text" id="address" placeholder="Улица, дом, квартира" required>
    <br><br>

    <label for="phone">Контактный телефон:</label><br>
    <input type="tel" id="phone" placeholder="+7 (_) _-__" required>
    <br><br>

    <label for="comments">Дополнительные комментарии:</label><br>
    <textarea rows="2" cols="25" placeholder="Дополнительная информация..."></textarea>
    <br><br>
    <button type="button" onclick="showMessage()">Оформить заказ</button>
    <button id="fadeOut">Скрыть</button>
</form>
</div>
<div id="app" align="center">
    <button @click="toggle">Показать/Скрыть блок</button>
    <div v-if="show">
        <button onclick="UserAgent()">Показать User Agent</button>
        <button onclick="Platform()">Показать платформу</button>
        <button onclick="ScreenInfo()">Информация о экране</button>
        <button onclick="Locations()">Показать URL</button>
        <button onclick="Frames()">Показать количество фреймов</button>
    </div>
</div>
<div id="aaa" align="center">
    <h2>Хотите добавить отзыв?</h2>
    <input v-model="newTask" placeholder="Отзывы о сайте">
    <button @click="addTask">Оставить отзыв</button>
    <ul>
        <li v-for="(task, index) in tasks" :key="index">
            {{ task }} 
            <button @click="removeTask(index)" style="margin-left: 10px;">Удалить</button>
        </li>
    </ul>
</div>
<script>
    //а
$(document).ready(function () {
    $("h1").text("Добро пожаловать!").css("color", "#f266a3");
    
    $("#add").click(function () {
        $("ul").append("<li>Новый элемент списка</li>");
    });

    $("#removen").click(function () {
        $("ul li:last").remove();
    });

    $("#change-font").click(function () {
        $(".menu").css({
            "font-size": "20px",
            "font-family": "Courier New",
            "color": "blue",
        });
    });

    $("a").hover(function () {
        $(this).css("font-size", "18px");
        }, function () {
            $(this).css("font-size", "");
        });
    
    $(".menu").click(function () {
        $(this).fadeOut(2000).fadeIn(2000);
    });


    $('#fadeOut').click(function () {
            $('#box').fadeOut();
    });
    

    //б
    $("a").tooltipster({
        content: "Перейти к разделу",
        animation: "fade",
        delay: 200,
        });
    });

    new Vue({
            el: '#app',
            data: {
                show: true
            },
            methods: {
                toggle() {
                    this.show = !this.show;
                }
            }
        });

        new Vue({
            el: '#aaa',
            data: {
                newTask: '',
                tasks: [] 
            },
            methods: {
                addTask() {
                    if (this.newTask.trim()) {
                        this.tasks.push(this.newTask.trim()); 
                        this.newTask = '';
                    }
                },
                removeTask(index) {
                    this.tasks.splice(index, 1);
                }
            }
        });

        new Vue({
            el: '#ch',
            methods: {
                chooseProduct: function() {
                    const products = {
                        'Корм для собак': 2000,
                        'Игрушки для собак': 1400,
                        'Поводки и ошейники': 3000,
                    };

                    let selectedProduct = prompt('Выберите товар: \nКорм для собак\nИгрушки для собак\nПоводки и ошейники\n');

                    if (products[selectedProduct]) {
                        alert(`${selectedProduct} стоит ${products[selectedProduct]} тенге`);
                    } else {
                        alert('Товар не найден!');
                    }
                }
            }
        });

        function showMessage() {
        alert('Заказ оформлен');
        }


    function tovar() {
        const h = document.getElementById('mys');
        h.style.color = 'teal';
        h.style.fontSize = '24px';
        h.style.fontFamily = 'Arial, sans-serif';
    }
    tovar()
    function sor() {
        const list = document.getElementById('catItems');
        const items = Array.from(list.getElementsByTagName('li'));
        items.sort((a, b) => {
            const nameA = a.innerText.toLowerCase();
            const nameB = b.innerText.toLowerCase();
            return nameA.localeCompare(nameB);
        });
        list.innerHTML = '';
        items.forEach(item => list.appendChild(item));
    }

    function kos() {
        const itemName = prompt("Введите название товара:");
        const itemPrice = prompt("Введите цену товара:");
        if (itemName && itemPrice) {
        const newItem = document.createElement('li');
        newItem.innerHTML = `<span>${itemName}:</span> <strong>от ${itemPrice} тг.</strong> <button onclick="remove(this)">Удалить</button>`;
        document.getElementById('catItems').appendChild(newItem);
        }
    }

    function remove(button) {
        const item = button.parentElement;
        item.remove();
    }
    function remove(button) {
            const item = button.parentElement;
            item.remove();
    }
    function UserAgent() {
        alert(navigator.userAgent);
    }

    function Platform() {
        alert(navigator.platform);
    }
    function ScreenInfo() {
        alert(screen.width+"x"+screen.height);
    }

    function Locations() {
        alert(`Текущий URL: ${window.location.href}`);
    }

    function Frames() {
        alert(`Количество фреймов: ${window.frames.length}`);
    }
    function Scree() {
    const info = `Ширина экрана: ${screen.width}px\n` +
                 `Высота экрана: ${screen.height}px\n` + 
                 `Доступная ширина: ${screen.availWidth}px\n` +
                 `Доступная высота: ${screen.availHeight}px`;
    alert(info);
}
    window.frames.i.location = 'file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/toy.html';
    window.frames.in.location = 'file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/acc.html';
    window.frames.inf.location = 'file:///C:/Users/user/Desktop/1%20%D1%81%D0%B5%D0%BC/html/%D0%BA%D0%BE%D1%80%D0%BC%D0%B0.html';
</script>
</body>
</html>
