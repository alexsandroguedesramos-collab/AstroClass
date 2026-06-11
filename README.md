

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exploração Astronômica</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #0b0c21;
            color: #ffffff;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #1c1f4a;
            padding: 20px;
            text-align: center;
        }

        header h1 {
            margin: 0;
            font-size: 2.5em;
            color: #ffd700;
        }

        nav {
            background-color: #2c2f66;
            display: flex;
            justify-content: center;
            gap: 20px;
            padding: 10px 0;
        }

        nav a {
            color: #ffffff;
            text-decoration: none;
            font-weight: bold;
        }

        nav a:hover {
            color: #ffd700;
        }

        section {
            padding: 40px 20px;
            max-width: 900px;
            margin: auto;
        }

        h2 {
            color: #ffd700;
        }

        .planetas {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }

        .planeta {
            background-color: #1c1f4a;
            padding: 20px;
            border-radius: 10px;
            width: 200px;
            text-align: center;
        }

        .planeta img {
            width: 100px;
            height: 100px;
        }

        footer {
            background-color: #1c1f4a;
            text-align: center;
            padding: 20px;
            margin-top: 40px;
        }

        button {
            background-color: #ffd700;
            border: none;
            padding: 10px 15px;
            cursor: pointer;
            border-radius: 5px;
            font-weight: bold;
        }

        button:hover {
            background-color: #e6c200;
        }
    </style>
</head>
<body>
    <header>
        <h1>Exploração Astronômica</h1>
    </header>

    <nav>
        <a href="#introducao">Introdução</a>
        <a href="#planetas">Planetas</a>
        <a href="#curiosidades">Curiosidades</a>
    </nav>

    <section id="introducao">
        <h2>Bem-vindo ao Universo!</h2>
        <p>Este site é dedicado à exploração do espaço e dos corpos celestes. Descubra planetas, estrelas e curiosidades do nosso sistema solar e além.</p>
    </section>

    <section id="planetas">
        <h2>Planetas do Sistema Solar</h2>
        <div class="planetas" id="lista-planetas">
            <!-- Planetas serão carregados via JavaScript -->
        </div>
    </section>

    <section id="curiosidades">
        <h2>Curiosidades Astronômicas</h2>
        <p>O espaço é cheio de mistérios! Sabia que existem estrelas maiores que o nosso Sol que poderiam engolir o planeta Júpiter inteiro? Ou que existem planetas feitos de diamante?</p>
        <button onclick="alert('Continue explorando e aprendendo sobre o cosmos! 🌌')">Inspire-se!</button>
    </section>

    <footer>
        &copy; 2026 Exploração Astronômica
    </footer>

    <script>
        const planetas = [
            { nome: "Mercúrio", img: "https://upload.wikimedia.org/wikipedia/commons/4/4a/Mercury_in_true_color.jpg" },
            { nome: "Vênus", img: "https://upload.wikimedia.org/wikipedia/commons/e/e5/Venus-real_color.jpg" },
            { nome: "Terra", img: "https://upload.wikimedia.org/wikipedia/commons/9/97/The_Earth_seen_from_Apollo_17.jpg" },
            { nome: "Marte", img: "https://upload.wikimedia.org/wikipedia/commons/0/02/OSIRIS_Mars_true_color.jpg" },
            { nome: "Júpiter", img: "https://upload.wikimedia.org/wikipedia/commons/e/e2/Jupiter.jpg" },
            { nome: "Saturno", img: "https://upload.wikimedia.org/wikipedia/commons/c/c7/Saturn_during_Equinox.jpg" },
            { nome: "Urano", img: "https://upload.wikimedia.org/wikipedia/commons/3/3d/Uranus2.jpg" },
            { nome: "Netuno", img: "https://upload.wikimedia.org/wikipedia/commons/5/56/Neptune_Full.jpg" },
        ];

        const listaPlanetas = document.getElementById('lista-planetas');

        planetas.forEach(planeta => {
            const div = document.createElement('div');
            div.classList.add('planeta');
            div.innerHTML = `
                <img src="${planeta.img}" alt="${planeta.nome}">
                <h3>${planeta.nome}</h3>
            `;
            listaPlanetas.appendChild(div);
        });
    </script>
</body>
</html>
