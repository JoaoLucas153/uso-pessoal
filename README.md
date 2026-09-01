# uso-pessoal
<index class="html"></index>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Uma surpresa para você</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f2f2f2;
            color: #222222;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        .page {
            position: absolute;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 40px;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.6s ease-in-out;
        }

        .page.active {
            opacity: 1;
            visibility: visible;
        }

        .content {
            max-width: 700px;
            text-align: center;
            font-size: 2.1rem;
            line-height: 1.6;
            font-weight: 400;
        }

        .btn-next {
            position: absolute;
            bottom: 40px;
            right: 40px;
            background-color: #222222;
            color: #f2f2f2;
            border: none;
            padding: 12px 24px;
            font-size: 1.1rem;
            font-weight: 600;
            border-radius: 30px;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.2s;
        }

        .btn-next:hover {
            background-color: #444444;
            transform: scale(1.05);
        }

        @media (max-width: 768px) {
            .content {
                font-size: 1.5rem;
                padding: 0 20px;
            }
            .btn-next {
                bottom: 20px;
                right: 20px;
                padding: 10px 20px;
                font-size: 0.95rem;
            }
        }
    </style>
</head>
<body>

    <!-- PRIMEIRA PÁGINA -->
    <div class="page active" id="page1">
        <div class="content">
            Eaeee, tudo bem, então, eu acabei fazendo este site pois estava com vontade de te confessar uma coisa mas como eu não queria te incomodar te enchendo de textos e mensagens, resolvi fazer este site, então, se você quiser, dá uma olhadinha e me diz o que achou depois me manda uma mensagem, se você quiser, claro..
        </div>
        <button class="btn-next" onclick="mudarPagina(2)">Próxima página</button>
    </div>

    <!-- SEGUNDA PÁGINA -->
    <div class="page" id="page2">
        <div class="content">
            Desde a primeira vez que te mandei a primeira mensagem, eu me senti tão bem quando você respondia gentilmente, ai daquele ponto pra frente foi so aumentando oque eu sentia por ti, você pode até não sentir o mesmo, mas, oque você acha de a gente sair qualquer dia desses para tomar um sorvete, comer um lanche, ou até mesmo somente para conversarmos, e andarmos pela city.
        </div>
        <button class="btn-next" onclick="mudarPagina(3)">Próxima página</button>
    </div>

    <!-- TERCEIRA PÁGINA -->
    <div class="page" id="page3">
        <div class="content">
            Não estou dizendo isso para te obrigar, mas por que eu estou gostando de ti a um tempo e não consigo ficar sem te dizer isso, mas por favor, dá esta chance para o humilde necessitado aqui 😭😭, prometo te fazer o mais feliz possível, você não irá se arrependerrrr. Mas se você não quiser, aí eu me lasco, mas você ainda pode continuar conversando comigo? tu é a única pessoa que é legal de conversar no dia a dia..
        </div>
    </div>

    <script>
        function mudarPagina(numeroPagina) {
            // Esconde todas as páginas
            const paginas = document.querySelectorAll('.page');
            paginas.forEach(page => page.classList.remove('active'));

            // Mostra a página solicitada
            const paginaAlvo = document.getElementById('page' + numeroPagina);
            if (paginaAlvo) {
                paginaAlvo.classList.add('active');
            }
        }
    </script>

</body>
</html>
