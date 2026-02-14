<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Donghua Galaxy</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            font-family: 'Arial', sans-serif;
            min-height: 100vh;
            padding: 20px;
        }

        header {
            text-align: center;
            color: white;
            margin-bottom: 40px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        h1 {
            font-size: 3em;
            margin-bottom: 10px;
            animation: fadeIn 1s ease-in;
        }

        .subtitle {
            font-size: 1.2em;
            opacity: 0.9;
        }

        .donghua-cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .donghua-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            transition: all 0.3s ease;
            transform-style: preserve-3d;
            position: relative;
        }

        .donghua-card:hover {
            transform: translateY(-15px) rotateX(5deg);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
        }

        .donghua-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5em;
            font-weight: bold;
            position: relative;
            overflow: hidden;
        }

        .donghua-image::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
            background-size: 20px 20px;
            animation: moveBackground 20s linear infinite;
        }

        @keyframes moveBackground {
            0% { transform: translate(0, 0); }
            100% { transform: translate(20px, 20px); }
        }

        .donghua-content {
            padding: 20px;
        }

        .donghua-title {
            font-size: 1.4em;
            color: #333;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .donghua-description {
            color: #666;
            font-size: 0.9em;
            margin-bottom: 15px;
            line-height: 1.5;
        }

        .episodes-section {
            margin-bottom: 15px;
        }

        .episodes-label {
            font-size: 0.85em;
            color: #667eea;
            font-weight: bold;
            margin-bottom: 8px;
        }

        .episodes-list {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 10px;
        }

        .episode-badge {
            background: #f0f0f0;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8em;
            color: #667eea;
            border: 1px solid #667eea;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .episode-badge:hover {
            background: #667eea;
            color: white;
        }

        .watch-buttons {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .watch-button {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 25px;
            cursor: pointer;
            font-size: 0.95em;
            font-weight: bold;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            text-align: center;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .watch-button:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.6);
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .donghua-card {
            animation: fadeIn 0.6s ease-out forwards;
        }

        .donghua-card:nth-child(1) { animation-delay: 0.1s; }
        .donghua-card:nth-child(2) { animation-delay: 0.2s; }
        .donghua-card:nth-child(3) { animation-delay: 0.3s; }
        .donghua-card:nth-child(4) { animation-delay: 0.4s; }
        .donghua-card:nth-child(5) { animation-delay: 0.5s; }
        .donghua-card:nth-child(6) { animation-delay: 0.6s; }
        .donghua-card:nth-child(7) { animation-delay: 0.7s; }
        .donghua-card:nth-child(8) { animation-delay: 0.8s; }
        .donghua-card:nth-child(9) { animation-delay: 0.9s; }
        .donghua-card:nth-child(10) { animation-delay: 1s; }
        .donghua-card:nth-child(11) { animation-delay: 1.1s; }
        .donghua-card:nth-child(12) { animation-delay: 1.2s; }
        .donghua-card:nth-child(13) { animation-delay: 1.3s; }
        .donghua-card:nth-child(14) { animation-delay: 1.4s; }
        .donghua-card:nth-child(15) { animation-delay: 1.5s; }
        .donghua-card:nth-child(16) { animation-delay: 1.6s; }
        .donghua-card:nth-child(17) { animation-delay: 1.7s; }
        .donghua-card:nth-child(18) { animation-delay: 1.8s; }
        .donghua-card:nth-child(19) { animation-delay: 1.9s; }
        .donghua-card:nth-child(20) { animation-delay: 2s; }
    </style>
</head>
<body>
    <header>
        <h1>🎬 Donghua Episode List</h1>
        <p class="subtitle">Explore the best Donghua series with multiple episodes</p>
    </header>

    <div class="donghua-cards">
        <!-- Card 1 -->
        <div class="donghua-card">
            <div class="donghua-image">https://image2url.com/r2/default/images/1771058156564-d03c61f8-04c4-4822-aec8-6ef6da335fc7.jpg</div>
            <div class="donghua-content">
                <div class="donghua-title">Battle Through The Haven</div>
                <p class="donghua-description">A thrilling journey through the celestial realm with stunning animation.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>https://www.dailymotion.com/video/x9yxge2
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/Heaven%20Officials%20Blessing%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/Heaven%20Officials%20Blessing%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 2 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 2</div>
            <div class="donghua-content">
                <div class="donghua-title">Soul Land</div>
                <p class="donghua-description">An epic adventure in a magical world with breathtaking visuals.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/Soul%20Land%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/Soul%20Land%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 3 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 3</div>
            <div class="donghua-content">
                <div class="donghua-title">Scumbag System</div>
                <p class="donghua-description">A hilarious comedy with intense action scenes and great animation.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/Scumbag%20System%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/Scumbag%20System%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 4 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 4</div>
            <div class="donghua-content">
                <div class="donghua-title">Martial Master</div>
                <p class="donghua-description">Follow the journey of a martial arts master in a stunning 3D world.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/Martial%20Master%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/Martial%20Master%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 5 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 5</div>
            <div class="donghua-content">
                <div class="donghua-title">Perfect World</div>
                <p class="donghua-description">Discover a perfect world filled with mystical creatures and adventures.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/Perfect%20World%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/Perfect%20World%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 6 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 6</div>
            <div class="donghua-content">
                <div class="donghua-title">Grandmaster of Demonic Cultivation</div>
                <p class="donghua-description">An emotional tale of magic, mystery, and profound connections.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/Grandmaster%20of%20Demonic%20Cultivation%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/Grandmaster%20of%20Demonic%20Cultivation%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 7 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 7</div>
            <div class="donghua-content">
                <div class="donghua-title">The King's Avatar</div>
                <p class="donghua-description">Experience the thrilling world of esports and gaming competitions.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/The%20Kings%20Avatar%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/The%20Kings%20Avatar%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 8 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 8</div>
            <div class="donghua-content">
                <div class="donghua-title">Sword Art Online</div>
                <p class="donghua-description">A legendary tale of virtual worlds and epic battles.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/Sword%20Art%20Online%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/Sword%20Art%20Online%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 9 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 9</div>
            <div class="donghua-content">
                <div class="donghua-title">Release That Witch</div>
                <p class="donghua-description">Witness magic, technology, and romance in this captivating series.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/Release%20That%20Witch%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/Release%20That%20Witch%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 10 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 10</div>
            <div class="donghua-content">
                <div class="donghua-title">Heavenly Officials' Blessing 2</div>
                <p class="donghua-description">The continuation of the celestial adventure with even more mystery.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/Heavenly%20Officials%20Blessing%202%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/Heavenly%20Officials%20Blessing%202%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 11 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 11</div>
            <div class="donghua-content">
                <div class="donghua-title">Mo Dao Zu Shi</div>
                <p class="donghua-description">The untamed path of a legendary cultivator and his companions.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
                </div>
                <div class="watch-buttons">
                    <a href="https://www.dailymotion.com/search/Mo%20Dao%20Zu%20Shi%20episode%201" target="_blank" class="watch-button">▶ Watch Episode 1</a>
                    <a href="https://www.dailymotion.com/search/Mo%20Dao%20Zu%20Shi%20episode%202" target="_blank" class="watch-button">▶ Watch Episode 2</a>
                </div>
            </div>
        </div>

        <!-- Card 12 -->
        <div class="donghua-card">
            <div class="donghua-image">Donghua Title 12</div>
            <div class="donghua-content">
                <div class="donghua-title">Thousand Years for Me</div>
                <p class="donghua-description">A timeless romance spanning centuries with gorgeous animation.</p>
                <div class="episodes-section">
                    <div class="episodes-label">Episodes Available:</div>
                    <div class="episodes-list">
                        <span class="episode-badge">Ep 1</span>
                        <span class="episode-badge">Ep 2</span>
                        <span class="episode-badge">Ep 3</span>
                    </div>
      
