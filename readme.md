Here's the updated webpage with actual moon and Mars images incorporated into the fancy design:

xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Celestial Deeds™ - Own a Piece of the Cosmos</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700;900&family=Playfair+Display:wght@400;500;600&family=Montserrat:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-gold: #d4af37;
            --deep-space: #0a0a1a;
            --nebula-purple: #1a002e;
            --starlight: #e6e6fa;
            --cosmic-blue: #003366;
            --mars-red: #b22222;
            --lunar-silver: #c0c0c0;
        }
        
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, var(--deep-space) 0%, var(--nebula-purple) 100%);
            color: var(--starlight);
            line-height: 1.7;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }
        
        /* STARRY BACKGROUND */
        body::before {
            content: '';
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(255,255,255,0.15) 0%, transparent 20%),
                radial-gradient(circle at 80% 70%, rgba(255,255,255,0.1) 0%, transparent 20%),
                radial-gradient(circle at 40% 40%, rgba(255,255,255,0.08) 0%, transparent 15%),
                radial-gradient(circle at 90% 20%, rgba(255,255,255,0.12) 0%, transparent 18%);
            animation: twinkle 20s ease-in-out infinite;
            z-index: -2;
        }
