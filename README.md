
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday, Alisha!</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&family=Pacifico&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 1rem;
            overflow: hidden; /* Prevent scrollbar from animated background */
            
            /* BEAUTIFUL ANIMATED BACKGROUND GRADIENT */
            background: linear-gradient(45deg, #ffc0cb, #e0b0ff, #c3f2e1, #ffecb3);
            background-size: 400% 400%;
            animation: gradientShift 20s ease infinite;
        }

        /* Keyframe for the shifting gradient */
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Custom styling for the celebration card */
        .celebration-card {
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25), 0 0 40px rgba(255, 105, 180, 0.4);
            transition: all 0.5s ease-in-out;
            max-width: 95%;
            width: 500px;
            min-height: 600px; 
            z-index: 10; /* Bring card above background elements */
        }
        
        /* Style for individual content sections */
        .content-section {
            opacity: 0;
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            transition: opacity 0.7s ease-in-out, transform 0.7s ease-in-out;
            transform: scale(0.95);
        }

        .content-section.active {
            opacity: 1;
            position: relative;
            transform: scale(1);
        }

        /* Festive Button Style */
        .festive-button {
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        .festive-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -4px rgba(0, 0, 0, 0.1);
        }

        .title-pacifico {
            font-family: 'Pacifico', cursive;
        }
        
        /* FALLING HEART ANIMATION STYLES */
        .falling-heart {
            position: absolute;
            font-size: 24px; /* Default heart size */
            pointer-events: none;
            z-index: 0;
            opacity: 0;
            line-height: 1; /* Ensure emoji size is consistent */
            animation: fallHearts linear infinite;
        }

        @keyframes fallHearts {
            0% { transform: translateY(-50vh) rotate(0deg); opacity: 0.5; }
            100% { transform: translateY(150vh) rotate(360deg); opacity: 0; }
        }

        /* Individual heart variations (for a diverse, staggered look) */
        .falling-heart:nth-child(1) { left: 10%; animation-duration: 18s; animation-delay: 0s; font-size: 20px; }
        .falling-heart:nth-child(2) { left: 20%; animation-duration: 22s; animation-delay: 2s; font-size: 16px; }
        .falling-heart:nth-child(3) { left: 35%; animation-duration: 15s; animation-delay: 4s; font-size: 28px; }
        .falling-heart:nth-child(4) { left: 50%; animation-duration: 20s; animation-delay: 6s; font-size: 24px; }
        .falling-heart:nth-child(5) { left: 65%; animation-duration: 17s; animation-delay: 8s; font-size: 22px; }
        .falling-heart:nth-child(6) { left: 80%; animation-duration: 25s; animation-delay: 10s; font-size: 18px; }
        .falling-heart:nth-child(7) { left: 90%; animation-duration: 19s; animation-delay: 12s; font-size: 26px; }
    </style>
</head>
<body>

    <!-- Falling Heart Animation Elements -->
    <span class="falling-heart">❤️</span>
    <span class="falling-heart">❤️</span>
    <span class="falling-heart">❤️</span>
    <span class="falling-heart">❤️</span>
    <span class="falling-heart">❤️</span>
    <span class="falling-heart">❤️</span>
    <span class="falling-heart">❤️</span>
    
    <div id="celebration-card" class="celebration-card bg-white rounded-3xl p-6 md:p-10 relative overflow-hidden">
        
        <!-- Content Sections Container -->
        <div id="content-container" class="relative w-full h-full">

            <!-- Section 1: The Invitation / Cover -->
            <section class="content-section text-center p-4 active" data-index="0">
                <div class="flex flex-col items-center justify-center h-full">
                    <h1 class="text-6xl title-pacifico text-pink-600 mb-6 animate-pulse">
                        🎉 Happy Birthday! 🎉
                    </h1>
                    <h2 class="text-4xl font-bold text-purple-700 mb-4">
                        A Grand Celebration
                    </h2>
                    <p class="text-xl text-gray-600">
                        Dear Alisha, open this digital card to begin a special journey dedicated just to you.
                    </p>
                </div>
            </section>

            <!-- Section 2: The Toast / To the Brightest Star -->
            <section class="content-section p-4" data-index="1">
                <h2 class="text-4xl font-extrabold text-pink-500 mb-4 border-b-2 pb-2 border-pink-200">
                    🥂 To the Brightest Star
                </h2>
                <p class="text-gray-700 text-lg mb-4">
                    Alisha, your **kindness** is a light that brightens every room you enter. You have an incredible gift for making others feel seen and valued.
                </p>
                <p class="text-gray-700 text-lg">
                    This year, we celebrate your unwavering **optimism** and the sheer joy you bring into our lives. You truly are one of a kind.
                </p>
                <img src="https://placehold.co/400x200/fecaca/9d174d?text=Radiant+Alisha" onerror="this.onerror=null; this.src='https://placehold.co/400x200/fecaca/9d174d?text=Radiant+Alisha';" alt="Placeholder graphic of a radiant light" class="w-full h-32 object-cover rounded-xl mt-6 shadow-md">
            </section>

            <!-- Section 3: The Journey / A Year of Amazing Feats -->
            <section class="content-section p-4" data-index="2">
                <h2 class="text-4xl font-extrabold text-purple-600 mb-4 border-b-2 pb-2 border-purple-200">
                    🚀 A Year of Amazing Feats
                </h2>
                <p class="text-gray-700 text-lg mb-4">
                    Look back at everything you accomplished! Whether it was conquering a tough challenge at work or mastering a new hobby, your **determination** shone through.
                </p>
                <div class="space-y-3 p-4 bg-purple-50 rounded-xl">
                    <p class="font-semibold text-purple-800">🌟 Growth: You never stop learning.</p>
                    <p class="font-semibold text-purple-800">💡 Resilience: Bouncing back stronger every time.</p>
                </div>
                <p class="text-gray-700 text-lg mt-4">
                    You inspire us all to push our boundaries and embrace new experiences.
                </p>
            </section>

            <!-- Section 4: The Gallery / Moments We Cherish -->
            <section class="content-section p-4" data-index="3">
                <h2 class="text-4xl font-extrabold text-teal-600 mb-4 border-b-2 pb-2 border-teal-200">
                    📸 Moments We Cherish
                </h2>
                <p class="text-gray-700 text-lg mb-6">
                    Here's a glimpse of the great times and laughter we've shared. May we create many more!
                </p>
                <div class="grid grid-cols-2 gap-4">
                    <img src="https://placehold.co/200x200/b2f5ea/065f46?text=Laughter" onerror="this.onerror=null; this.src='https://placehold.co/200x200/b2f5ea/065f46?text=Laughter';" alt="Placeholder memory image 1" class="w-full h-24 object-cover rounded-lg shadow-lg transform rotate-2">
                    <img src="https://placehold.co/200x200/f9bc8f/9a3412?text=Adventure" onerror="this.onerror=null; this.src='https://placehold.co/200x200/f9bc8f/9a3412?text=Adventure';" alt="Placeholder memory image 2" class="w-full h-24 object-cover rounded-lg shadow-lg transform -rotate-2">
                    <img src="https://placehold.co/200x200/c7d2fe/3730a3?text=Friends" onerror="this.onerror=null; this.src='https://placehold.co/200x200/c7d2fe/3730a3?text=Friends';" alt="Placeholder memory image 3" class="w-full h-24 object-cover rounded-lg shadow-lg transform translate-y-1">
                    <img src="https://placehold.co/200x200/fed7aa/ea580c?text=Celebration" onerror="this.onerror=null; this.src='https://placehold.co/200x200/fed7aa/ea580c?text=Celebration';" alt="Placeholder memory image 4" class="w-full h-24 object-cover rounded-lg shadow-lg transform -translate-y-1">
                </div>
            </section>

            <!-- Section 5: The Heartfelt Wish / Our Deepest Hopes -->
            <section class="content-section p-4" data-index="4">
                <h2 class="text-4xl font-extrabold text-indigo-700 mb-4 border-b-2 pb-2 border-indigo-200">
                    💖 Our Deepest Hopes
                </h2>
                <p class="text-gray-700 text-lg mb-4">
                    For the year ahead, we wish you:
                </p>
                <ul class="list-disc list-inside text-gray-800 text-xl space-y-2 ml-4">
                    <li class="font-medium text-indigo-500">Unending **happiness** and peace.</li>
                    <li class="font-medium text-indigo-500">The **courage** to follow your biggest dreams.</li>
                    <li class="font-medium text-indigo-500">More laughter and great **adventures**.</li>
                </ul>
                <p class="text-gray-700 text-lg mt-6">
                    May your path be filled with success and beautiful surprises.
                </p>
            </section>

            <!-- Section 6: The Dedication / A Special Message -->
            <section class="content-section p-4" data-index="5">
                <h2 class="text-4xl font-extrabold text-red-500 mb-4 border-b-2 pb-2 border-red-200">
                    📜 A Special Message
                </h2>
                <div class="bg-red-50 p-6 rounded-2xl border-l-4 border-red-400 italic text-gray-700 text-2xl font-serif">
                    "The world is waiting for your light. Shine brightly, Alisha, and remember that every new year is a fresh canvas for your masterpiece."
                </div>
                <p class="text-lg text-right text-gray-500 mt-4">- With all our love</p>
            </section>

            <!-- Section 7: The Grand Finale -->
            <section class="content-section text-center p-4" data-index="6">
                <div class="flex flex-col items-center justify-center h-full">
                    <h2 class="text-5xl title-pacifico text-yellow-600 mb-6">
                        🎁 Happy Birthday, Alisha!
                    </h2>
                    <p class="text-2xl font-semibold text-gray-800 mb-8">
                        The grand finale to your celebration has arrived!
                    </p>
                    <div class="text-6xl mb-6 animate-bounce">
                        🥳 🎈 🎂
                    </div>
                    <p class="text-xl text-purple-700 font-medium">
                        Thank you for being you. Now go have the most amazing birthday!
                    </p>
                </div>
            </section>

        </div>
        
        <!-- Navigation Buttons -->
        <div class="flex justify-between mt-4">
            <button id="back-button" class="festive-button bg-gray-300 text-gray-800 font-bold py-2 px-4 rounded-full opacity-0 pointer-events-none" onclick="changeSection(-1)">
                &larr; Back
            </button>
            <button id="next-button" class="festive-button bg-pink-500 hover:bg-pink-600 text-white font-bold py-2 px-6 rounded-full" onclick="changeSection(1)">
                Next &rarr;
            </button>
        </div>
    </div>

    <script>
        // Set the current environment variables (required for Firebase if used, but not used here)
        const appId = typeof __app_id !== 'undefined' ? __app_id : 'default-app-id';

        let currentPageIndex = 0;
        const sections = document.querySelectorAll('.content-section');
        const nextButton = document.getElementById('next-button');
        const backButton = document.getElementById('back-button');

        // Initial setup: activate the first section
        document.addEventListener('DOMContentLoaded', () => {
            updateUI();
        });
        
        /**
         * Changes the currently visible celebration section.
         * @param {number} direction - 1 for next, -1 for back.
         */
        function changeSection(direction) {
            const newIndex = currentPageIndex + direction;
            
            // Check boundaries
            if (newIndex >= 0 && newIndex < sections.length) {
                // Deactivate current section
                sections[currentPageIndex].classList.remove('active');
                
                // Update index
                currentPageIndex = newIndex;
                
                // Activate new section
                sections[currentPageIndex].classList.add('active');
                
                updateUI();
            }
        }

        /**
         * Updates button visibility based on the current page index.
         */
        function updateUI() {
            // Check if we are on the first section (index 0)
            if (currentPageIndex === 0) {
                backButton.classList.add('opacity-0', 'pointer-events-none');
            } else {
                backButton.classList.remove('opacity-0', 'pointer-events-none');
            }

            // Check if we are on the last section (index 6, since we have 7 sections)
            if (currentPageIndex === sections.length - 1) {
                nextButton.classList.add('opacity-0', 'pointer-events-none');
            } else {
                nextButton.classList.remove('opacity-0', 'pointer-events-none');
            }
        }

        // Initialize display to show only the first section
        sections.forEach((section, index) => {
            if (index !== 0) {
                section.classList.remove('active');
            }
        });

    </script>
</body>
</html>
