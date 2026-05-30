<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LUNAR REGISTRY OFFICE - Official Novelty Celestial Deeds</title>
    //fonts.googleapis.com/css2?family=Times+New+Roman:wght@400;700&family=Courier+New:wght@400;700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --navy: #002147;
            --gold: #ffd700;
            --white: #ffffff;
            --cream: #f8f4e6;
            --dark-gray: #2c3e50;
            --light-gray: #ecf0f1;
            --red: #c41e3a;
        }
        
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'Times New Roman', serif;
            background: linear-gradient(135deg, #000011 0%, #000022 50%, #001133 100%);
            color: var(--white);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 2rem;
            min-height: 100vh;
        }
        
        /* OFFICIAL HEADER */
        header {
            text-align: center;
            padding: 3rem 0;
            border-bottom: 3px double var(--gold);
            margin-bottom: 3rem;
            position: relative;
        }
        
        .official-seal {
            width: 120px;
            height: 120px;
            margin: 0 auto 1.5rem;
            background: var(--white);
            border-radius: 50%;
            border: 3px solid var(--gold);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: relative;
        }
        
        .official-seal::before {
            content: '';
            position: absolute;
            width: 80%;
            height: 80%;
            border: 2px dashed var(--gold);
            border-radius: 50%;
        }
        
        .official-seal .moon-img {
            width: 60px;
            height: 60px;
            background: url('https://upload.wikimedia.org/wikipedia/commons/thumb/8/8d/Moon.jpg/250px-Moon.jpg') center/cover no-repeat;
            border-radius: 50%;
            margin-bottom: 0.5rem;
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.5);
        }
        
        .official-seal text {
            font-family: 'Courier New', monospace;
            font-size: 0.8rem;
            text-align: center;
            line-height: 1.2;
        }
        
        .official-seal text.top { 
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 0.2rem;
        }
        
        .official-seal text.bottom {
            font-size: 0.7rem;
        }
        
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2.8rem;
            font-weight: 700;
            color: var(--gold);
            text-transform: uppercase;
            letter-spacing: 2px;
            margin: 1rem 0;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.3);
        }
        
        .subtitle {
            font-family: 'Courier New', monospace;
            font-size: 1.2rem;
            color: var(--light-gray);
            text-transform: uppercase;
            letter-spacing: 1.5px;
            margin-bottom: 2rem;
        }
        
        /* OFFICIAL DOCUMENT STYLE */
        .document {
            background: var(--cream);
            color: var(--navy);
            border: 2px solid var(--navy);
            border-radius: 0;
            margin: 2rem 0;
            overflow: hidden;
            position: relative;
        }
        
        .document-header {
            background: var(--navy);
            color: var(--gold);
            padding: 1.5rem 2rem;
            border-bottom: 3px solid var(--gold);
        }
        
        .document-header h2 {
            font-family: 'Times New Roman', serif;
            font-size: 1.8rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 0.5rem;
        }
        
        .document-body {
            padding: 2.5rem;
        }
        
        /* FORMAL SECTIONS */
        .formal-section {
            margin: 2rem 0;
            padding: 1.5rem;
            border-left: 3px solid var(--gold);
            background: rgba(255, 215, 0, 0.05);
        }
        
        .formal-section h3 {
            font-family: 'Times New Roman', serif;
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--navy);
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .formal-section h3::before {
            content: "▣";
            color: var(--gold);
        }
        
        /* MOON-FOCUSED DISPLAY */
        .moon-showcase {
            text-align: center;
            margin: 3rem 0;
            padding: 2rem;
            background: rgba(0, 0, 0, 0.3);
            border: 1px solid var(--gold);
            border-radius: 0;
        }
        
        .moon-showcase img {
            width: 250px;
            height: 250px;
            object-fit: cover;
            border: 4px solid var(--gold);
            box-shadow: 0 0 25px rgba(255, 215, 0, 0.4);
            margin-bottom: 1.5rem;
            border-radius: 0;
        }
        
        .moon-details {
            font-family: 'Courier New', monospace;
            font-size: 1.1rem;
            color: var(--light-gray);
            max-width: 600px;
            margin: 0 auto;
            line-height: 1.8;
        }
        
        /* OFFICIAL BUTTONS */
        .official-btn {
            display: inline-block;
            background: var(--navy);
            color: var(--gold);
            text-decoration: none;
            font-family: 'Times New Roman', serif;
            font-weight: 700;
            font-size: 1.1rem;
            padding: 1rem 2.5rem;
            border: 2px solid var(--gold);
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .official-btn:hover {
            background: var(--gold);
            color: var(--navy);
            box-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
            transform: translateY(-2px);
        }
        
        .official-btn:active {
            transform: translateY(0);
        }
        
        .official-btn::before {
            content: '';
            position: absolute;
            top: -50%; left: -50%;
            width: 200%; height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,215,0,0.1), transparent);
            transform: rotate(45deg);
            transition: all 0.5s;
        }
        
        .official-btn:hover::before {
            transform: rotate(45deg) translateX(100%);
        }
        
        /* PRODUCT DISPLAY - OFFICIAL STYLE */
        .official-products {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }
        
        .official-product {
            border: 2px solid var(--navy);
            background: rgba(0, 0, 0, 0.2);
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
        }
        
        .official-product:hover {
            border-color: var(--gold);
            background: rgba(0, 0, 0, 0.4);
            transform: translateY(-5px);
        }
        
        .official-product h3 {
            font-family: 'Times New Roman', serif;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--gold);
            text-transform: uppercase;
            margin-bottom: 1.5rem;
        }
        
        .moon-product img {
            width: 180px;
            height: 180px;
            object-fit: cover;
            border: 3px solid var(--gold);
            margin: 1rem 0;
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.3);
        }
        
        .mars-product img {
            width: 180px;
            height: 180px;
            object-fit: cover;
            border: 3px solid var(--red);
            margin: 1rem 0;
            box-shadow: 0 0 15px rgba(196, 30, 58, 0.3);
        }
        
        .official-product .price {
            font-family: 'Courier New', monospace;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--gold);
            background: var(--navy);
            display: inline-block;
            padding: 0.5rem 1.5rem;
            border: 2px solid var(--gold);
            margin: 1.5rem 0;
        }
        
        .official-product p {
            font-size: 1rem;
            color: var(--light-gray);
            margin-bottom: 1.5rem;
            line-height: 1.6;
        }
        
        /* OFFICIAL DEED PREVIEW */
        .deed-certificate {
            background: var(--cream);
            border: 3px solid var(--navy);
            padding: 3rem;
            margin: 2rem 0;
            position: relative;
            min-height: 500px;
        }
        
        .deed-certificate::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; height: 8px;
            background: repeating-linear-gradient(
                90deg,
                var(--navy),
                var(--navy) 10px,
                var(--gold) 10px,
                var(--gold) 20px
            );
        }
        
        .deed-certificate::after {
            content: '';
            position: absolute;
            bottom: 0; left: 0; right: 0; height: 8px;
            background: repeating-linear-gradient(
                90deg,
                var(--navy),
                var(--navy) 10px,
                var(--gold) 10px,
                var(--gold) 20px
            );
        }
        
        .deed-seal {
            position: absolute;
            top: -30px; right: -30px;
            width: 100px;
            height: 100px;
            background: var(--white);
            border: 3px solid var(--gold);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.7rem;
            text-align: center;
            line-height: 1.2;
        }
        
        .deed-seal div {
            font-family: 'Courier New', monospace;
            font-weight: 700;
        }
        
        .deed-content {
            text-align: center;
            font-family: 'Times New Roman', serif;
        }
        
        .deed-content p {
            margin: 1.5rem 0;
            font-size: 1.2rem;
            color: var(--navy);
        }
        
        .deed-content h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2.8rem;
            font-weight: 700;
            color: var(--navy);
            margin: 1.5rem 0;
            letter-spacing: -1px;
        }
        
        .deed-content h2 {
            font-family: 'Times New Roman', serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--navy);
            margin: 1.5rem 0;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .deed-footer {
            margin-top: 3rem;
            font-size: 0.9rem;
            color: var(--dark-gray);
            border-top: 1px solid var(--navy);
            padding-top: 1.5rem;
        }
        
        .deed-footer .official-note {
            font-family: 'Courier New', monospace;
            font-size: 0.8rem;
            text-align: center;
            margin-top: 1rem;
            color: var(--red);
            font-style: italic;
        }
        
        /* FORM STYLE - OFFICIAL */
        .official-form {
            background: rgba(0, 0, 0, 0.2);
            border: 2px solid var(--navy);
            padding: 2.5rem;
            margin: 2rem 0;
        }
        
        .official-form h2 {
            font-family: 'Times New Roman', serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--gold);
            text-align: center;
            margin-bottom: 2rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .form-group {
            margin: 1.5rem 0;
        }
        
        .form-group label {
            display: block;
            font-family: 'Times New Roman', serif;
            font-weight: 700;
            color: var(--white);
            margin-bottom: 0.5rem;
        }
        
        .form-group input {
            width: 100%;
            padding: 0.75rem;
            border: 2px solid var(--gold);
            background: rgba(0, 0, 0, 0.3);
            color: var(--white);
            font-family: 'Courier New', monospace;
            font-size: 1rem;
            border-radius: 0;
        }
        
        .form-group input:focus {
            outline: none;
            border-color: var(--white);
            box-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
        }
        
        /* FOOTER */
        footer {
            text-align: center;
            padding: 3rem 0;
            border-top: 1px solid var(--gold);
            margin-top: 4rem;
            font-size: 0.9rem;
            color: var(--light-gray);
        }
        
        .footer-links {
            margin: 1.5rem 0;
        }
        
        .footer-links a {
            color: var(--gold);
            text-decoration: none;
            margin: 0 1rem;
            font-family: 'Courier New', monospace;
        }
        
        .footer-links a:hover {
            text-decoration: underline;
        }
        
        /* RESPONSIVE */
        @media (max-width: 768px) {
            .container { padding: 1rem; }
            h1 { font-size: 2.2rem; }
            .official-products { grid-template-columns: 1fr; }
            .moon-showcase img { width: 200px; height: 200px; }
            .deed-certificate { padding: 2rem; }
        }
        
        @media (max-width: 480px) {
            h1 { font-size: 1.8rem; }
            .official-seal { width: 80px; height: 80px; }
            .official-seal .moon-img { width: 40px; height: 40px; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- OFFICIAL HEADER -->
        <header>
            <div class="official-seal">
                <div class="moon-img"></div>
                <div class="text top">LUNAR REGISTRY</div>
                <div class="text bottom">OFFICIAL NOVELTY DOCUMENTS</div>
            </div>
            <h1>DEPARTMENT OF EXTRATERRESTRIAL PROPERTY</h1>
            <p class="subtitle">Official Novelty Celestial Property Registry • Established 2026</p>
        </header>

        <!-- MOON SHOWCASE -->
        <section class="moon-showcase">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/8d/Moon.jpg/400px-Moon.jpg" 
                 alt="Official Lunar Surface Image" 
                 title="Mare Tranquillitatis - Sea of Tranquility">
            <div class="moon-details">
                <strong>OFFICIAL LUNAR REGISTRY NOTICE:</strong> All deeds registered through this office commemorate humanity's peaceful exploration of space. The moon imagery featured represents Mare Tranquillitatis (Sea of Tranquility), site of humanity's first lunar landing. These documents are novelty items commemorating space exploration achievements.
            </div>
        </section>

        <!-- MAIN CONTENT -->
        <main>
            <!-- OFFICIAL DISCLAIMER -->
            <section class="document">
                <div class="document-header">
                    <h2>§ 1. OFFICIAL NOTICE & LEGAL DISCLAIMER</h2>
                    <p>Pursuant to the Treaty on Principles Governing the Activities of States in the Exploration and Use of Outer Space, including the Moon and Other Celestial Bodies (Outer Space Treaty, 1967)</p>
                </div>
                <div class="document-body">
                    <div class="formal-section">
                        <h3>⚠ REGISTRY ADVISORY ⚠</h3>
                        <p><strong>THIS IS A NOVELTY REGISTRY ONLY.</strong> Under international space law, including the Outer Space Treaty of 1967 and subsequent agreements, no nation may claim sovereignty over celestial bodies, and therefore no individual may own land on the moon, Mars, or other space bodies.</p>
                        <p>All documents issued by the Lunar Registry Office are <em>novelty items</em> intended strictly for entertainment, commemorative, or educational purposes. They confer no actual property rights, ownership interests, development privileges, or access rights to any celestial body.</p>
                    </div>
                    
                    <div class="formal-section">
                        <h3>📜 OFFICIAL PURPOSE 📜</h3>
                        <p>This registry commemorates humanity's achievements in space exploration and serves as a novelty commemorative service for enthusiasts of lunar and Martian exploration. All registrations are recorded in our novelty registry database for commemorative purposes only.</p>
                    </div>
                </div>
            </section>

            <!-- OFFICIAL PRODUCTS -->
            <section class="official-products">
                <!-- Moon Product -->
                <div class="official-product moon-product" data-planet="moon">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/8d/Moon.jpg/250px-Moon.jpg" 
                         alt="Official Lunar Surface" 
                         title="Mare Tranquillitatis - Lunar Registry Sector">
                    <h3>LUNAR PROPERTY DEED</h3>
                    <p>Official novelty deed commemorating one acre of lunar surface. Each deed features personalized coordinates from historic lunar regions and an official registry number.</p>
                    <div class="price">$49.99</div>
                    <button class="official-btn" onclick="selectPlanet('moon')">REGISTER LUNAR PARCEL</button>
                </div>
                
                <!-- Mars Product -->
                <div class="official-product mars-product" data-planet="mars">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/02/Mars_Valles_Marineris.jpg/250px-Mars_Valles_Marineris.jpg" 
                         alt="Official Mars Surface" 
                         title="Valles Marineris - Martian Registry Zone">
                    <h3>MARTIAN PROPERTY DEED</h3>
                    <p>Official novelty deed commemorating one hectare of Martian terrain. Features coordinates from notable Martian regions and an official registry number.</p>
                    <div class="price">$49.99</div>
                    <button class="official-btn" onclick="selectPlanet('mars')">REGISTER MARTIAN PARCEL</button>
                </div>
            </section>
        </main>

        <!-- FORM SECTION -->
        <section id="formSection" class="official-form" style="display: none;">
            <h2>REGISTER YOUR <span id="regType"></span> PARCEL</h2>
            
            <form id="registrationForm">
                <div class="form-group">
                    abel for="registrantName">REGISTRANT NAME (AS IT SHOULD APPEAR ON DEED):</label>
                    <input type="text" id="registrantName" required 
                           placeholder="ENTER FULL LEGAL NAME FOR OFFICIAL REGISTRY">
                </div>
                
                <div class="form-group">
                    abel for="locationPreference">PREFERRED LUNAR REGION (OPTIONAL):</label>
                    <input type="text" id="locationPreference" 
                           placeholder="E.G., MARE TRANQUILLITATIS, OCEANUM PROCELLARUM, OR LEAVE BLANK FOR ASSIGNED SECTOR">
                </div>
                
                <div style="text-align: center; margin: 2.5rem 0;">
                    <button type="submit" class="official-btn">GENERATE OFFICIAL DEED PREVIEW</button>
                    <button type="button" class="official-btn" onclick="resetRegistration()" 
                            style="background: var(--dark-gray); border-color: var(--dark-gray); margin-left: 1rem;">
                        CANCEL REGISTRATION
                    </button>
                </div>
            </form>
        </section>

        <!-- OFFICIAL DEED CERTIFICATE -->
        <section id="deedCertificate" class="deed-certificate" style="display: none;">
            <div class="deed-seal">
                <div>LUNAR</div>
                <div>REGISTRY</div>
                <div>SEAL</div>
            </div>
            
            <div class="deed-content">
                <p>THIS IS TO CERTIFY THAT THE LUNAR REGISTRY OFFICE</p>
                <h1 id="registrantDisplay"></h1>
                <p>HAS BEEN GRANTED HONORARY REGISTRATION OF</p>
                <h2 id="propertyType"></h2>
                <p>LOCATED AT THE FOLLOWING OFFICIAL COORDINATES:</p>
                <p style="font-size: 1.4rem; font-weight: 700; letter-spacing: 2px; 
                         background: var(--navy); color: var(--gold); 
                         display: inline-block; padding: 0.5rem 1.5rem; 
                         margin: 1.5rem 0; border: 2px solid var(--gold);">
                    <span id="coordinatesDisplay">SECTOR TO BE ASSIGNED</span>
                </p>
                <p>ACCORDING TO THE PROVISIONS OF THE <br>NOVELTY CELESTIAL PROPERTY ACT OF 2026</p>
                <p>FOR COMMEMORATIVE AND ENTERTAINMENT PURPOSES ONLY</p>
            </div>
            
            <div class="deed-footer">
                <p>REGISTRY NUMBER: <span id="registryNumber">LR-XXXXXX</span> | 
                   DATE OF ISSUE: <span id="issueDate">DATE</span> | 
                   OFFICIAL FEE: $49.99</p>
                <p class="official-note">⚠ THIS IS A NOVELTY DOCUMENT WITHOUT LEGAL EFFECT OR VALUE. NO ACTUAL PROPERTY RIGHTS ARE CONVEYED.</p>
                <div style="text-align: center; margin-top: 2rem;">
                    <button class="official-btn" onclick="window.print()" style="background: var(--dark-gray); border-color: var(--dark-gray);">
                        PRINT OFFICIAL COPY
                    </button>
                    <button class="official-btn" onclick="resetRegistration()" 
                            style="margin-left: 1rem; background: var(--dark-gray); border-color: var(--dark-gray);">
                        REGISTER ANOTHER PARCEL
                    </button>
                </div>
            </div>
        </section>
    </div>

    <script>
        let selectedPlanet = null;
        let regType = '';
        
        function selectPlanet(planet) {
            selectedPlanet = planet;
            regType = planet === 'moon' ? 'LUNAR' : 'MARTIAN';
            
            // Show registration form
            document.getElementById('formSection').style.display = 'block';
            document.getElementById('regType').textContent = regType;
            
            // Hide main content
            document.querySelector('main').style.display = 'none';
        }
        
        document.getElementById('registrationForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const registrantName = document.getElementById('registrantName').value.trim();
            const locationPreference = document.getElementById('locationPreference').value.trim();
            
            if (!registrantName) {
                alert('PLEASE ENTER REGISTRANT NAME FOR OFFICIAL REGISTRY');
                return;
            }
            
            // Update deed display
            document.getElementById('registrantDisplay').textContent = registrantName;
            document.getElementById('propertyType').textContent = 
                selectedPlanet === 'moon' ? 'ONE ACRE OF LUNAR SURFACE' : 'ONE HECTARE OF MARTIAN TERRAIN';
            
            const coordinates = locationPreference || 
                              (selectedPlanet === 'moon' ? 'MARE TRANQUILLITATIS SECTOR ALPHA-7' : 'VALLIS MARINERIS SECTOR GAMMA-3');
            document.getElementById('coordinatesDisplay').textContent = coordinates;
            
            // Generate registry number
            const registryNum = 'LR-' + Math.floor(Math.random()*900000)+100000;
            document.getElementById('registryNumber').textContent = registryNum;
            
            // Format date
            const options = { year: 'numeric', month: 'long', day: 'numeric' };
            document.getElementById('issueDate').textContent = new Date().toLocaleDateString(undefined, options);
            
            // Show deed certificate
            document.getElementById('formSection').style.display = 'none';
            document.getElementById('deedCertificate').style.display = 'block';
        });
        
        function resetRegistration() {
            document.getElementById('registrationForm').reset();
            document.getElementById('formSection').style.display = 'none';
            document.getElementById('deedCertificate').style.display = 'none';
            document.querySelector('main').style.display = 'block';
            selectedPlanet = null;
        }
    </script>
</body>
</html>
