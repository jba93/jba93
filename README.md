<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Juliana Arvani</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: "Segoe UI", sans-serif;
}

body{
    min-height:100vh;
    background:
        linear-gradient(180deg,#180022,#090012);
    color:white;
    overflow-x:hidden;
}

/* Fundo vaporwave */

body::before{
    content:"";
    position:fixed;
    inset:0;
    background:
    radial-gradient(circle at 20% 20%, rgba(255,0,140,.25), transparent 30%),
    radial-gradient(circle at 80% 30%, rgba(255,60,60,.25), transparent 30%),
    radial-gradient(circle at 50% 80%, rgba(180,0,255,.25), transparent 30%);
    z-index:-1;
}

/* Cabeçalho */

.hero{
    text-align:center;
    padding:100px 20px;
}

.avatar{
    width:140px;
    height:140px;
    margin:auto;
    border-radius:50%;
    background:linear-gradient(
        135deg,
        #ff006e,
        #ff4d6d
    );

    display:flex;
    align-items:center;
    justify-content:center;

    font-size:48px;
    font-weight:bold;

    box-shadow:
        0 0 30px #ff006e,
        0 0 60px rgba(255,0,110,.4);
}

h1{
    margin-top:25px;
    font-size:3rem;
    color:#fff;
}

.subtitle{
    margin-top:10px;
    color:#ffb3d1;
    font-size:1.1rem;
}

.section{
    max-width:900px;
    margin:auto;
    padding:60px 25px;
}

.card{
    background:rgba(255,255,255,.05);
    border:1px solid rgba(255,255,255,.1);
    backdrop-filter:blur(10px);
    border-radius:24px;
    padding:30px;
    margin-bottom:25px;
}

h2{
    margin-bottom:20px;
    color:#ff4d8d;
}

p{
    line-height:1.8;
    color:#f5d6e8;
}

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:20px;
}

.project{
    text-align:center;
    transition:.3s;
}

.project:hover{
    transform:translateY(-5px);
}

.tag{
    display:inline-block;
    margin:5px;
    padding:8px 14px;
    border-radius:50px;
    background:linear-gradient(
        135deg,
        #ff006e,
        #ff4d6d
    );
}

.contact{
    text-align:center;
}

.contact a{
    color:#ff85b5;
    text-decoration:none;
    display:block;
    margin:10px 0;
}

footer{
    text-align:center;
    padding:40px;
    color:#d9a5bd;
}

.line{
    width:200px;
    height:3px;
    margin:20px auto;
    background:linear-gradient(
        90deg,
        transparent,
        #ff006e,
        transparent
    );
}

</style>
</head>
<body>

<section class="hero">

    <div class="avatar">
        JB
    </div>

    <h1>Juliana Arvani</h1>

    <div class="line"></div>

    <p class="subtitle">
        Dados • Python • Analytics
    </p>

</section>

<section class="section">

    <div class="card">
        <h2>✦ Sobre Mim</h2>

        <p>
            Olá! Sou Juliana Arvani.
            Trabalho utilizando dados e 
            análises para apoiar decisões 
            estratégicas de negócio.

            Tenho interesse em tecnologia, programação,
            automação de processos e ciência de dados.
        </p>
    </div>

    <div class="card">

        <h2>✦ Tecnologias</h2>

        <div class="tags">
            <span class="tag">Python</span>
            <span class="tag">SQL</span>
            <span class="tag">Power BI</span>
            <span class="tag">Excel</span>
            <span class="tag">Git</span>
            <span class="tag">GitHub</span>
        </div>

    </div>

    <div class="card">

        <h2>✦ Portfólio</h2>

        <div class="grid">

            <div class="project">
                <h3>📊 Análise de Dados</h3>
                <p>Dashboards, indicadores e análises.</p>
            </div>

            <div class="project">
                <h3>🐍 Python</h3>
                <p>Automação e desenvolvimento.</p>
            </div>

            <div class="project">
                <h3>📈 Modelagem</h3>
                <p>Projetos analíticos para negócios.</p>
            </div>

        </div>

    </div>

    <div class="card contact">

        <h2>✦ Contato</h2>

        /jba93" target="_blank">
            💻 GitHub
        </a>

        https://www.linkedin.com/in/juliana-arvani/
            💼 LinkedIn
        </a>

    </div>

</section>

<footer>
    ✦ Feito por Juliana Arvani ✦
</footer>

<script>

const cards = document.querySelectorAll('.card');

const observer = new IntersectionObserver(entries => {

    entries.forEach(entry => {

        if(entry.isIntersecting){
            entry.target.animate(
                [
                    {opacity:0, transform:'translateY(30px)'},
                    {opacity:1, transform:'translateY(0)'}
                ],
                {
                    duration:700,
                    fill:'forwards'
                }
            );
        }

    });

});

cards.forEach(card => {
    card.style.opacity = 0;
    observer.observe(card);
});

</script>

</body>
</html>
