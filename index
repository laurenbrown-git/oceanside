<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Oceanside Travel Itinerary</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            padding: 40px;
            text-align: center;
            color: white;
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }

        .header .dates {
            font-size: 1.3em;
            font-weight: 300;
        }

        .content {
            padding: 40px;
        }

        .destination-header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 15px;
        }

        .destination-header h2 {
            color: #667eea;
            font-size: 2em;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .destination-header h2::before {
            content: "📍";
            margin-right: 10px;
        }

        .day-card {
            margin-bottom: 25px;
            background: #f8f9fa;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            border-left: 5px solid #4facfe;
        }

        .day-header {
            padding: 20px;
            background: white;
            cursor: pointer;
            transition: all 0.3s ease;
            display: grid;
            grid-template-columns: 1fr auto;
            gap: 20px;
            align-items: center;
        }

        .day-header:hover {
            background: #e3f2fd;
        }

        .day-info {
            display: flex;
            flex-direction: column;
            gap: 5px;
        }

        .day-title {
            font-size: 1.4em;
            font-weight: 600;
            color: #667eea;
        }

        .day-date {
            color: #666;
            font-size: 1em;
        }

        .weather-info {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 15px 20px;
            background: linear-gradient(135deg, #ffeaa7 0%, #fdcb6e 100%);
            border-radius: 10px;
        }

        .weather-icon {
            font-size: 2.5em;
        }

        .weather-details {
            display: flex;
            flex-direction: column;
            gap: 3px;
        }

        .temperature {
            font-size: 1.4em;
            font-weight: bold;
            color: #2d3436;
        }

        .conditions {
            color: #636e72;
            font-size: 0.95em;
        }

        .toggle-arrow {
            font-size: 1.2em;
            color: #4facfe;
            transition: transform 0.3s ease;
            grid-column: 2;
            grid-row: 1 / 3;
            align-self: center;
        }

        .day-header.active .toggle-arrow {
            transform: rotate(180deg);
        }

        .collapsible-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s ease, opacity 0.3s ease;
            opacity: 0;
        }

        .collapsible-content.active {
            max-height: 2000px;
            opacity: 1;
        }

        .day-content {
            padding: 20px;
        }

        .section-title {
            color: #555;
            font-size: 1.1em;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .activities {
            list-style: none;
            margin-bottom: 15px;
        }

        .activities li {
            padding: 12px 15px;
            margin: 8px 0;
            background: white;
            border-radius: 8px;
            border-left: 3px solid #00f2fe;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s;
        }

        .activities li:hover {
            transform: translateX(5px);
        }

        .activities li::before {
            content: "✓";
            color: #4facfe;
            font-weight: bold;
            margin-right: 10px;
        }

        /* Dining Section Styles */
        .dining-section {
            margin-top: 40px;
            background: linear-gradient(135deg, #fff5f5 0%, #ffe8e8 100%);
            border-radius: 15px;
            padding: 30px;
            border-left: 5px solid #ff6b6b;
        }

        .dining-header {
            text-align: center;
            margin-bottom: 25px;
        }

        .dining-header h3 {
            font-size: 2em;
            color: #c92a2a;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .restaurant-card {
            background: white;
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 15px;
            box-shadow: 0 3px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s, box-shadow 0.2s;
            border-left: 4px solid #ff6b6b;
        }

        .restaurant-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.15);
        }

        .restaurant-name {
            font-size: 1.3em;
            font-weight: 700;
            color: #c92a2a;
            margin-bottom: 8px;
        }

        .restaurant-description {
            color: #495057;
            line-height: 1.6;
            margin-bottom: 12px;
        }

        .restaurant-link {
            display: inline-block;
            color: #4facfe;
            text-decoration: none;
            font-weight: 600;
            margin-bottom: 8px;
            transition: color 0.2s;
        }

        .restaurant-link:hover {
            color: #0984e3;
            text-decoration: underline;
        }

        .restaurant-link::before {
            content: "🌐 ";
        }

        .restaurant-location {
            color: #6c757d;
            font-size: 0.95em;
            font-style: italic;
        }

        .restaurant-location::before {
            content: "📍 ";
        }

        .notes {
            background: #fff9e6;
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #ffc107;
            margin-top: 30px;
        }

        .notes::before {
            content: "📝 ";
            font-size: 1.2em;
        }

        .notes strong {
            color: #f57c00;
        }

        .footer {
            text-align: center;
            padding: 20px;
            background: #f8f9fa;
            color: #777;
            font-size: 0.9em;
        }

        @media (max-width: 600px) {
            .header h1 {
                font-size: 1.8em;
            }

            .header .dates {
                font-size: 1.1em;
            }

            .content {
                padding: 20px;
            }

            .day-header {
                grid-template-columns: 1fr;
            }

            .weather-info {
                flex-direction: column;
                text-align: center;
            }

            .toggle-arrow {
                grid-column: 1;
                grid-row: 3;
                justify-self: center;
                margin-top: 10px;
            }

            .dining-section {
                padding: 20px;
            }

            .dining-header h3 {
                font-size: 1.5em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🌴 Oceanside Beach Getaway 🌴</h1>
            <div class="dates">March 18 - March 22, 2026</div>
        </div>

        <div class="content">
            <div class="destination-header">
                <h2>Oceanside, California</h2>
            </div>

            <!-- Day 1 -->
            <div class="day-card">
                <div class="day-header" onclick="toggleDay(this)">
                    <div class="day-info">
                        <div class="day-title">Day 1</div>
                        <div class="day-date">Wednesday, March 18</div>
                    </div>
                    <div class="weather-info">
                        <div class="weather-icon">☀️</div>
                        <div class="weather-details">
                            <div class="temperature">72°F</div>
                            <div class="conditions">Sunny</div>
                        </div>
                    </div>
                    <div class="toggle-arrow">▼</div>
                </div>
                <div class="collapsible-content">
                    <div class="day-content">
                        <div class="section-title">🎯 Activities:</div>
                        <ul class="activities">
                            <li>Arrival and check-in at the condo</li>
                            <li>Beach time</li>
                            <li>Explore the Oceanside Pier</li>
                            <li>Dinner at a local restaurant</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Day 2 -->
            <div class="day-card">
                <div class="day-header" onclick="toggleDay(this)">
                    <div class="day-info">
                        <div class="day-title">Day 2</div>
                        <div class="day-date">Thursday, March 19</div>
                    </div>
                    <div class="weather-info">
                        <div class="weather-icon">🌤️</div>
                        <div class="weather-details">
                            <div class="temperature">70°F</div>
                            <div class="conditions">Partly Cloudy</div>
                        </div>
                    </div>
                    <div class="toggle-arrow">▼</div>
                </div>
                <div class="collapsible-content">
                    <div class="day-content">
                        <div class="section-title">🎯 Activities:</div>
                        <ul class="activities">
                            <li>Morning beach time</li>
                            <li>Visit Oceanside Harbor</li>
                            <li>Lunch by the water</li>
                            <li>Explore local shops and attractions</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Day 3 -->
            <div class="day-card">
                <div class="day-header" onclick="toggleDay(this)">
                    <div class="day-info">
                        <div class="day-title">Day 3</div>
                        <div class="day-date">Friday, March 20</div>
                    </div>
                    <div class="weather-info">
                        <div class="weather-icon">☀️</div>
                        <div class="weather-details">
                            <div class="temperature">74°F</div>
                            <div class="conditions">Sunny</div>
                        </div>
                    </div>
                    <div class="toggle-arrow">▼</div>
                </div>
                <div class="collapsible-content">
                    <div class="day-content">
                        <div class="section-title">🎯 Activities:</div>
                        <ul class="activities">
                            <li>Full day at the beach</li>
                            <li>Beach games and activities with the kids</li>
                            <li>Beachside lunch</li>
                            <li>Evening stroll along the coast</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Day 4 -->
            <div class="day-card">
                <div class="day-header" onclick="toggleDay(this)">
                    <div class="day-info">
                        <div class="day-title">Day 4</div>
                        <div class="day-date">Saturday, March 21</div>
                    </div>
                    <div class="weather-info">
                        <div class="weather-icon">⛅</div>
                        <div class="weather-details">
                            <div class="temperature">68°F</div>
                            <div class="conditions">Mostly Sunny</div>
                        </div>
                    </div>
                    <div class="toggle-arrow">▼</div>
                </div>
                <div class="collapsible-content">
                    <div class="day-content">
                        <div class="section-title">🎯 Activities:</div>
                        <ul class="activities">
                            <li>Morning beach time</li>
                            <li>Visit California Surf Museum</li>
                            <li>Explore downtown Oceanside</li>
                            <li>Farewell dinner</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Day 5 -->
            <div class="day-card">
                <div class="day-header" onclick="toggleDay(this)">
                    <div class="day-info">
                        <div class="day-title">Day 5</div>
                        <div class="day-date">Sunday, March 22</div>
                    </div>
                    <div class="weather-info">
                        <div class="weather-icon">☀️</div>
                        <div class="weather-details">
                            <div class="temperature">71°F</div>
                            <div class="conditions">Clear</div>
                        </div>
                    </div>
                    <div class="toggle-arrow">▼</div>
                </div>
                <div class="collapsible-content">
                    <div class="day-content">
                        <div class="section-title">🎯 Activities:</div>
                        <ul class="activities">
                            <li>Final beach morning</li>
                            <li>Pack and check out</li>
                            <li>Departure</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Dining Section -->
            <div class="dining-section">
                <div class="dining-header">
                    <h3>🍽️ Dining Options</h3>
                </div>

                <div class="restaurant-card">
                    <div class="restaurant-name">Stratford at the Harbor</div>
                    <div class="restaurant-description">Classic breakfast/lunch with harbor views; very family-friendly.</div>
                    <a href="https://stratfordharbor.com/" target="_blank" class="restaurant-link">Visit Website</a>
                </div>

                <div class="restaurant-card">
                    <div class="restaurant-name">Oceanside Broiler</div>
                    <div class="restaurant-description">Waterfront seafood & American fare with a kids' menu and marina views.</div>
                    <a href="https://www.oceanside-broiler.com/" target="_blank" class="restaurant-link">Visit Website</a>
                </div>

                <div class="restaurant-card">
                    <div class="restaurant-name">Harbor Fish & Chips</div>
                    <div class="restaurant-description">Casual counter-service fish & chips; easy post-beach option for kids.</div>
                    <a href="https://harborfishandchips.com/" target="_blank" class="restaurant-link">Visit Website</a>
                </div>

                <div class="restaurant-card">
                    <div class="restaurant-name">Hello Betty</div>
                    <div class="restaurant-description">Fun beachy vibe with rooftop deck, great for fish tacos, burgers, and casual family meals.</div>
                    <a href="https://www.hellobettyoceanside.com/" target="_blank" class="restaurant-link">Visit Website</a>
                    <div class="restaurant-location">211 Mission Ave (by the pier; 3–5 min drive / ~15–20 min walk down the Strand)</div>
                </div>

                <div class="restaurant-card">
                    <div class="restaurant-name">High/Low (Seabird Resort)</div>
                    <div class="restaurant-description">Bright, modern, very family-friendly breakfast & lunch with ocean views; easy to walk up from the beach.</div>
                    <a href="https://www.highlowoceanside.com/" target="_blank" class="restaurant-link">Visit Website</a>
                    <div class="restaurant-location">101 Mission Ave (Seabird Resort, just inland from the pier)</div>
                </div>

                <div class="restaurant-card">
                    <div class="restaurant-name">Zigzag Pizza</div>
                    <div class="restaurant-description">Fast-casual pizza, salads, and pastas; easy with kids and close to the pier.</div>
                    <a href="https://www.zigzagpizza.com/" target="_blank" class="restaurant-link">Visit Website</a>
                    <div class="restaurant-location">333 N Myers St, Oceanside / 714 N Coast Hwy (3–4 min drive / 10–15 min walk inland)</div>
                </div>

                <div class="restaurant-card">
                    <div class="restaurant-name">Swami's Café – Oceanside</div>
                    <div class="restaurant-description">Healthy-ish, beach-casual spot with smoothies, pancakes, bowls, and a very relaxed vibe.</div>
                    <a href="https://swamiscafe.com/oceanside/" target="_blank" class="restaurant-link">Visit Website</a>
                    <div class="restaurant-location">608 Mission Ave, Oceanside</div>
                </div>
            </div>

            <div class="notes">
                <strong>Accommodation Details:</strong><br>
                Staying at our condo on the strip with 3 adults and 2 kids
            </div>
        </div>

        <div class="footer">
            Have a wonderful trip! 🌊☀️
        </div>
    </div>

    <script>
        function toggleDay(header) {
            const content = header.nextElementSibling;
            const isActive = header.classList.contains('active');
            
            // Close all other days
            document.querySelectorAll('.day-header').forEach(h => {
                h.classList.remove('active');
                h.nextElementSibling.classList.remove('active');
            });
            
            // Toggle current day
            if (!isActive) {
                header.classList.add('active');
                content.classList.add('active');
            }
        }
    </script>
</body>
</html>
