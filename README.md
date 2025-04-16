<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jony.edu - ЕНТ дайындық</title>
    <link rel="stylesheet" href="style.css" type="text/css">
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo" onclick="showHome()">Jony.edu</div>
            <nav>
                <a href="#" onclick="showHome()">Басты бет</a>
                <a href="#" onclick="showSubjects()">Пәндер</a>
                <a href="#" onclick="showStats()">Статистика</a>
                <a href="#" onclick="startENTTest()">ЕНТ Тест</a>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <h1>Jony.edu - Сынық білім платформасы</h1>
            <p>Убт дайындық</p>
            <button class="btn" onclick="startENTTest()">Тестті бастау</button>
        </div>
    </section>

    <div class="container">
        <div id="home-page">
            <section class="section">
                <h2 class="section-title">Неге Jony.edu таңдау керек?</h2>
                <div class="subjects-grid">
                    <div class="subject-card">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>ЕНТ тесттері</h3>
                            <p>Нақты ЕНТ сынағына ұқсас тесттер</p>
                        </div>
                    </div>
                    <div class="subject-card">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Қателерді талдау</h3>
                            <p>Әрбір тесттен кейін егжей-тегжейлі түсіндіру</p>
                        </div>
                    </div>
                    <div class="subject-card">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Бейімделген оқыту</h3>
                            <p>Сіздің білім деңгейіңізге сай сұрақтар</p>
                        </div>
                    </div>
                </div>
            </section>
        </div>

        <div id="subjects-page" style="display: none;">
            <section class="section">
                <h2 class="section-title">Пәнді таңдаңыз</h2>
                <div class="subjects-grid">
                    <div class="subject-card" onclick="startSubjectTest('math')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Математика</h3>
                            <p>Алгебра, геометрия және математикалық талдау</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                    <div class="subject-card" onclick="startSubjectTest('history')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Қазақстан тарихы</h3>
                            <p>Ежелгі заманнан бүгінгі күнге дейін</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                    <div class="subject-card" onclick="startSubjectTest('kazakh')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Қазақ тілі</h3>
                            <p>Грамматика, лексика және әдебиет</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                    <div class="subject-card" onclick="startSubjectTest('russian')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Орыс тілі</h3>
                            <p>Грамматика және тесттер</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                    <div class="subject-card" onclick="startSubjectTest('physics')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Физика</h3>
                            <p>Механика, термодинамика және электродинамика</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                    <div class="subject-card" onclick="startSubjectTest('chemistry')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Химия</h3>
                            <p>Органикалық және бейорганикалық химия</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                </div>
            </section>
        </div>

        <div id="ent-test-page" class="test-container">
            <div class="test-header">
                <h2>ЕНТ Тесті</h2>
                <div class="timer" id="timer">20:00</div>
            </div>
            
            <div id="question-container"></div>
            
            <div class="test-nav">
                <button class="btn" id="prev-btn" onclick="prevQuestion()" disabled>Артқа</button>
                <button class="btn" id="next-btn" onclick="nextQuestion()">Келесі</button>
                <button class="btn" id="finish-btn" onclick="finishTest()" style="display: none;">Тестті аяқтау</button>
            </div>
        </div>

        <div id="results-page" class="results-container">
            <h2 class="results-title">Тест нәтижелері</h2>
            <div class="score" id="score">Сіздің нәтижеңіз: 0/20</div>
            
            <div class="progress-bar">
                <div class="progress" id="progress-bar"></div>
            </div>
            
            <h3>Қателерді талдау:</h3>
            <div class="mistakes-list" id="mistakes-list"></div>
            
            <button class="btn" onclick="showHome()" style="margin-top: 2rem;">Басты бетке оралу</button>
        </div>

        <div id="stats-page" class="stats-container">
            <h2 class="section-title">Сіздің статистикаңыз</h2>
            
            <h3>Пәндер бойынша прогресс:</h3>
            <div style="margin: 1rem 0;">
                <p>Математика</p>
                <div class="progress-bar">
                    <div class="progress" style="width: 65%;"></div>
                </div>
            </div>
            
            <div style="margin: 1rem 0;">
                <p>Қазақстан тарихы</p>
                <div class="progress-bar">
                    <div class="progress" style="width: 45%;"></div>
                </div>
            </div>
            
            <div style="margin: 1rem 0;">
                <p>Қазақ тілі</p>
                <div class="progress-bar">
                    <div class="progress" style="width: 30%;"></div>
                </div>
            </div>
            
            <h3 style="margin-top: 2rem;">Соңғы нәтижелер:</h3>
            <ul id="last-results" style="margin: 1rem 0; list-style: none;">
                <li>ЕНТ Тесті: 15/20 (75%)</li>
                <li>Математика: 8/10 (80%)</li>
                <li>Тарих: 6/10 (60%)</li>
            </ul>
            
            <button class="btn" onclick="showHome()" style="margin-top: 1rem;">Басты бетке оралу</button>
        </div>
    </div>

    <footer>
        <div class="container">
            <p>© 2024 Jony.edu - Барлық құқықтар қорғалған</p>
            <p>Бірыңғай ұлттық тестілеуге дайындық</p>
        </div>
    </footer>

    <script src="script.js"></script>
</body>
</html>
