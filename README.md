<html lang="en"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UMWTV 2026 Merchant Exchange Conference</title>
    <!-- Tailwind CSS v3 -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome -->
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <!-- GSAP for animations -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
    <!-- AOS for scroll animations -->
    <link href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#0056b3',
                        secondary: '#00a0e9',
                        accent: '#ff6b00',
                        dark: '#1a1a2e',
                        light: '#f5f5f5'
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                    backgroundImage: {
                        'hero-pattern': 'linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7))',
                    }
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .text-shadow {
                text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            }
            .glass {
                background: rgba(255, 255, 255, 0.2);
                backdrop-filter: blur(8px);
                -webkit-backdrop-filter: blur(8px);
                border: 1px solid rgba(255, 255, 255, 0.18);
            }
            .card-hover {
                transition: all 0.3s ease;
            }
            .card-hover:hover {
                transform: translateY(-10px);
                box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
            }
            .countdown-item {
                @apply bg-white bg-opacity-20 rounded-lg p-4 text-center backdrop-blur-sm border border-white border-opacity-30;
            }
            .countdown-number {
                @apply text-4xl md:text-5xl font-bold text-white;
            }
            .countdown-label {
                @apply text-sm uppercase tracking-wider text-white text-opacity-80;
            }
            .prize-card {
                @apply relative overflow-hidden rounded-xl shadow-lg transition-all duration-300 hover:shadow-2xl;
            }
            .prize-card:hover .prize-overlay {
                opacity: 1;
            }
            .prize-overlay {
                @apply absolute inset-0 bg-gradient-to-t from-black to-transparent opacity-70 transition-opacity duration-300;
            }
            .btn-primary {
                @apply bg-primary hover:bg-blue-700 text-white font-bold py-3 px-6 rounded-full transition-all duration-300 transform hover:scale-105 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-opacity-50;
            }
            .btn-secondary {
                @apply bg-accent hover:bg-orange-600 text-white font-bold py-3 px-6 rounded-full transition-all duration-300 transform hover:scale-105 focus:outline-none focus:ring-2 focus:ring-orange-500 focus:ring-opacity-50;
            }
            .section-title {
                @apply text-3xl md:text-4xl font-bold mb-8 text-center relative;
            }
            .section-title::after {
                content: '';
                @apply absolute bottom-0 left-1/2 transform -translate-x-1/2 w-24 h-1 bg-accent mt-2;
            }
        }
    </style>
</head>
<body class="bg-light text-dark">
    <!-- Navigation -->
    <nav class="fixed top-0 w-full z-50 bg-white bg-opacity-90 backdrop-blur-sm shadow-md">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <a href="#" class="flex items-center">
                <span class="text-primary text-2xl font-bold">UMWTV</span>
            </a>
            <div class="hidden md:flex space-x-8">
                <a href="#about" class="text-dark hover:text-primary transition-colors">About</a>
                <a href="#schedule" class="text-dark hover:text-primary transition-colors">Schedule</a>
                <a href="#prizes" class="text-dark hover:text-primary transition-colors">Prizes</a>
                <a href="#rewards" class="text-dark hover:text-primary transition-colors">Rewards</a>
                <a href="#faq" class="text-dark hover:text-primary transition-colors">FAQ</a>
            </div>
            <button class="btn-primary hidden md:block">Register Now</button>
            <button class="md:hidden text-dark focus:outline-none" id="mobile-menu-button">
                <i class="fa fa-bars text-xl"></i>
            </button>
        </div>
        <!-- Mobile Menu -->
        <div class="md:hidden hidden bg-white w-full absolute top-full left-0 shadow-md" id="mobile-menu">
            <div class="container mx-auto px-4 py-3 flex flex-col space-y-4">
                <a href="#about" class="text-dark hover:text-primary transition-colors py-2">About</a>
                <a href="#schedule" class="text-dark hover:text-primary transition-colors py-2">Schedule</a>
                <a href="#prizes" class="text-dark hover:text-primary transition-colors py-2">Prizes</a>
                <a href="#rewards" class="text-dark hover:text-primary transition-colors py-2">Rewards</a>
                <a href="#faq" class="text-dark hover:text-primary transition-colors py-2">FAQ</a>
                <button class="btn-primary w-full">Register Now</button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative h-screen flex items-center justify-center text-white overflow-hidden">
        <div class="absolute inset-0 z-0">
            <img src="https://p11-doubao-search-sign.byteimg.com/tos-cn-i-be4g95zd3a/919616098005418130~tplv-be4g95zd3a-image.jpeg?lk3s=feb11e32&amp;x-expires=1783222795&amp;x-signature=DcMBydxaCCUD6qLNjzsCushTWe0%3D" alt="Business Conference" class="w-full h-full object-cover">
            <div class="absolute inset-0 bg-dark bg-opacity-70"></div>
        </div>
        <div class="container mx-auto px-4 z-10 text-center" data-aos="fade-up" data-aos-duration="1000">
            <h1 class="text-4xl md:text-6xl font-bold mb-4 text-shadow">UMWTV 2026 Merchant Exchange Conference</h1>
            <p class="text-xl md:text-2xl mb-8 max-w-3xl mx-auto">Join us for an exclusive cross-border e-commerce conference in Cape Town, South Africa</p>
            <div class="flex flex-col md:flex-row justify-center items-center space-y-4 md:space-y-0 md:space-x-6 mb-12">
                <div class="flex items-center">
                    <i class="fa fa-calendar text-accent mr-2"></i>
                    <span>February 7, 2026</span>
                </div>
                <div class="flex items-center">
                    <i class="fa fa-map-marker text-accent mr-2"></i>
                    <span>Cape Grace, A Fairmont Managed Hotel</span>
                </div>
            </div>
            
            <!-- Countdown Timer -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 md:gap-8 max-w-3xl mx-auto mb-12">
                <div class="countdown-item">
                    <div class="countdown-number" id="days">00</div>
                    <div class="countdown-label">Days</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="hours">00</div>
                    <div class="countdown-label">Hours</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="minutes">00</div>
                    <div class="countdown-label">Minutes</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="seconds">00</div>
                    <div class="countdown-label">Seconds</div>
                </div>
            </div>
            
            <div class="flex flex-col md:flex-row justify-center space-y-4 md:space-y-0 md:space-x-6">
                <a href="https://umw-tv.com/xml/index.html#/login" target="_blank" class="btn-primary">
                    <i class="fa fa-ticket mr-2"></i> Click to participate
                </a>
                <a href="#prizes" class="btn-secondary">
                    <i class="fa fa-info-circle mr-2"></i> Learn More
                </a>
            </div>
        </div>
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
            <a href="#about" class="text-white">
                <i class="fa fa-chevron-down text-2xl"></i>
            </a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="section-title" data-aos="fade-up">About the Conference</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                <div data-aos="fade-right">
                    <p class="text-lg mb-6">Thank you for your continued trust and support. To create a better development environment and provide better services, our company has decided to organize a cross-border e-commerce exchange conference on February 7, 2026.</p>
                    <p class="text-lg mb-6">We invite representatives from well-known e-commerce enterprises, experts and scholars, relevant government departments, platform merchants, manufacturers, and industry associations at home and abroad to discuss cross-border e-commerce development trends, policies and regulations, market changes, and new technology applications.</p>
                    <p class="text-lg mb-6">By accumulating subscriptions to the Exchange Development Fund, you can obtain an invitation letter for the online or offline exchange meeting and participate in this offline exchange meeting activity of the company. We sincerely invite all members to attend!</p>
                </div>
                <div class="rounded-xl overflow-hidden shadow-lg" data-aos="fade-left">
                    <img src="https://p3-doubao-search-sign.byteimg.com/tos-cn-i-be4g95zd3a/988868700557541385~tplv-be4g95zd3a-image.jpeg?lk3s=feb11e32&amp;x-expires=1783222795&amp;x-signature=sfY1YdbZqlFpvXvtmPEqjRTH2%2FU%3D" alt="Business Meeting" class="w-full h-auto">
                </div>
            </div>
        </div>
    </section>

    <!-- Schedule Section -->
    <section id="schedule" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <h2 class="section-title" data-aos="fade-up">Event Schedule</h2>
            <div class="max-w-4xl mx-auto">
                <!-- Timeline -->
                <div class="relative">
                    <!-- Timeline Line -->
                    <div class="absolute left-0 md:left-1/2 h-full w-1 bg-primary transform md:-translate-x-1/2"></div>
                    
                    <!-- Day 1 -->
                    <div class="mb-12 relative" data-aos="fade-up">
                        <div class="flex flex-col md:flex-row items-start">
                            <div class="md:w-1/2 md:pr-12 md:text-right mb-6 md:mb-0">
                                <div class="bg-white p-6 rounded-lg shadow-md">
                                    <h3 class="text-xl font-bold text-primary mb-2">February 6, 2026</h3>
                                    <p class="text-gray-700 mb-4">Arrival in Cape Town &amp; Accommodation</p>
                                    <div class="flex items-center text-gray-600">
                                        <i class="fa fa-map-marker text-accent mr-2"></i>
                                        <span>Cape Grace, A Fairmont Managed Hotel</span>
                                    </div>
                                    <div class="mt-2 text-gray-600">
                                        <p>V&amp;A Waterfront, W Quay Rd, Victoria &amp; Alfred Waterfront, Cape Town, 8001 South Africa</p>
                                    </div>
                                </div>
                            </div>
                            <div class="absolute left-0 md:left-1/2 w-6 h-6 bg-primary rounded-full transform -translate-y-1/2 md:-translate-x-1/2 mt-3 md:mt-0"></div>
                            <div class="md:w-1/2 md:pl-12"></div>
                        </div>
                    </div>
                    
                    <!-- Day 2 -->
                    <div class="mb-12 relative" data-aos="fade-up" data-aos-delay="100">
                        <div class="flex flex-col md:flex-row items-start">
                            <div class="md:w-1/2 md:pr-12"></div>
                            <div class="absolute left-0 md:left-1/2 w-6 h-6 bg-primary rounded-full transform -translate-y-1/2 md:-translate-x-1/2 mt-3 md:mt-0"></div>
                            <div class="md:w-1/2 md:pl-12">
                                <div class="bg-white p-6 rounded-lg shadow-md">
                                    <h3 class="text-xl font-bold text-primary mb-2">February 7, 2026</h3>
                                    <p class="text-gray-700 mb-4">Conference Day &amp; Gala Dinner</p>
                                    <ul class="text-gray-600 space-y-2">
                                        <li><i class="fa fa-check-circle text-accent mr-2"></i> Check-in &amp; Registration</li>
                                        <li><i class="fa fa-check-circle text-accent mr-2"></i> Opening Speech</li>
                                        <li><i class="fa fa-check-circle text-accent mr-2"></i> Operation Report</li>
                                        <li><i class="fa fa-check-circle text-accent mr-2"></i> Live Lucky Draw</li>
                                        <li><i class="fa fa-check-circle text-accent mr-2"></i> Gala Dinner</li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Day 3 -->
                    <div class="relative" data-aos="fade-up" data-aos-delay="200">
                        <div class="flex flex-col md:flex-row items-start">
                            <div class="md:w-1/2 md:pr-12 md:text-right mb-6 md:mb-0">
                                <div class="bg-white p-6 rounded-lg shadow-md">
                                    <h3 class="text-xl font-bold text-primary mb-2">February 8, 2026</h3>
                                    <p class="text-gray-700 mb-4">Office Visit &amp; Experience Exchange</p>
                                    <ul class="text-gray-600 space-y-2 md:ml-auto">
                                        <li><i class="fa fa-check-circle text-accent mr-2"></i> Office Visit</li>
                                        <li><i class="fa fa-check-circle text-accent mr-2"></i> Experience Sharing</li>
                                        <li><i class="fa fa-check-circle text-accent mr-2"></i> Suggestions &amp; Feedback</li>
                                        <li><i class="fa fa-check-circle text-accent mr-2"></i> Optimization &amp; Improvement</li>
                                        <li><i class="fa fa-check-circle text-accent mr-2"></i> Gala Dinner</li>
                                    </ul>
                                </div>
                            </div>
                            <div class="absolute left-0 md:left-1/2 w-6 h-6 bg-primary rounded-full transform -translate-y-1/2 md:-translate-x-1/2 mt-3 md:mt-0"></div>
                            <div class="md:w-1/2 md:pl-12"></div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Hotel Image -->
            <div class="mt-16 rounded-xl overflow-hidden shadow-xl" data-aos="fade-up">
                <img src="https://p3-flow-imagex-sign.byteimg.com/tos-cn-i-a9rns2rl98/rc/pc/code_assistant/09cf21be037c479eaa6aad87d807676b~tplv-a9rns2rl98-image.image?rcl=202601061312017AF9E4FFDC054B998142&amp;rk3s=8e244e95&amp;rrcfp=e75484ac&amp;x-expires=1768281122&amp;x-signature=OHMZyRScihJByGvrlOqsOzboSiQ%3D" alt="Cape Grace Hotel" class="w-full h-auto">
            </div>
        </div>
    </section>

    <!-- Prizes Section -->
    <section id="prizes" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="section-title" data-aos="fade-up">Lucky Draw Prizes</h2>
            <p class="text-center text-lg mb-12 max-w-3xl mx-auto" data-aos="fade-up">
                Exciting prizes await our participants at the UMWTV 2026 Conference Lucky Draw. Don't miss your chance to win big!
            </p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Grand Prize -->
                <div class="col-span-1 md:col-span-2 lg:col-span-3" data-aos="fade-up">
                    <div class="prize-card bg-gradient-to-r from-primary to-secondary text-white">
                        <div class="p-8">
                            <div class="flex flex-col md:flex-row items-center justify-between">
                                <div class="mb-6 md:mb-0">
                                    <h3 class="text-2xl font-bold mb-2">Grand Prize</h3>
                                    <p class="text-4xl font-bold mb-4">3,000,000 ZAR</p>
                                    <p class="opacity-80">Limited to 3 winners</p>
                                </div>
                                <div class="flex items-center justify-center">
                                    <div class="bg-white rounded-full p-4 text-primary">
                                        <i class="fa fa-trophy text-5xl"></i>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- First Prize -->
                <div class="prize-card" data-aos="fade-up" data-aos-delay="100">
                    <img src="https://p11-doubao-search-sign.byteimg.com/labis/image/926144a1aca919952e09612db2ff76ab~tplv-be4g95zd3a-image.jpeg?lk3s=feb11e32&amp;x-expires=1783222795&amp;x-signature=WY9N%2FAnX4G8k%2BojLTSty8R%2FOfnY%3D" alt="Tesla Model Y" class="w-full h-64 object-cover">
                    <div class="prize-overlay"></div>
                    <div class="absolute bottom-0 left-0 right-0 p-6 text-white">
                        <h3 class="text-xl font-bold mb-2">First Prize</h3>
                        <p class="text-lg font-semibold mb-1">Tesla Model Y (2025)</p>
                        <p class="text-lg font-semibold mb-1">+ 1,000,000 ZAR</p>
                        <p class="text-sm opacity-80">Limited to 20 winners</p>
                    </div>
                </div>
                
                <!-- Second Prize -->
                <div class="prize-card" data-aos="fade-up" data-aos-delay="200">
                    <img src="https://p26-doubao-search-sign.byteimg.com/labis/image/052518ae49d15637e8916d8697f0bbfd~tplv-be4g95zd3a-image.jpeg?lk3s=feb11e32&amp;x-expires=1783222795&amp;x-signature=PEo6yRbOgAoCnkAuqd4g%2BZga%2FPU%3D" alt="Honda CB1000 Hornet SP" class="w-full h-64 object-cover">
                    <div class="prize-overlay"></div>
                    <div class="absolute bottom-0 left-0 right-0 p-6 text-white">
                        <h3 class="text-xl font-bold mb-2">Second Prize</h3>
                        <p class="text-lg font-semibold mb-1">Honda CB1000 Hornet SP</p>
                        <p class="text-lg font-semibold mb-1">+ 500,000 ZAR</p>
                        <p class="text-sm opacity-80">Limited to 50 winners</p>
                    </div>
                </div>
                
                <!-- Third Prize -->
                <div class="prize-card" data-aos="fade-up" data-aos-delay="300">
                    <img src="https://p11-doubao-search-sign.byteimg.com/ecom-shop-material/jpeg_m_db39afef7648723d330bcb310988786e_sx_65508_www800-800~tplv-be4g95zd3a-image.jpeg?lk3s=feb11e32&amp;x-expires=1783222795&amp;x-signature=g3NcZJlx5qVRIzoN5TLh74zS%2BdY%3D" alt="Samsung Home Appliances" class="w-full h-64 object-cover">
                    <div class="prize-overlay"></div>
                    <div class="absolute bottom-0 left-0 right-0 p-6 text-white">
                        <h3 class="text-xl font-bold mb-2">Third Prize</h3>
                        <p class="text-lg font-semibold mb-1">Samsung Home Appliance Series</p>
                        <p class="text-lg font-semibold mb-1">+ 300,000 ZAR</p>
                        <p class="text-sm opacity-80">Limited to 80 winners</p>
                    </div>
                </div>
                
                <!-- Fourth Prize -->
                <div class="prize-card bg-gradient-to-r from-green-500 to-teal-500" data-aos="fade-up" data-aos-delay="400">
                    <div class="p-8 text-white">
                        <div class="flex flex-col items-center justify-center text-center">
                            <div class="bg-white rounded-full p-4 text-teal-500 mb-4">
                                <i class="fa fa-money text-4xl"></i>
                            </div>
                            <h3 class="text-xl font-bold mb-2">Fourth Prize</h3>
                            <p class="text-3xl font-bold mb-4">100,000 ZAR</p>
                            <p class="opacity-80">Limited to 200 winners</p>
                        </div>
                    </div>
                </div>
                
                <!-- Fifth Prize -->
                <div class="prize-card bg-gradient-to-r from-purple-500 to-pink-500" data-aos="fade-up" data-aos-delay="500">
                    <div class="p-8 text-white">
                        <div class="flex flex-col items-center justify-center text-center">
                            <div class="bg-white rounded-full p-4 text-pink-500 mb-4">
                                <i class="fa fa-gift text-4xl"></i>
                            </div>
                            <h3 class="text-xl font-bold mb-2">Fifth Prize</h3>
                            <p class="text-3xl font-bold mb-4">50,000 ZAR</p>
                            <p class="opacity-80">Unlimited winners</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Rewards Section -->
    <section id="rewards" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <h2 class="section-title" data-aos="fade-up">Investment Rewards</h2>
            <p class="text-center text-lg mb-12 max-w-3xl mx-auto" data-aos="fade-up">
                Subscribe to the UMWTV Exchange Development Fund and earn lucky draw chances. The more you invest, the higher your chances of winning!
            </p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
                <!-- Reward 1 -->
                <div class="bg-white rounded-xl shadow-lg p-8 transition-all duration-300 hover:shadow-xl hover:-translate-y-1" data-aos="fade-up">
                    <div class="flex items-center justify-between mb-6">
                        <div class="bg-blue-100 rounded-full p-3">
                            <i class="fa fa-star text-primary text-xl"></i>
                        </div>
                        <span class="text-2xl font-bold text-primary">1x</span>
                    </div>
                    <h3 class="text-xl font-bold mb-2">VIP Package 1
</h3>
                    <p class="text-3xl font-bold text-gray-800 mb-4">3,000 ZAR</p>
                    <p class="text-gray-600 mb-6">Subscribe to the UMWTV Exchange Development Fund and get 1 lucky draw chance</p>
                    <a href="https://umw-tv.com/xml/index.html#/login" target="_blank" class="btn-primary w-full">Click to participate</a>
                </div>
                
                <!-- Reward 2 -->
                <div class="bg-white rounded-xl shadow-lg p-8 transition-all duration-300 hover:shadow-xl hover:-translate-y-1" data-aos="fade-up" data-aos-delay="100">
                    <div class="flex items-center justify-between mb-6">
                        <div class="bg-blue-100 rounded-full p-3">
                            <i class="fa fa-star text-primary text-xl"></i>
                        </div>
                        <span class="text-2xl font-bold text-primary">2x</span>
                    </div>
                    <h3 class="text-xl font-bold mb-2">VIP Package 2
</h3>
                    <p class="text-3xl font-bold text-gray-800 mb-4">5,000 ZAR</p>
                    <p class="text-gray-600 mb-6">Subscribe to the UMWTV Exchange Development Fund and get 2 lucky draw chances</p>
                    <a href="https://umw-tv.com/xml/index.html#/login" target="_blank" class="btn-primary w-full">Click to participate</a>
                </div>
                
                <!-- Reward 3 -->
                <div class="bg-white rounded-xl shadow-lg p-8 transition-all duration-300 hover:shadow-xl hover:-translate-y-1" data-aos="fade-up" data-aos-delay="200">
                    <div class="flex items-center justify-between mb-6">
                        <div class="bg-blue-100 rounded-full p-3">
                            <i class="fa fa-star text-primary text-xl"></i>
                        </div>
                        <span class="text-2xl font-bold text-primary">5x</span>
                    </div>
                    <h3 class="text-xl font-bold mb-2">VIP Package 3
</h3>
                    <p class="text-3xl font-bold text-gray-800 mb-4">10,000 ZAR</p>
                    <p class="text-gray-600 mb-6">Subscribe to the UMWTV Exchange Development Fund and get 5 lucky draw chances</p>
                    <a href="https://umw-tv.com/xml/index.html#/login" target="_blank" class="btn-primary w-full">Click to participate</a>
                </div>
                
                <!-- Reward 4 -->
                <div class="bg-white rounded-xl shadow-lg p-8 transition-all duration-300 hover:shadow-xl hover:-translate-y-1" data-aos="fade-up" data-aos-delay="300">
                    <div class="flex items-center justify-between mb-6">
                        <div class="bg-blue-100 rounded-full p-3">
                            <i class="fa fa-star text-primary text-xl"></i>
                        </div>
                        <span class="text-2xl font-bold text-primary">12x</span>
                    </div>
                    <h3 class="text-xl font-bold mb-2">VIP Package 4
</h3>
                    <p class="text-3xl font-bold text-gray-800 mb-4">20,000 ZAR</p>
                    <p class="text-gray-600 mb-6">Subscribe to the UMWTV Exchange Development Fund and get 12 lucky draw chances</p>
                    <a href="https://umw-tv.com/xml/index.html#/login" target="_blank" class="btn-primary w-full">Click to participate</a>
                </div>
                
                <!-- Reward 5 -->
                <div class="bg-white rounded-xl shadow-lg p-8 transition-all duration-300 hover:shadow-xl hover:-translate-y-1" data-aos="fade-up" data-aos-delay="400">
                    <div class="flex items-center justify-between mb-6">
                        <div class="bg-blue-100 rounded-full p-3">
                            <i class="fa fa-star text-primary text-xl"></i>
                        </div>
                        <span class="text-2xl font-bold text-primary">30x</span>
                    </div>
                    <h3 class="text-xl font-bold mb-2">VIP Package 5
</h3>
                    <p class="text-3xl font-bold text-gray-800 mb-4">50,000 ZAR</p>
                    <p class="text-gray-600 mb-6">Subscribe to the UMWTV Exchange Development Fund and get 30 lucky draw chances</p>
                    <a href="https://umw-tv.com/xml/index.html#/login" target="_blank" class="btn-primary w-full">Click to participate</a>
                </div>
                
                <!-- Reward 6 -->
                <div class="bg-gradient-to-r from-primary to-secondary rounded-xl shadow-lg p-8 transition-all duration-300 hover:shadow-xl hover:-translate-y-1 text-white" data-aos="fade-up" data-aos-delay="500">
                    <div class="flex items-center justify-between mb-6">
                        <div class="bg-white bg-opacity-20 rounded-full p-3">
                            <i class="fa fa-star text-white text-xl"></i>
                        </div>
                        <span class="text-2xl font-bold">80x</span>
                    </div>
                    <h3 class="text-xl font-bold mb-2">VIP Package 6</h3>
                    <p class="text-3xl font-bold mb-4">100,000 ZAR</p>
                    <p class="opacity-90 mb-6">Subscribe to the UMWTV Exchange Development Fund and get 80 lucky draw chances</p>
                    <a href="https://umw-tv.com/xml/index.html#/login" target="_blank" class="bg-white text-primary hover:bg-gray-100 font-bold py-3 px-6 rounded-full transition-all duration-300 transform hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50 w-full">
                        Click to participate
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section id="faq" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="section-title" data-aos="fade-up">Frequently Asked Questions</h2>
            
            <div class="max-w-3xl mx-auto">
                <!-- FAQ Item 1 -->
                <div class="mb-6" data-aos="fade-up">
                    <button class="faq-toggle w-full flex justify-between items-center bg-gray-50 p-4 rounded-lg focus:outline-none" onclick="toggleFaq(this)">
                        <span class="text-lg font-medium">How can I participate in the conference?</span>
                        <i class="fa fa-plus text-primary transition-transform duration-300"></i>
                    </button>
                    <div class="faq-content hidden bg-white p-4 rounded-b-lg border-t-0 border border-gray-200">
                        <p class="text-gray-700">You can participate by subscribing to the UMWTV Exchange Development Fund. Once you reach the specified investment amount, you can contact the recruitment manager to register your information. Invitations will be sent out from February 1 to February 3, 2026.</p>
                    </div>
                </div>
                
                <!-- FAQ Item 2 -->
                <div class="mb-6" data-aos="fade-up" data-aos-delay="100">
                    <button class="faq-toggle w-full flex justify-between items-center bg-gray-50 p-4 rounded-lg focus:outline-none" onclick="toggleFaq(this)">
                        <span class="text-lg font-medium">Do I need to pay for travel and accommodation?</span>
                        <i class="fa fa-plus text-primary transition-transform duration-300"></i>
                    </button>
                    <div class="faq-content hidden bg-white p-4 rounded-b-lg border-t-0 border border-gray-200">
                        <p class="text-gray-700">No, all expenses for this event are covered by the company. You do not need to pay for travel, accommodation, or meals.</p>
                    </div>
                </div>
                
                <!-- FAQ Item 3 -->
                <div class="mb-6" data-aos="fade-up" data-aos-delay="200">
                    <button class="faq-toggle w-full flex justify-between items-center bg-gray-50 p-4 rounded-lg focus:outline-none" onclick="toggleFaq(this)">
                        <span class="text-lg font-medium">What if I cannot attend the event in person?</span>
                        <i class="fa fa-plus text-primary transition-transform duration-300"></i>
                    </button>
                    <div class="faq-content hidden bg-white p-4 rounded-b-lg border-t-0 border border-gray-200">
                        <p class="text-gray-700">If you cannot attend in person, you can participate in the lucky draw synchronously through the APP. The prizes are the same as the on-site lucky draw. Additionally, your invitation letter can be exchanged for an extra lucky draw chance.</p>
                    </div>
                </div>
                
                <!-- FAQ Item 4 -->
                <div class="mb-6" data-aos="fade-up" data-aos-delay="300">
                    <button class="faq-toggle w-full flex justify-between items-center bg-gray-50 p-4 rounded-lg focus:outline-none" onclick="toggleFaq(this)">
                        <span class="text-lg font-medium">Can I bring my products to the conference?</span>
                        <i class="fa fa-plus text-primary transition-transform duration-300"></i>
                    </button>
                    <div class="faq-content hidden bg-white p-4 rounded-b-lg border-t-0 border border-gray-200">
                        <p class="text-gray-700">Yes, merchants can bring their products to discuss cooperation with our company during the event.</p>
                    </div>
                </div>
                
                <!-- FAQ Item 5 -->
                <div class="mb-6" data-aos="fade-up" data-aos-delay="400">
                    <button class="faq-toggle w-full flex justify-between items-center bg-gray-50 p-4 rounded-lg focus:outline-none" onclick="toggleFaq(this)">
                        <span class="text-lg font-medium">Is the lucky draw fair and transparent?</span>
                        <i class="fa fa-plus text-primary transition-transform duration-300"></i>
                    </button>
                    <div class="faq-content hidden bg-white p-4 rounded-b-lg border-t-0 border border-gray-200">
                        <p class="text-gray-700">Yes, notary public officials will be invited to the event to ensure the lucky draw is fair, just, and transparent.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="py-20 bg-gradient-to-r from-primary to-secondary text-white">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-6" data-aos="fade-up">Ready to Join Us?</h2>
            <p class="text-xl mb-10 max-w-2xl mx-auto" data-aos="fade-up">
                Don't miss this opportunity to network with industry leaders and win exciting prizes. Register now for the UMWTV 2026 Merchant Exchange Conference!
            </p>
            <div class="flex flex-col md:flex-row justify-center space-y-4 md:space-y-0 md:space-x-6" data-aos="fade-up" data-aos-delay="100">
                <a href="https://umw-tv.com/xml/index.html#/login" target="_blank" class="bg-white text-primary hover:bg-gray-100 font-bold py-3 px-8 rounded-full transition-all duration-300 transform hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50">
                    <i class="fa fa-ticket mr-2"></i> Click to participate
                </a>
                <a href="https://api.whatsapp.com/send/?phone=27761320253&amp;text&amp;type=phone_number&amp;app_absent=0" target="_blank" class="bg-transparent border-2 border-white text-white hover:bg-white hover:text-primary font-bold py-3 px-8 rounded-full transition-all duration-300 transform hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50">
                    <i class="fa fa-phone mr-2"></i> Contact Us
                </a>
            </div>
        </div>
    </section>



    <script>
        // Initialize AOS
        document.addEventListener('DOMContentLoaded', function() {
            AOS.init({
                duration: 800,
                easing: 'ease-in-out',
                once: true
            });
            
            // Mobile Menu Toggle
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            
            mobileMenuButton.addEventListener('click', function() {
                mobileMenu.classList.toggle('hidden');
            });
            
            // Initialize Countdown Timer
            initializeCountdown();
        });
        
        // FAQ Toggle Function
        function toggleFaq(element) {
            const content = element.nextElementSibling;
            const icon = element.querySelector('i');
            
            content.classList.toggle('hidden');
            icon.classList.toggle('fa-plus');
            icon.classList.toggle('fa-minus');
            icon.classList.toggle('rotate-45');
        }
        
        // Countdown Timer Function
        function initializeCountdown() {
            const countdownDate = new Date('February 7, 2026 00:00:00').getTime();
            
            function updateCountdown() {
                const now = new Date().getTime();
                const distance = countdownDate - now;
                
                const days = Math.floor(distance / (1000 * 60 * 60 * 24));
                const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((distance % (1000 * 60)) / 1000);
                
                document.getElementById('days').innerText = days.toString().padStart(2, '0');
                document.getElementById('hours').innerText = hours.toString().padStart(2, '0');
                document.getElementById('minutes').innerText = minutes.toString().padStart(2, '0');
                document.getElementById('seconds').innerText = seconds.toString().padStart(2, '0');
                
                if (distance < 0) {
                    clearInterval(x);
                    document.getElementById('days').innerText = '00';
                    document.getElementById('hours').innerText = '00';
                    document.getElementById('minutes').innerText = '00';
                    document.getElementById('seconds').innerText = '00';
                }
            }
            
            // Update countdown immediately and then every second
            updateCountdown();
            const x = setInterval(updateCountdown, 1000);
        }
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    // Close mobile menu if open
                    document.getElementById('mobile-menu').classList.add('hidden');
                    
                    // Scroll to target with offset for fixed header
                    const headerHeight = document.querySelector('nav').offsetHeight;
                    const targetPosition = targetElement.getBoundingClientRect().top + window.pageYOffset - headerHeight;
                    
                    window.scrollTo({
                        top: targetPosition,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>

</body></html>
