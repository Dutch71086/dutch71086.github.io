<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lunar & Martian Deeds - Novelty Space Property</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Georgia', serif; background: #0a0a1a; color: #e0e0ff; line-height: 1.6; }
        .container { max-width: 800px; margin: 0 auto; padding: 2rem; }
        header { text-align: center; padding: 2rem 0; border-bottom: 1px solid #333; }
        h1 { font-size: 2.5rem; margin-bottom: 0.5rem; color: #ffd700; }
        .disclaimer { background: rgba(255, 0, 0, 0.1); border: 1px solid #ff4444; 
                     padding: 1.5rem; margin: 2rem 0; border-radius: 8px; }
        .disclaimer h2 { color: #ff4444; margin-bottom: 1rem; }
        .disclaimer p { font-size: 0.9rem; }
        .deed-preview { background: rgba(255, 215, 0, 0.05); border: 2px solid #ffd700; 
                        padding: 2rem; margin: 2rem 0; border-radius: 12px; text-align: center; }
        .deed-preview h2 { color: #ffd700; margin-bottom: 1rem; }
        .deed-content { font-size: 1.2rem; margin: 1.5rem 0; }
        .deed-footer { font-size: 0.9rem; color: #ccc; margin-top: 2rem; }
        .form-group { margin: 1.5rem 0; }
        label { display: block; margin-bottom: 0.5rem; font-weight: bold; }
        input, select { width: 100%; padding: 0.75rem; border: 1px solid #555; 
                       background: rgba(255,255,255,0.05); border-radius: 4px; color: #fff; }
        button { background: #ffd700; color: #000; border: none; padding: 1rem 2rem; 
                 font-size: 1.1rem; cursor: pointer; border-radius: 4px; 
                 transition: background 0.3s; }
        button:hover { background: #ffe066; }
        .planet-options { display: flex; gap: 1rem; margin: 1rem 0; }
        .planet-option { flex: 1; text-align: center; padding: 1rem; 
                        background: rgba(255,255,255,0.03); border-radius: 8px; }
        .planet-option img { max-width: 60px; margin-bottom: 0.5rem; }
        .footer { text-align: center; padding: 2rem 0; font-size: 0.9rem; color: #666; border-top: 1px solid #333; margin-top: 3rem; }
        @media (max-width: 600px) { .container { padding: 1rem; } h1 { font-size: 2rem; } }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Lunar & Martian Deeds Office</h1>
            <p>Novelty Celestial Property Certificates</p>
        </header>

        <div class="disclaimer">
            <h2>⚠️ LEGAL DISCLAIMER - READ BEFORE PURCHASE</h2>
            <p><strong>These deeds are novelty items ONLY.</strong> Under the Outer Space Treaty of 1967, no nation can claim sovereignty over celestial bodies, and therefore no individual can own land on the moon, Mars, or any other space body. These certificates have no legal standing and do not confer any actual property rights, ownership, or development privileges. They are intended strictly as entertainment gifts, decorative items, or conversation pieces.</p>
            <p>By purchasing, you acknowledge this is a novelty product with no real-world value or legal significance.</p>
        </div>

        <section>
            <h2>Choose Your Celestial Property</h2>
            <div class="planet-options">
                <div class="planet-option" onclick="selectPlanet('moon')">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/8d/Moon.jpg/250px-Moon.jpg" alt="Moon">
                    <h3>Moon Property</h3>
                    <p>Select your lunar parcel</p>
                </div>
                <div class="planet-option" onclick="selectPlanet('mars')">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/02/Mars_Valles_Marineris.jpg/250px-Mars_Valles_Marineris.jpg" alt="Mars">
                    <h3>Mars Property</h3>
                    <p>Select your Martian parcel</p>
                </div>
            </div>
        </section>

        <form id="deedForm">
            <div class="form-group">
                <label for="ownerName">Owner's Name (as it should appear on deed):</label>
                <input type="text" id="ownerName" required placeholder="Enter full name">
            </div>
            
            <div class="form-group">
                <label for="planet">Celestial Body:</label>
                <select id="planet" required>
                    <option value="">-- Select Moon or Mars --</option>
                    <option value="moon">Moon (Lunar Surface)</option>
                    <option value="mars">Mars (Martian Surface)</option>
                </select>
            </div>
            
            <div class="form-group">
                <label for="coordinates">Preferred Coordinates (optional):</label>
                <input type="text" id="coordinates" placeholder="e.g., Sea of Tranquility or Olympus Mons Base">
            </div>
            
            <button type="submit">Generate Deed Preview</button>
        </form>

        <div id="deedPreview" class="deed-preview" style="display: none;">
            <h2>Your Novelty Celestial Deed</h2>
            <div class="deed-content" id="deedContent">
                <!-- Deed content will be inserted here -->
            </div>
            <div class="deed-footer">
                <p>Registry Number: LUNAR-<span id="registryNum">XXXXXX</span> | Issued: <span id="issueDate">Date</span></p>
                <p><em>This is a novelty item with no legal validity. For entertainment purposes only.</em></p>
            </div>
        </div>
    </div>

    <script>
        let selectedPlanet = null;
        
        function selectPlanet(planet) {
            selectedPlanet = planet;
            document.getElementById('planet').value = planet;
            // Highlight selected option
            document.querySelectorAll('.planet-option').forEach(opt => {
                opt.style.border = opt.dataset.planet === planet ? '2px solid #ffd700' : 'none';
            });
        }
        
        document.getElementById('deedForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const ownerName = document.getElementById('ownerName').value.trim();
            const planet = document.getElementById('planet').value;
            const coordinates = document.getElementById('coordinates').value || 
                            (planet === 'moon' ? 'Sea of Tranquility' : 'Olympem Mons Region');
            
            if (!ownerName || !planet) {
                alert('Please fill in all required fields');
                return;
            }
            
            // Generate deed content
            const deedContent = `
                <p>This is to certify that</p>
                <h1>${ownerName}</h1>
                <p>has been granted honorary ownership of</p>
                <h2>${planet === 'moon' ? 'One Acre of Lunar Surface' : 'One Hectare of Martian Terrain'}</h2>
                <p>Located at:</p>
                <p><em>${coordinates}</em></p>
                <p>According to the provisions of the <strong>Novelty Space Property Act</strong></p>
                <p>For entertainment and commemorative purposes only</p>
            `;
            
            document.getElementById('deedContent').innerHTML = deedContent;
            document.getElementById('registryNum').textContent = Math.floor(Math.random()*900000)+100000;
            document.getElementById('issueDate').textContent = new Date().toLocaleDateString();
            
            document.getElementById('deedPreview').style.display = 'block';
            window.scrollTo({ top: document.getElementById('deedPreview').offsetTop, behavior: 'smooth' });
        });
    </script>
</body>
</html>
