<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arcade Hub - GitHub Games</title>
    <style>
        :root { --neon: #00ff88; --bg: #0d0d0d; --card: #1e1e1e; }
        body { font-family: 'Inter', sans-serif; background: var(--bg); color: white; margin: 0; padding: 20px; }
        header { margin-bottom: 40px; border-bottom: 2px solid var(--neon); padding-bottom: 10px; }
        h1 { font-size: 2.5em; letter-spacing: 2px; color: var(--neon); }
        .grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); gap: 15px; max-width: 1200px; margin: 0 auto; }
        .game-card { background: var(--card); border-radius: 10px; overflow: hidden; transition: 0.3s; text-decoration: none; color: white; display: flex; flex-direction: column; border: 1px solid #333; }
        .game-card:hover { transform: scale(1.05); border-color: var(--neon); box-shadow: 0 0 15px rgba(0,255,136,0.3); }
        .thumb { height: 120px; background: #2a2a2a; display: flex; align-items: center; justify-content: center; font-size: 2em; }
        .info { padding: 10px; font-weight: 600; font-size: 0.9em; text-align: center; }
    </style>
</head>
<body>

    <header>
        <h1>🎮 MI ARCADE GITHUB</h1>
        <p>Selecciona un juego para empezar a jugar inmediatamente.</p>
    </header>

    <div class="grid" id="container"></div>

    <script>
        const games = [
            { n: "Rocketgoal.io", u: "https://rocketgoal.io/", e: "🚀" },
            { n: "Scape Road City", u: "https://escaperoad.org", e: "🏙️" },
            { n: "Scape Road 3", u: "https://agaronline.io/escape-road-3", e: "🏎️" },
            { n: "Scape Raid", u: "https://escaperoad.io/", e: "🚓" },
            { n: "Eggy Car", u: "https://eggycar.club", e: "🥚" },
            { n: "Top Speed 3D", u: "https://topspeed.com", e: "🏁" },
            { n: "Getaway Shootout", u: "https://getawayshootout.com", e: "🏃" },
            { n: "Rooftop Snipers", u: "https://rooftopsnipers.com", e: "🎯" },
            { n: "Rooftop Snipers 2", u: "https://rooftopsnipers2.com", e: "🔫" },
            { n: "SmashKarts.io", u: "https://smashkarts.io", e: "💣" },
            { n: "Flip Rush", u: "https://poki.com", e: "🚲" },
            { n: "Geometry Dash", u: "https://geometrydash.io", e: "🟨" },
            { n: "Wheelie Master", u: "https://poki.com", e: "🏍️" },
            { n: "Slope Rider", u: "https://slope-game.github.io/", e: "⛷️" },
            { n: "Furious Kart Racing", u: "https://crazygames.com", e: "🏎️" },
            { n: "Impostor Online", u: "https://crazygames.com", e: "🕵️" },
            { n: "Gartic Phone", u: "https://garticphone.com", e: "📞" },
            { n: "Make It Meme", u: "https://makeitmeme.com", e: "🤡" },
            { n: "Pinturillo 2", u: "https://pinturillo2.com", e: "🎨" },
            { n: "Slither.io", u: "https://slither.io", e: "🐍" },
            { n: "Melon Sandbox", u: "https://melonsandbox.com/", e: "🍉" },
            { n: "Retro Rush", u: "https://poki.com", e: "🕶️" },
            { n: "James Gun", u: "https://poki.com", e: "🕴️" }
        ];

        const container = document.getElementById('container');
        games.forEach(g => {
            const card = document.createElement('a');
            card.href = g.u;
            card.target = "_blank";
            card.className = 'game-card';
            card.innerHTML = `
                <div class="thumb">${g.e}</div>
                <div class="info">${g.n}</div>
            `;
            container.appendChild(card);
        });
    </script>
</body>
</html>
