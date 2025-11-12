<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Help Around the Block</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Load Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        /* Custom styles for the Inter font and smooth transitions */
        :root {
            --primary-color: #10b981; /* Emerald 500 */
            --secondary-color: #3b82f6; /* Blue 500 */
        }
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8fafc; /* Slate 50 */
        }
        .task-card:hover {
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            transform: translateY(-2px);
        }
        .btn-primary {
            transition: all 0.2s;
        }
        .btn-primary:hover {
            background-color: #059669; /* Emerald 600 */
            transform: translateY(-1px);
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo/Title -->
                <div class="flex-shrink-0">
                    <a href="#" class="text-2xl font-extrabold text-emerald-600 tracking-tight">
                        <i data-lucide="handshake" class="inline-block w-6 h-6 mr-1 align-middle"></i>
                        Help Around the Block
                    </a>
                </div>
                
                <!-- Desktop Nav Links -->
                <nav class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-4">
                        <a href="#how-it-works" class="text-gray-600 hover:text-emerald-600 px-3 py-2 rounded-md text-sm font-medium transition duration-150">How It Works</a>
                        <a href="#requests" class="text-gray-600 hover:text-emerald-600 px-3 py-2 rounded-md text-sm font-medium transition duration-150">Find Tasks</a>
                        <button id="open-post-modal" class="btn-primary bg-emerald-500 text-white px-4 py-2 rounded-lg text-sm font-semibold shadow-lg">Post a Request</button>
                    </div>
                </nav>

                <!-- Mobile Menu Button -->
                <div class="md:hidden">
                    <button id="mobile-menu-button" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-emerald-500">
                        <i data-lucide="menu" class="w-6 h-6"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu (Hidden by default) -->
        <div id="mobile-menu" class="md:hidden hidden">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="#how-it-works" class="block text-gray-700 hover:bg-emerald-50 hover:text-emerald-600 px-3 py-2 rounded-md text-base font-medium">How It Works</a>
                <a href="#requests" class="block text-gray-700 hover:bg-emerald-50 hover:text-emerald-600 px-3 py-2 rounded-md text-base font-medium">Find Tasks</a>
                <button id="open-post-modal-mobile" class="w-full btn-primary bg-emerald-500 text-white px-4 py-2 rounded-lg text-base font-semibold shadow-lg mt-2">Post a Request</button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <main>
        <div class="bg-gradient-to-r from-emerald-50 to-cyan-50 py-20 sm:py-28">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <span class="inline-block bg-emerald-200 text-emerald-800 text-xs font-semibold px-3 py-1 rounded-full uppercase mb-4">Community Strong</span>
                <h1 class="text-5xl sm:text-6xl font-extrabold text-gray-900 mb-4 leading-tight">
                    Get Local Help. Be a Local Hero.
                </h1>
                <p class="text-xl text-gray-600 max-w-3xl mx-auto mb-8">
                    Connect with neighbors for small tasks, errands, and support, right around the corner.
                </p>
                <div class="flex justify-center space-x-4">
                    <button id="open-post-modal-hero" class="btn-primary bg-emerald-600 text-white px-8 py-3 rounded-xl text-lg font-bold shadow-xl shadow-emerald-200 hover:bg-emerald-700">
                        I Need Help
                    </button>
                    <a href="#requests" class="inline-flex items-center bg-white border border-gray-300 text-gray-700 px-8 py-3 rounded-xl text-lg font-bold shadow-md hover:bg-gray-50 transition duration-150">
                        <i data-lucide="heart" class="w-5 h-5 mr-2"></i>
                        I Can Help
                    </a>
                </div>
            </div>
        </div>

        <!-- How It Works Section -->
        <section id="how-it-works" class="py-16 sm:py-24 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-3xl sm:text-4xl font-bold text-center text-gray-900 mb-12">How It Works in 3 Simple Steps</h2>
                <div class="grid md:grid-cols-3 gap-10 text-center">

                    <!-- Step 1 -->
                    <div class="p-6 rounded-2xl bg-white border border-emerald-100 shadow-lg transition duration-300 hover:shadow-xl">
                        <div class="w-16 h-16 bg-emerald-100 text-emerald-600 rounded-full flex items-center justify-center mx-auto mb-4">
                            <i data-lucide="list-checks" class="w-8 h-8"></i>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">1. Post Your Task</h3>
                        <p class="text-gray-600">Describe the help you need, whether it's moving boxes or picking up groceries. It's quick and free.</p>
                    </div>

                    <!-- Step 2 -->
                    <div class="p-6 rounded-2xl bg-white border border-blue-100 shadow-lg transition duration-300 hover:shadow-xl">
                        <div class="w-16 h-16 bg-blue-100 text-blue-600 rounded-full flex items-center justify-center mx-auto mb-4">
                            <i data-lucide="users" class="w-8 h-8"></i>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">2. Neighbors Respond</h3>
                        <p class="text-gray-600">Local, verified volunteers or paid helpers nearby will see your request and offer assistance.</p>
                    </div>

                    <!-- Step 3 -->
                    <div class="p-6 rounded-2xl bg-white border border-yellow-100 shadow-lg transition duration-300 hover:shadow-xl">
                        <div class="w-16 h-16 bg-yellow-100 text-yellow-600 rounded-full flex items-center justify-center mx-auto mb-4">
                            <i data-lucide="check-circle" class="w-8 h-8"></i>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">3. Get It Done</h3>
                        <p class="text-gray-600">Connect directly with your helper and complete the task! Strengthen your local community.</p>
                    </div>

                </div>
            </div>
        </section>

        <!-- Current Requests Section -->
        <section id="requests" class="py-16 sm:py-24 bg-slate-50">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-3xl sm:text-4xl font-bold text-center text-gray-900 mb-12">Current Local Requests</h2>

                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">

                    <!-- Task Card 1 -->
                    <div class="task-card bg-white p-6 rounded-xl shadow-lg transition duration-300 border-l-4 border-emerald-500">
                        <div class="flex justify-between items-start mb-3">
                            <span class="text-sm font-medium bg-red-100 text-red-800 px-3 py-1 rounded-full">Urgent</span>
                            <i data-lucide="map-pin" class="w-5 h-5 text-gray-500"></i>
                        </div>
                        <h3 class="text-xl font-bold text-gray-900 mb-2">Help Moving a Sofa</h3>
                        <p class="text-gray-600 mb-4 text-sm">Need two strong people for about 30 minutes to move a large sofa from the garage to the living room. ASAP!</p>
                        <div class="flex items-center text-sm text-gray-500 space-x-4">
                            <span><i data-lucide="clock" class="w-4 h-4 inline mr-1"></i> Posted 2h ago</span>
                            <span><i data-lucide="dollar-sign" class="w-4 h-4 inline mr-1"></i> Paid/Tip</span>
                        </div>
                    </div>

                    <!-- Task Card 2 -->
                    <div class="task-card bg-white p-6 rounded-xl shadow-lg transition duration-300 border-l-4 border-blue-500">
                        <div class="flex justify-between items-start mb-3">
                            <span class="text-sm font-medium bg-blue-100 text-blue-800 px-3 py-1 rounded-full">Errand</span>
                            <i data-lucide="map-pin" class="w-5 h-5 text-gray-500"></i>
                        </div>
                        <h3 class="text-xl font-bold text-gray-900 mb-2">Weekly Grocery Pickup</h3>
                        <p class="text-gray-600 mb-4 text-sm">Looking for someone reliable to pick up my grocery order every Thursday afternoon. Will pay hourly rate.</p>
                        <div class="flex items-center text-sm text-gray-500 space-x-4">
                            <span><i data-lucide="calendar" class="w-4 h-4 inline mr-1"></i> Every Thursday</span>
                            <span><i data-lucide="dollar-sign" class="w-4 h-4 inline mr-1"></i> Paid</span>
                        </div>
                    </div>

                    <!-- Task Card 3 -->
                    <div class="task-card bg-white p-6 rounded-xl shadow-lg transition duration-300 border-l-4 border-yellow-500">
                        <div class="flex justify-between items-start mb-3">
                            <span class="text-sm font-medium bg-yellow-100 text-yellow-800 px-3 py-1 rounded-full">Volunteer</span>
                            <i data-lucide="map-pin" class="w-5 h-5 text-gray-500"></i>
                        </div>
                        <h3 class="text-xl font-bold text-gray-900 mb-2">Watering Plants While Away</h3>
                        <p class="text-gray-600 mb-4 text-sm">Going on vacation for one week. Need someone to stop by twice to water indoor and patio plants. Neighborly favor!</p>
                        <div class="flex items-center text-sm text-gray-500 space-x-4">
                            <span><i data-lucide="sun" class="w-4 h-4 inline mr-1"></i> Next Week</span>
                            <span><i data-lucide="dollar-sign" class="w-4 h-4 inline mr-1"></i> Free</span>
                        </div>
                    </div>

                    <!-- Task Card 4 (Hidden on small screens) -->
                    <div class="task-card bg-white p-6 rounded-xl shadow-lg transition duration-300 border-l-4 border-purple-500 hidden lg:block">
                        <div class="flex justify-between items-start mb-3">
                            <span class="text-sm font-medium bg-purple-100 text-purple-800 px-3 py-1 rounded-full">Repair</span>
                            <i data-lucide="map-pin" class="w-5 h-5 text-gray-500"></i>
                        </div>
                        <h3 class="text-xl font-bold text-gray-900 mb-2">Fixing a Dripping Faucet</h3>
                        <p class="text-gray-600 mb-4 text-sm">Faucet in the kitchen sink is leaking. Hoping to find someone handy with plumbing experience for a quick fix.</p>
                        <div class="flex items-center text-sm text-gray-500 space-x-4">
                            <span><i data-lucide="wrench" class="w-4 h-4 inline mr-1"></i> Any evening</span>
                            <span><i data-lucide="dollar-sign" class="w-4 h-4 inline mr-1"></i> Tip</span>
                        </div>
                    </div>

                </div>

                <div class="text-center mt-12">
                    <button id="load-more-btn" class="inline-flex items-center bg-white border border-emerald-300 text-emerald-600 px-6 py-3 rounded-xl text-md font-semibold shadow-md hover:bg-emerald-50 transition duration-150">
                        <i data-lucide="rotate-ccw" class="w-5 h-5 mr-2"></i>
                        Load More Requests
                    </button>
                </div>

            </div>
        </section>

        <!-- Call to Action Footer CTA -->
        <section class="bg-emerald-600 py-16">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <h2 class="text-3xl sm:text-4xl font-extrabold text-white mb-4">Ready to Get or Give Help?</h2>
                <p class="text-xl text-emerald-100 mb-8">Join the growing community making life easier, one block at a time.</p>
                <button id="open-post-modal-footer" class="btn-primary bg-white text-emerald-600 px-10 py-4 rounded-xl text-xl font-bold shadow-2xl hover:bg-gray-100 hover:text-emerald-700">
                    Join the Community
                </button>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-4 gap-8">
                <!-- Brand Info -->
                <div>
                    <h3 class="text-xl font-bold text-emerald-400 mb-4">Help Around the Block</h3>
                    <p class="text-sm text-gray-400">Making neighborhood support simple and reliable since 2025.</p>
                </div>
                <!-- Links 1 -->
                <div>
                    <h4 class="text-lg font-semibold mb-4">Company</h4>
                    <ul class="space-y-2 text-sm">
                        <li><a href="#" class="text-gray-400 hover:text-emerald-400 transition">About Us</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-emerald-400 transition">Careers</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-emerald-400 transition">Press</a></li>
                    </ul>
                </div>
                <!-- Links 2 -->
                <div>
                    <h4 class="text-lg font-semibold mb-4">Support</h4>
                    <ul class="space-y-2 text-sm">
                        <li><a href="#" class="text-gray-400 hover:text-emerald-400 transition">FAQ</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-emerald-400 transition">Contact Us</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-emerald-400 transition">Safety Guidelines</a></li>
                    </ul>
                </div>
                <!-- Social -->
                <div>
                    <h4 class="text-lg font-semibold mb-4">Follow Us</h4>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-emerald-400 transition"><i data-lucide="instagram" class="w-6 h-6"></i></a>
                        <a href="#" class="text-gray-400 hover:text-emerald-400 transition"><i data-lucide="facebook" class="w-6 h-6"></i></a>
                        <a href="#" class="text-gray-400 hover:text-emerald-400 transition"><i data-lucide="twitter" class="w-6 h-6"></i></a>
                    </div>
                </div>
            </div>
            <div class="mt-8 pt-6 border-t border-gray-700 text-center">
                <p class="text-sm text-gray-500">&copy; 2025 Help Around the Block. All rights reserved.</p>
            </div>
        </div>
    </footer>


    <!-- Post Request Modal (Hidden by default) -->
    <div id="post-request-modal" class="fixed inset-0 bg-gray-900 bg-opacity-75 flex items-center justify-center z-50 hidden transition-opacity duration-300">
        <div class="bg-white rounded-xl shadow-2xl w-full max-w-lg p-6 m-4 relative transform transition-all duration-300 scale-95 opacity-0" id="modal-content">
            <!-- Close Button -->
            <button id="close-post-modal" class="absolute top-4 right-4 text-gray-400 hover:text-gray-700">
                <i data-lucide="x" class="w-6 h-6"></i>
            </button>

            <h3 class="text-2xl font-bold text-gray-900 mb-4">Post a New Request</h3>
            <p class="text-gray-600 mb-6">Tell your neighbors what you need help with. It takes just a minute!</p>

            <form>
                <div class="mb-4">
                    <label for="task-title" class="block text-sm font-medium text-gray-700 mb-1">Task Title</label>
                    <input type="text" id="task-title" placeholder="E.g., Need help with garden weeding" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500" required>
                </div>
                <div class="mb-4">
                    <label for="task-description" class="block text-sm font-medium text-gray-700 mb-1">Description</label>
                    <textarea id="task-description" rows="4" placeholder="Be detailed about what the task involves and where you are located (approximate block/street is fine)." class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500" required></textarea>
                </div>
                <div class="mb-6">
                    <label for="task-compensation" class="block text-sm font-medium text-gray-700 mb-1">Compensation</label>
                    <select id="task-compensation" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                        <option value="volunteer">Volunteer (Neighborly Favor)</option>
                        <option value="tip">Tip Offered</option>
                        <option value="paid">Paid (Specify Rate)</option>
                    </select>
                </div>

                <button type="submit" class="btn-primary w-full bg-emerald-600 text-white px-4 py-3 rounded-lg text-lg font-bold hover:bg-emerald-700">
                    Post Request
                </button>
                <div id="submit-message" class="mt-4 text-center text-sm text-green-600 hidden">
                    Your request has been posted successfully! A neighbor will reach out soon.
                </div>
            </form>
        </div>
    </div>


    <!-- JavaScript for Mobile Menu and Modal -->
    <script>
        // Initialize Lucide Icons
        lucide.createIcons();

        // 1. Mobile Menu Toggle
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // 2. Modal Logic
        const modal = document.getElementById('post-request-modal');
        const modalContent = document.getElementById('modal-content');
        const openButtons = [
            document.getElementById('open-post-modal'),
            document.getElementById('open-post-modal-mobile'),
            document.getElementById('open-post-modal-hero'),
            document.getElementById('open-post-modal-footer'),
        ];
        const closeButton = document.getElementById('close-post-modal');
        const form = modal.querySelector('form');
        const submitMessage = document.getElementById('submit-message');

        function openModal() {
            modal.classList.remove('hidden');
            // Animate in
            setTimeout(() => {
                modal.classList.add('opacity-100');
                modalContent.classList.remove('scale-95', 'opacity-0');
            }, 10);
            submitMessage.classList.add('hidden'); // Reset message
        }

        function closeModal() {
            // Animate out
            modal.classList.remove('opacity-100');
            modalContent.classList.add('scale-95', 'opacity-0');
            // Hide after animation completes
            setTimeout(() => {
                modal.classList.add('hidden');
            }, 300);
        }

        openButtons.forEach(btn => {
            if (btn) {
                btn.addEventListener('click', openModal);
            }
        });

        closeButton.addEventListener('click', closeModal);

        // Close modal when clicking outside of it
        modal.addEventListener('click', (e) => {
            if (e.target === modal) {
                closeModal();
            }
        });

        // Form submission (for demo purposes)
        form.addEventListener('submit', (e) => {
            e.preventDefault();
            
            // In a real app, this is where you'd send data to a server (like Firestore).
            
            // Show success message
            submitMessage.classList.remove('hidden');
            
            // Reset form fields
            form.reset();

            // Auto-close modal after a delay
            setTimeout(closeModal, 2000);
        });
        
        // 3. Mock Load More Button
        const loadMoreBtn = document.getElementById('load-more-btn');
        loadMoreBtn.addEventListener('click', () => {
            loadMoreBtn.innerHTML = '<i data-lucide="loader-circle" class="w-5 h-5 mr-2 animate-spin"></i> Loading...';
            
            // Simulate API call delay
            setTimeout(() => {
                // In a real app, load more tasks here.
                alert('No more mock tasks to load! You have seen them all. Time to post your own!');
                
                // Reset button text
                loadMoreBtn.innerHTML = '<i data-lucide="rotate-ccw" class="w-5 h-5 mr-2"></i> Load More Requests';
                lucide.createIcons();
            }, 1000);
        });

    </script>
</body>
</html>
