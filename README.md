<!DOCTYPE html>

<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Setembro Amarelo | Valorize a Vida</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    scroll-behavior:smooth;
}

:root{
    --yellow:#ffd21f;
    --yellow2:#ffb800;
    --dark:#111827;
    --dark2:#182235;
    --card:#202c42;
    --text:#f8fafc;
    --muted:#aeb9ca;
    --green:#43d17a;
    --border:rgba(255,255,255,.1);
}

body{
    font-family:Arial,Helvetica,sans-serif;
    background:
        radial-gradient(circle at 80% 10%,rgba(255,210,31,.14),transparent 30%),
        radial-gradient(circle at 10% 40%,rgba(67,209,122,.08),transparent 25%),
        var(--dark);
    color:var(--text);
    line-height:1.7;
}

/* NAVBAR */

nav{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
    background:rgba(17,24,39,.9);
    backdrop-filter:blur(15px);
    border-bottom:1px solid var(--border);
}

.nav{
    max-width:1200px;
    margin:auto;
    padding:15px 25px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.logo{
    font-size:21px;
    font-weight:bold;
    color:var(--yellow);
}

.logo span{
    color:white;
}

.links{
    display:flex;
    list-style:none;
    gap:22px;
}

.links a{
    text-decoration:none;
    color:var(--muted);
    font-size:14px;
    transition:.3s;
}

.links a:hover{
    color:var(--yellow);
}

/* HERO */

.hero{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:120px 20px 70px;
}

.hero-content{
    max-width:900px;
}

.badge{
    display:inline-block;
    padding:7px 16px;
    border-radius:30px;
    background:rgba(255,210,31,.1);
    border:1px solid rgba(255,210,31,.35);
    color:var(--yellow);
    font-size:13px;
    font-weight:bold;
    margin-bottom:20px;
}

.hero h1{
    font-size:clamp(50px,8vw,90px);
    line-height:1;
    margin-bottom:25px;
}

.hero h1 span{
    color:var(--yellow);
}

.hero p{
    max-width:700px;
    margin:auto;
    color:var(--muted);
    font-size:18px;
}

.buttons{
    margin-top:35px;
    display:flex;
    justify-content:center;
    gap:15px;
    flex-wrap:wrap;
}

.btn{
    padding:13px 22px;
    border-radius:10px;
    text-decoration:none;
    font-weight:bold;
    transition:.3s;
}

.primary{
    background:var(--yellow);
    color:#171717;
}

.primary:hover{
    transform:translateY(-3px);
    box-shadow:0 10px 30px rgba(255,210,31,.25);
}

.secondary{
    color:white;
    border:1px solid var(--border);
    background:rgba(255,255,255,.04);
}

.secondary:hover{
    background:rgba(255,255,255,.08);
}

/* SECTIONS */

section{
    max-width:1200px;
    margin:auto;
    padding:90px 25px;
}

.title{
    margin-bottom:45px;
}

.title small{
    color:var(--yellow);
    text-transform:uppercase;
    letter-spacing:2px;
    font-weight:bold;
}

.title h2{
    font-size:40px;
    margin-top:5px;
}

.title p{
    color:var(--muted);
    max-width:700px;
    margin-top:10px;
}

/* CARDS */

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
    gap:20px;
}

.card{
    background:linear-gradient(145deg,var(--card),#172033);
    border:1px solid var(--border);
    border-radius:18px;
    padding:28px;
    transition:.3s;
}

.card:hover{
    transform:translateY(-6px);
    border-color:rgba(255,210,31,.4);
}

.icon{
    width:50px;
    height:50px;
    display:flex;
    align-items:center;
    justify-content:center;
    border-radius:13px;
    background:rgba(255,210,31,.12);
    font-size:24px;
    margin-bottom:18px;
}

.card h3{
    margin-bottom:10px;
}

.card p{
    color:var(--muted);
    font-size:15px;
}

/* CONTENT */

.content{
    background:var(--card);
    border:1px solid var(--border);
    border-radius:20px;
    padding:35px;
    margin-bottom:25px;
}

.content h3{
    color:var(--yellow);
    margin-bottom:12px;
}

.content p{
    color:#d3dae6;
    margin-bottom:12px;
}

/* HIGHLIGHT */

.highlight{
    border-left:4px solid var(--yellow);
    padding:20px;
    background:rgba(255,210,31,.07);
    border-radius:0 12px 12px 0;
    margin:25px 0;
}

.highlight strong{
    color:var(--yellow);
}

/* TIMELINE */

.timeline{
    max-width:850px;
    margin:auto;
    position:relative;
}

.timeline:before{
    content:"";
    position:absolute;
    left:20px;
    top:0;
    height:100%;
    width:2px;
    background:rgba(255,210,31,.3);
}

.item{
    position:relative;
    padding-left:65px;
    margin-bottom:35px;
}

.dot{
    position:absolute;
    left:11px;
    top:5px;
    width:20px;
    height:20px;
    border-radius:50%;
    background:var(--yellow);
    box-shadow:0 0 0 5px rgba(255,210,31,.1);
}

.item h3{
    color:var(--yellow);
}

/* STEPS */

.steps{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
    gap:18px;
}

.step{
    background:var(--card);
    border:1px solid var(--border);
    border-radius:16px;
    padding:25px;
}

.number{
    color:var(--yellow);
    font-size:30px;
    font-weight:bold;
}

/* QUIZ */

.quiz{
    max-width:850px;
    margin:auto;
}

.question{
    display:none;
    background:var(--card);
    border:1px solid var(--border);
    padding:30px;
    border-radius:20px;
}

.question.active{
    display:block;
    animation:fade .4s;
}

@keyframes fade{
    from{
        opacity:0;
        transform:translateY(10px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.question-number{
    color:var(--yellow);
    font-weight:bold;
    margin-bottom:10px;
}

.question h3{
    margin-bottom:20px;
}

.options{
    display:grid;
    gap:10px;
}

.option{
    border:1px solid var(--border);
    background:#29364d;
    color:white;
    padding:15px;
    border-radius:10px;
    cursor:pointer;
    text-align:left;
    transition:.2s;
}

.option:hover{
    border-color:var(--yellow);
    transform:translateX(3px);
}

.option.correct{
    background:rgba(67,209,122,.18);
    border-color:var(--green);
}

.option.wrong{
    background:rgba(220,80,80,.18);
    border-color:#e66;
}

.explanation{
    display:none;
    margin-top:18px;
    padding:15px;
    background:rgba(255,255,255,.04);
    border-radius:10px;
    color:var(--muted);
}

.quiz-buttons{
    display:flex;
    justify-content:space-between;
    margin-top:20px;
}

.quiz-btn{
    border:0;
    padding:12px 20px;
    border-radius:9px;
    background:var(--yellow);
    font-weight:bold;
    cursor:pointer;
}

.quiz-btn:disabled{
    opacity:.4;
    cursor:not-allowed;
}

#result{
    display:none;
    text-align:center;
    background:var(--card);
    padding:40px;
    border-radius:20px;
    border:1px solid var(--border);
}

#score{
    color:var(--yellow);
    font-size:55px;
    font-weight:bold;
    margin:15px;
}

/* FOOTER */

footer{
    border-top:1px solid var(--border);
    text-align:center;
    padding:35px 20px;
    color:var(--muted);
}

footer strong{
    color:var(--yellow);
}

@media(max-width:700px){

    .links{
        display:none;
    }

    .hero h1{
        font-size:50px;
    }

    .title h2{
        font-size:32px;
    }

    section{
        padding:70px 18px;
    }
}
</style>

</head>

<body>

<nav>
    <div class="nav">

```
    <div class="logo">
        Setembro <span>Amarelo</span>
    </div>

    <ul class="links">
        <li><a href="#inicio">Início</a></li>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#importancia">Importância</a></li>
        <li><a href="#acolhimento">Acolhimento</a></li>
        <li><a href="#quiz">Quiz</a></li>
    </ul>

</div>
```

</nav>

<header class="hero" id="inicio">

```
<div class="hero-content">

    <span class="badge">
        💛 CONSCIENTIZAÇÃO • ACOLHIMENTO • PREVENÇÃO
    </span>

    <h1>
        Setembro<br>
        <span>Amarelo</span>
    </h1>

    <p>
        Um espaço educativo para aprender sobre saúde emocional,
        prevenção, empatia, acolhimento e a importância de conversar
        e buscar apoio.
    </p>

    <div class="buttons">

        <a href="#sobre" class="btn primary">
            Começar a estudar →
        </a>

        <a href="#quiz" class="btn secondary">
            Fazer o quiz
        </a>

    </div>

</div>
```

</header>

<section id="sobre">

```
<div class="title">

    <small>01 • Conheça a campanha</small>

    <h2>O que é o Setembro Amarelo?</h2>

    <p>
        Entenda a proposta da campanha e por que falar sobre saúde
        emocional é importante.
    </p>

</div>

<div class="content">

    <h3>💛 Uma campanha de conscientização</h3>

    <p>
        O Setembro Amarelo é uma campanha de conscientização voltada
        à valorização da vida, à promoção do diálogo sobre saúde
        emocional e à prevenção do suicídio.
    </p>

    <p>
        A campanha busca combater o silêncio e o estigma que podem
        dificultar que uma pessoa procure ajuda quando está passando
        por um momento difícil.
    </p>

</div>

<div class="highlight">

    <strong>Ideia principal:</strong>
    cuidar da saúde emocional faz parte do cuidado com a saúde
    como um todo. Escutar, acolher e incentivar a busca por ajuda
    são atitudes importantes.

</div>
```

</section>

<section id="importancia">

```
<div class="title">

    <small>02 • Por que falar sobre isso?</small>

    <h2>Informação também é cuidado</h2>

</div>

<div class="cards">

    <div class="card">

        <div class="icon">🧠</div>

        <h3>Saúde emocional</h3>

        <p>
            Nossas emoções fazem parte da vida. Aprender a reconhecê-las
            e conversar sobre elas pode contribuir para o bem-estar.
        </p>

    </div>

    <div class="card">

        <div class="icon">💬</div>

        <h3>Diálogo</h3>

        <p>
            Conversas respeitosas podem ajudar a diminuir o isolamento
            e mostrar que procurar apoio é uma atitude de cuidado.
        </p>

    </div>

    <div class="card">

        <div class="icon">🤝</div>

        <h3>Acolhimento</h3>

        <p>
            Demonstrar atenção e empatia pode fazer diferença para
            alguém que esteja enfrentando um período difícil.
        </p>

    </div>

    <div class="card">

        <div class="icon">🌱</div>

        <h3>Prevenção</h3>

        <p>
            A prevenção envolve informação, apoio, acesso a cuidados
            e construção de ambientes onde as pessoas possam pedir ajuda.
        </p>

    </div>

</div>
```

</section>

<section>

```
<div class="title">

    <small>03 • Como ajudar</small>

    <h2>Pequenas atitudes podem acolher</h2>

</div>

<div class="steps">

    <div class="step">

        <div class="number">01</div>

        <h3>Escute</h3>

        <p>
            Dê atenção à pessoa sem interromper ou transformar
            imediatamente a conversa em um julgamento.
        </p>

    </div>

    <div class="step">

        <div class="number">02</div>

        <h3>Leve a sério</h3>

        <p>
            Quando alguém demonstra sofrimento emocional, trate
            o que ela está sentindo com respeito.
        </p>

    </div>

    <div class="step">

        <div class="number">03</div>

        <h3>Incentive ajuda</h3>

        <p>
            Incentive a pessoa a conversar com um adulto de confiança
            ou com um profissional de saúde.
        </p>

    </div>

    <div class="step">

        <div class="number">04</div>

        <h3>Não fique sozinho</h3>

        <p>
            Situações difíceis não precisam ser enfrentadas sem apoio.
            Procurar pessoas confiáveis é uma forma de cuidado.
        </p>

    </div>

</div>
```

</section>

<section id="acolhimento">

```
<div class="title">

    <small>04 • Acolhimento</small>

    <h2>Como construir um ambiente mais acolhedor?</h2>

</div>

<div class="cards">

    <div class="card">

        <div class="icon">👂</div>

        <h3>Ouvir sem julgar</h3>

        <p>
            Evite minimizar os sentimentos de outra pessoa ou dizer
            que ela simplesmente precisa "ser forte".
        </p>

    </div>

    <div class="card">

        <div class="icon">❤️</div>

        <h3>Demonstrar cuidado</h3>

        <p>
            Mostrar presença, respeito e atenção pode ajudar a pessoa
            a perceber que ela não precisa lidar com tudo sozinha.
        </p>

    </div>

    <div class="card">

        <div class="icon">🏫</div>

        <h3>Na escola</h3>

        <p>
            Professores, funcionários, familiares e colegas podem
            contribuir para um ambiente mais seguro e respeitoso.
        </p>

    </div>

    <div class="card">

        <div class="icon">🌎</div>

        <h3>Na sociedade</h3>

        <p>
            Informação responsável ajuda a combater preconceitos
            e facilita o acesso das pessoas ao apoio necessário.
        </p>

    </div>

</div>
```

</section>

<section>

```
<div class="title">

    <small>05 • Mitos e fatos</small>

    <h2>Informação correta é importante</h2>

</div>

<div class="content">

    <h3>❌ "Falar sobre saúde emocional sempre piora a situação."</h3>

    <p>
        Conversas responsáveis e acolhedoras podem ajudar a diminuir
        o isolamento. O importante é abordar o tema com cuidado,
        respeito e incentivar a busca por apoio adequado.
    </p>

</div>

<div class="content">

    <h3>❌ "Pedir ajuda é sinal de fraqueza."</h3>

    <p>
        Procurar ajuda é uma forma de cuidar de si. Psicólogos,
        médicos, familiares, professores e outras pessoas de confiança
        podem fazer parte de uma rede de apoio.
    </p>

</div>

<div class="content">

    <h3>✅ "Saúde mental merece atenção durante todo o ano."</h3>

    <p>
        O Setembro Amarelo aumenta a visibilidade do tema, mas
        cuidado emocional, empatia e prevenção são importantes
        durante todo o ano.
    </p>

</div>
```

</section>

<section>

```
<div class="title">

    <small>06 • Reflexão</small>

    <h2>Uma mensagem importante</h2>

</div>

<div class="content">

    <h3>💛 Você não precisa resolver tudo sozinho</h3>

    <p>
        Momentos difíceis fazem parte da experiência humana. Quando
        uma situação parece pesada demais, conversar com alguém de
        confiança e buscar ajuda profissional pode ser um passo
        importante.
    </p>

    <p>
        Se você perceber que alguém está passando por uma situação
        difícil, procure um adulto de confiança ou um profissional
        de saúde que possa ajudar.
    </p>

</div>
```

</section>

<section id="quiz">

```
<div class="title">

    <small>07 • Teste seus conhecimentos</small>

    <h2>Quiz do Setembro Amarelo 🧠</h2>

    <p>
        Responda às questões e descubra quanto você aprendeu.
    </p>

</div>


<div class="quiz">

    <div class="question active">

        <div class="question-number">
            QUESTÃO 1 / 6
        </div>

        <h3>
            Qual é o principal objetivo do Setembro Amarelo?
        </h3>

        <div class="options">

            <button class="option" onclick="answer(this,false)">
                A) Promover uma competição esportiva
            </button>

            <button class="option" onclick="answer(this,true)">
                B) Promover conscientização, prevenção e valorização da vida
            </button>

            <button class="option" onclick="answer(this,false)">
                C) Falar somente sobre alimentação
            </button>

            <button class="option" onclick="answer(this,false)">
                D) Celebrar uma data esportiva
            </button>

        </div>

        <div class="explanation">
            O Setembro Amarelo busca ampliar a conscientização sobre
            saúde emocional, prevenção e valorização da vida.
        </div>

        <div class="quiz-buttons">
            <span></span>
            <button class="quiz-btn" onclick="nextQuestion()" disabled>
                Próxima →
            </button>
        </div>

    </div>


    <div class="question">

        <div class="question-number">
            QUESTÃO 2 / 6
        </div>

        <h3>
            Qual atitude pode contribuir para o acolhimento de alguém?
        </h3>

        <div class="options">

            <button class="option" onclick="answer(this,false)">
                A) Ignorar a pessoa
            </button>

            <button class="option" onclick="answer(this,true)">
                B) Escutar com respeito e incentivar a busca por ajuda
            </button>

            <button class="option" onclick="answer(this,false)">
                C) Fazer julgamentos
            </button>

            <button class="option" onclick="answer(this,false)">
                D) Dizer que o problema não importa
            </button>

        </div>

        <div class="explanation">
            Escutar com respeito e incentivar a busca por apoio são
            atitudes que podem contribuir para o acolhimento.
        </div>

        <div class="quiz-buttons">

            <button class="quiz-btn" onclick="previousQuestion()">
                ← Voltar
            </button>

            <button class="quiz-btn" onclick="nextQuestion()" disabled>
                Próxima →
            </button>

        </div>

    </div>


    <div class="question">

        <div class="question-number">
            QUESTÃO 3 / 6
        </div>

        <h3>
            A saúde emocional deve ser cuidada:
        </h3>

        <div class="options">

            <button class="option" onclick="answer(this,false)">
                A) Somente em setembro
            </button>

            <button class="option" onclick="answer(this,true)">
                B) Durante todo o ano
            </button>

            <button class="option" onclick="answer(this,false)">
                C) Apenas na escola
            </button>

            <button class="option" onclick="answer(this,false)">
                D) Apenas quando existe um problema
            </button>

        </div>

        <div class="explanation">
            O Setembro Amarelo amplia a discussão sobre o tema,
            mas o cuidado com a saúde emocional é importante
            durante todo o ano.
        </div>

        <div class="quiz-buttons">

            <button class="quiz-btn" onclick="previousQuestion()">
                ← Voltar
            </button>

            <button class="quiz-btn" onclick="nextQuestion()" disabled>
                Próxima →
            </button>

        </div>

    </div>


    <div class="question">

        <div class="question-number">
            QUESTÃO 4 / 6
        </div>

        <h3>
            Pedir ajuda quando alguém está passando por uma situação
            difícil significa:
        </h3>

        <div class="options">

            <button class="option" onclick="answer(this,false)">
                A) Fraqueza
            </button>

            <button class="option" onclick="answer(this,true)">
                B) Uma atitude de cuidado
            </button>

            <button class="option" onclick="answer(this,false)">
                C) Falta de responsabilidade
            </button>

            <button class="option" onclick="answer(this,false)">
                D) Algo desnecessário
            </button>

        </div>

        <div class="explanation">
            Procurar ajuda é uma forma de cuidado e pode aproximar
            a pessoa de uma rede de apoio.
        </div>

        <div class="quiz-buttons">

            <button class="quiz-btn" onclick="previousQuestion()">
                ← Voltar
            </button>

            <button class="quiz-btn" onclick="nextQuestion()" disabled>
                Próxima →
            </button>

        </div>

    </div>


    <div class="question">

        <div class="question-number">
            QUESTÃO 5 / 6
        </div>

        <h3>
            Quem pode fazer parte de uma rede de apoio?
        </h3>

        <div class="options">

            <button class="option" onclick="answer(this,false)">
                A) Somente amigos
            </button>

            <button class="option" onclick="answer(this,false)">
                B) Somente professores
            </button>

            <button class="option" onclick="answer(this,true)">
                C) Pessoas de confiança e profissionais de saúde
            </button>

            <button class="option" onclick="answer(this,false)">
                D) Ninguém
            </button>

        </div>

        <div class="explanation">
            Uma rede de apoio pode envolver familiares, amigos,
            professores, adultos de confiança e profissionais
            de saúde.
        </div>

        <div class="quiz-buttons">

            <button class="quiz-btn" onclick="previousQuestion()">
                ← Voltar
            </button>

            <button class="quiz-btn" onclick="nextQuestion()" disabled>
                Próxima →
            </button>

        </div>

    </div>


    <div class="question">

        <div class="question-number">
            QUESTÃO 6 / 6
        </div>

        <h3>
            Qual atitude ajuda a combater o estigma relacionado
            à saúde emocional?
        </h3>

        <div class="options">

            <button class="option" onclick="answer(this,false)">
                A) Espalhar informações falsas
            </button>

            <button class="option" onclick="answer(this,false)">
                B) Fazer piadas sobre o sofrimento dos outros
            </button>

            <button class="option" onclick="answer(this,true)">
                C) Buscar informação confiável e tratar as pessoas com respeito
            </button>

            <button class="option" onclick="answer(this,false)">
                D) Evitar qualquer conversa sobre o assunto
            </button>

        </div>

        <div class="explanation">
            Informação confiável, empatia e respeito ajudam a reduzir
            preconceitos e tornam o ambiente mais acolhedor.
        </div>

        <div class="quiz-buttons">

            <button class="quiz-btn" onclick="previousQuestion()">
                ← Voltar
            </button>

            <button class="quiz-btn" onclick="nextQuestion()">
                Finalizar →
            </button>

        </div>

    </div>


    <div id="result">

        <h2>Quiz concluído! 💛</h2>

        <div id="score">0/6</div>

        <p id="message"></p>

        <br>

        <button class="quiz-btn" onclick="restartQuiz()">
            Refazer quiz
        </button>

    </div>

</div>
```

</section>

<footer>

```
<p>
    💛 <strong>Setembro Amarelo</strong>
</p>

<p>
    Informação • Empatia • Acolhimento • Valorização da Vida
</p>

<br>

<small>
    Este site é educativo e não substitui orientação de profissionais
    de saúde.
</small>
```

</footer>

<script>

let currentQuestion = 0;
let score = 0;
let answered = false;

const questions = document.querySelectorAll(".question");

function answer(button, correct){

    if(answered) return;

    answered = true;

    const current = questions[currentQuestion];

    const options = current.querySelectorAll(".option");

    options.forEach(option => {
        option.disabled = true;
    });

    if(correct){

        button.classList.add("correct");

        score++;

    }else{

        button.classList.add("wrong");

        options.forEach(option => {

            if(
                option.getAttribute("onclick") &&
                option.getAttribute("onclick").includes("true")
            ){
                option.classList.add("correct");
            }

        });

    }

    current.querySelector(".explanation").style.display="block";

    const nextButton =
        current.querySelector(".quiz-buttons button:last-child");

    if(nextButton){
        nextButton.disabled=false;
    }
}


function nextQuestion(){

    if(!answered) return;

    questions[currentQuestion].classList.remove("active");

    currentQuestion++;

    if(currentQuestion >= questions.length){

        showResult();

        return;
    }

    questions[currentQuestion].classList.add("active");

    answered=false;
}


function previousQuestion(){

    if(currentQuestion===0) return;

    questions[currentQuestion].classList.remove("active");

    currentQuestion--;

    questions[currentQuestion].classList.add("active");

    answered=true;
}


function showResult(){

    document.getElementById("result").style.display="block";

    document.getElementById("score").textContent =
        score + "/6";

    let message;

    if(score===6){

        message="Excelente! Você entendeu muito bem os principais conceitos.";

    }else if(score>=4){

        message="Muito bom! Você já compreendeu boa parte do conteúdo.";

    }else if(score>=2){

        message="Bom começo! Revise o conteúdo e tente novamente.";

    }else{

        message="Que tal revisar o material e fazer o quiz novamente?";

    }

    document.getElementById("message").textContent=message;
}


function restartQuiz(){

    currentQuestion=0;
    score=0;
    answered=false;

    document.getElementById("result").style.display="none";

    questions.forEach((question,index)=>{

        question.classList.remove("active");

        const options =
            question.querySelectorAll(".option");

        options.forEach(option=>{

            option.disabled=false;

            option.classList.remove("correct");
            option.classList.remove("wrong");

        });

        const explanation =
            question.querySelector(".explanation");

        if(explanation){
            explanation.style.display="none";
        }

        const nextButton =
            question.querySelector(".quiz-buttons button:last-child");

        if(nextButton){
            nextButton.disabled=true;
        }

    });

    questions[0].classList.add("active");
}

</script>

</body>
</html># Setembro-amarelo
