# flask2-html

Сайт можно посмотреть по http://127.0.0.1:5000/

APP.PY

from flask import Flask, render_template

app = Flask(__name__)


@app.route("/")
def home():
    return render_template("index.html")


if __name__ == "__main__":
    app.run(debug=True)


INDEX.HTML

<!DOCTYPE html>
<html lang="ru">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Мой блог</title>

    <link rel="stylesheet" href="{{ url_for('static', filename='style.css') }}">
</head>

<body>

    <header>
        <h1>Мои достижения и навыки</h1>

        <p class="subtitle">
            Добро пожаловать в мой учебный блог!
        </p>
    </header>


    <main>

        <section class="about">
            <h2>Обо мне</h2>

            <img src="{{ url_for('static', filename='image.png') }}"
                 alt="Моя фотография">

            <p>
                Я изучаю веб-разработку и постепенно осваиваю
                HTML, CSS, Python и Flask.
            </p>

            <p>
                В этом блоге я рассказываю о своих навыках,
                достижениях и результатах обучения.
            </p>
        </section>


        <section class="skills">
            <h2>Мои навыки</h2>

            <ul>
                <li>HTML — создание структуры веб-страниц</li>
                <li>CSS — оформление и стилизация сайтов</li>
                <li>Python — программирование</li>
                <li>Flask — создание веб-приложений</li>
                <li>Adobe Illustrator — работа с графикой</li>
            </ul>
        </section>


        <section class="achievements">
            <h2>Мои достижения</h2>

            <ol>
                <li>Создала своё первое Flask-приложение.</li>
                <li>Научилась работать с HTML и CSS.</li>
                <li>Освоила базовую работу в GitHub.</li>
            </ol>
        </section>


        <section class="progress">
            <h2>Мой прогресс обучения</h2>

            <table>
                <tr>
                    <th>HTML</th>
                    <th>CSS</th>
                    <th>Python</th>
                    <th>Flask</th>
                    <th>Git</th>
                    <th>GitHub</th>
                    <th>JavaScript</th>
                    <th>Дизайн</th>
                </tr>

                <tr>
                    <td>80%</td>
                    <td>70%</td>
                    <td>60%</td>
                    <td>50%</td>
                    <td>50%</td>
                    <td>40%</td>
                    <td>20%</td>
                    <td>75%</td>
                </tr>

                <tr>
                    <td>90%</td>
                    <td>80%</td>
                    <td>60%</td>
                    <td>50%</td>
                    <td>40%</td>
                    <td>40%</td>
                    <td>10%</td>
                    <td>80%</td>
                </tr>

                <tr>
                    <td>Хороший прогресс</td>
                    <td>Нужно практиковаться</td>
                    <td>Изучаю основы</td>
                    <td>Изучаю Flask</td>
                    <td>Изучаю Git</td>
                    <td>Работаю с GitHub</td>
                    <td>Начальный уровень</td>
                    <td>Хороший уровень</td>
                </tr>
            </table>
        </section>

    </main>


    <footer>
        <p>Учебный проект Flask • 2026</p>
    </footer>

</body>

</html>


STYLE.CSS


* {
    box-sizing: border-box;
}

body {
    margin: 0;
    background-color: #eef3f8;
    color: #263238;
    font-family: Arial, sans-serif;
    font-size: 18px;
    line-height: 1.6;
}


header {
    background-color: #315b78;
    color: white;
    text-align: center;
    padding: 40px 20px;
}


h1 {
    margin: 0;
    font-family: Georgia, serif;
    font-size: 42px;
}


.subtitle {
    font-size: 22px;
    margin-top: 10px;
}


main {
    max-width: 1100px;
    margin: 30px auto;
    padding: 0 20px;
}


section {
    background-color: white;
    margin-bottom: 30px;
    padding: 30px;
    border-radius: 15px;
}


h2 {
    font-family: Georgia, serif;
    font-size: 30px;
    margin-top: 0;
}


p {
    font-size: 18px;
}


img {
    display: block;
    width: 300px;
    height: 300px;
    object-fit: cover;
    margin: 20px auto;
    border-radius: 50%;
}


ul,
ol {
    font-size: 18px;
    padding-left: 30px;
}


li {
    margin-bottom: 8px;
}


table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 20px;
    font-size: 15px;
}


th,
td {
    border: 1px solid #9aaab5;
    padding: 12px;
    text-align: center;
}


th {
    background-color: #315b78;
    color: white;
}


td {
    background-color: #f7f9fb;
}


footer {
    text-align: center;
    background-color: #263238;
    color: white;
    padding: 20px;
    font-size: 16px;
}
