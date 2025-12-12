<script lang="ts">
	import { onMount } from 'svelte';

    // Trusted customers and partners
    const customers = [
        { name: 'Trezor', src: 'https://placehold.co/80x30?text=Trezor' },
        { name: 'MyEtherWallet', src: 'https://placehold.co/80x30?text=MEW' },
        { name: '1inch', src: 'https://placehold.co/80x30?text=1inch' },
        { name: 'Exodus', src: 'https://placehold.co/80x30?text=Exodus' },
        { name: 'Spark', src: 'https://placehold.co/80x30?text=Spark' },
        { name: 'Magpie', src: 'https://placehold.co/80x30?text=Magpie' },
    ];

    const caseStudies = [
        {
            tag: 'Case Study',
            title: 'Trezor: 29,000 Takedowns at 99.76% Success',
            desc: 'How PhishFort scaled Trezor\'s phishing protection from 300 manual cases per year to 29,000 automated takedowns.',
            img: 'https://placehold.co/300x200/E8E8E3/1a1a1a?text=Trezor',
            bg: 'bg-primary-50'
        },
        {
            tag: 'Case Study',
            title: 'Spark: 97% Takedown Success in 8 Months',
            desc: 'Spark achieved 120+ phishing domain and social media takedowns with a 97% success rate.',
            img: 'https://placehold.co/300x200/D4C5A3/1a1a1a?text=Spark',
            bg: 'bg-gray-100'
        },
        {
            tag: 'Industry Report',
            title: 'The State of Crypto Phishing in 2025',
            desc: 'PhishFort\'s annual report on phishing threats targeting cryptocurrency brands and users.',
            img: 'https://placehold.co/300x200/E8E8E3/1a1a1a?text=Report',
            bg: 'bg-primary-50'
        },
        {
            tag: 'Whitepaper',
            title: 'AI-Powered Phishing Detection',
            desc: 'How PhishFort combines machine learning with expert analysts to achieve 98%+ takedown rates.',
            img: 'https://placehold.co/300x200/F0E6D2/1a1a1a?text=AI',
            bg: 'bg-gray-100'
        }
    ];

    const testimonials = [
        {
            quote: "They do a fantastic job... They are top tier and spring into action no matter the time of day (or night!). 10/10, will continue to work with PhishFort.",
            author: "Kosala Hemachandra",
            role: "CEO",
            company: "MyEtherWallet",
            img: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?q=80&w=400&auto=format&fit=crop"
        },
        {
            quote: "This is something that we could not achieve by ourselves manually managing this process.",
            author: "Jiří Petřík",
            role: "Head of Information Security",
            company: "Trezor",
            img: "https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?q=80&w=400&auto=format&fit=crop"
        },
        {
            quote: "Their reaction time is excellent... The team is professional, proactive, and easy to collaborate with.",
            author: "Security Leader",
            role: "Security Team",
            company: "1inch",
            img: "https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?q=80&w=400&auto=format&fit=crop"
        }
    ];
</script>

<div class="min-h-screen bg-white text-gray-900 font-sans selection:bg-gray-200">
    <!-- Header -->
    <header class="fixed top-0 left-0 right-0 z-50 bg-white/90 backdrop-blur-sm border-b border-gray-100">
        <div class="max-w-[1600px] mx-auto px-6 py-6 flex justify-between items-center">
            <div class="w-64">
                <a href="/" class="text-xl font-bold leading-tight block tracking-tight">
                    PhishFort
                </a>
            </div>
            <div>
                <a href="#" class="bg-black text-white px-5 py-2.5 text-xs font-medium rounded-sm hover:bg-gray-800 transition-colors">
                    Get Protected
                </a>
            </div>
        </div>
    </header>

    <main class="pt-32 pb-20">
        <div class="max-w-[1600px] mx-auto px-6 grid grid-cols-12 gap-8">
            <!-- Sidebar Navigation -->
            <div class="col-span-2 hidden lg:block sticky top-32 h-fit">
                <nav class="flex flex-col space-y-3 text-xs text-gray-500 font-medium">
                    <a href="#" class="text-black">Home</a>
                    <a href="#" class="hover:text-black transition-colors">Platform</a>
                    <a href="#" class="hover:text-black transition-colors">Solutions</a>
                    <a href="#" class="hover:text-black transition-colors">Case Studies</a>
                    <a href="#" class="hover:text-black transition-colors">About</a>
                </nav>
            </div>

            <!-- Main Content Area -->
            <div class="col-span-12 lg:col-span-10 space-y-32">
                
                <!-- Hero Section -->
                <section class="relative">
                    <div class="relative w-full h-[600px] overflow-hidden rounded-sm bg-gradient-to-br from-gray-950 via-gray-900 to-primary-950">
                        <!-- Background Pattern -->
                        <div class="absolute inset-0 opacity-10">
                            <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, rgba(255,255,255,0.15) 1px, transparent 0); background-size: 40px 40px;"></div>
                        </div>
                        
                        <div class="absolute inset-0 flex flex-col items-center justify-center p-12 text-center">
                            <h1 class="text-4xl md:text-5xl font-normal text-white mb-6 max-w-3xl leading-tight">
                                Eliminate phishing threats<br>with AI detection and global takedowns
                            </h1>
                            <p class="text-lg text-gray-300 mb-12 max-w-2xl">
                                98% takedown success rate. 4-6 hour average response time. 24/7 protection for your brand.
                            </p>

                            <!-- Logos Card -->
                            <div class="bg-white/95 backdrop-blur-sm p-8 rounded-sm shadow-sm max-w-3xl w-full">
                                <p class="text-[10px] text-gray-500 mb-6 uppercase tracking-wide">
                                    Trusted by leading crypto and Web3 brands
                                </p>
                                <div class="grid grid-cols-3 md:grid-cols-6 gap-8 items-center justify-items-center opacity-70">
                                    {#each customers as customer}
                                        <div class="h-6 flex items-center justify-center">
                                            <span class="text-[11px] font-semibold text-gray-800">{customer.name}</span>
                                        </div>
                                    {/each}
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- How PhishFort Works Section -->
                <section>
                    <div class="flex justify-between items-baseline mb-24 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900 max-w-xl leading-tight">
                            How PhishFort protects your brand
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Our Process</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-3 gap-12 mb-24">
                        <!-- Step 1 -->
                        <div class="space-y-4">
                            <div class="w-12 h-12 bg-primary-500 text-white flex items-center justify-center text-xl font-medium rounded-sm">
                                1
                            </div>
                            <h3 class="text-xl font-medium text-gray-900">Discover Early</h3>
                            <p class="text-sm text-gray-600 leading-relaxed">
                                AI-powered detection engine continuously scans the web, mobile app stores, social media, and dark web for brand impersonations and phishing threats before they launch.
                            </p>
                        </div>

                        <!-- Step 2 -->
                        <div class="space-y-4">
                            <div class="w-12 h-12 bg-primary-500 text-white flex items-center justify-center text-xl font-medium rounded-sm">
                                2
                            </div>
                            <h3 class="text-xl font-medium text-gray-900">React Fast</h3>
                            <p class="text-sm text-gray-600 leading-relaxed">
                                24/7 analyst teams across 21 countries validate threats and initiate takedowns through global enforcement networks. Average takedown time: 4-6 hours.
                            </p>
                        </div>

                        <!-- Step 3 -->
                        <div class="space-y-4">
                            <div class="w-12 h-12 bg-primary-500 text-white flex items-center justify-center text-xl font-medium rounded-sm">
                                3
                            </div>
                            <h3 class="text-xl font-medium text-gray-900">Adapt & Learn</h3>
                            <p class="text-sm text-gray-600 leading-relaxed">
                                Attack techniques and signatures are integrated back into detection systems, continuously improving protection and staying ahead of evolving threats.
                            </p>
                        </div>
                    </div>

                    <!-- Stats -->
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-8 p-12 bg-gray-50 rounded-sm">
                        <div class="text-center">
                            <div class="text-4xl font-light text-gray-900 mb-2">98%+</div>
                            <div class="text-xs text-gray-500 uppercase tracking-wider">Takedown Success</div>
                        </div>
                        <div class="text-center">
                            <div class="text-4xl font-light text-gray-900 mb-2">4-6h</div>
                            <div class="text-xs text-gray-500 uppercase tracking-wider">Avg Response Time</div>
                        </div>
                        <div class="text-center">
                            <div class="text-4xl font-light text-gray-900 mb-2">24/7</div>
                            <div class="text-xs text-gray-500 uppercase tracking-wider">Global Coverage</div>
                        </div>
                        <div class="text-center">
                            <div class="text-4xl font-light text-gray-900 mb-2">400M+</div>
                            <div class="text-xs text-gray-500 uppercase tracking-wider">Users Protected</div>
                        </div>
                    </div>
                </section>

                <!-- Services Section -->
                <section>
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Comprehensive brand protection services
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Our Services</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                        <!-- Service 1: Website Phishing -->
                        <div class="bg-white border border-gray-200 rounded-sm p-8 hover:border-primary-500 transition-colors group">
                            <div class="w-12 h-12 bg-primary-500 rounded-sm flex items-center justify-center mb-6 group-hover:bg-primary-600 transition-colors">
                                <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9"></path>
                                </svg>
                            </div>
                            <h3 class="text-xl font-medium text-gray-900 mb-4">Website phishing site detection & takedown</h3>
                            <p class="text-sm text-gray-600 leading-relaxed mb-6">
                                AI-powered scanning identifies fake websites impersonating your brand across the web. Our global enforcement network achieves 99%+ takedown success with 4-6 hour average response time.
                            </p>
                            <div class="flex items-center gap-2 text-xs text-primary-600 font-medium">
                                <span>Learn more</span>
                                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
                                </svg>
                            </div>
                        </div>

                        <!-- Service 2: Mobile App -->
                        <div class="bg-white border border-gray-200 rounded-sm p-8 hover:border-primary-500 transition-colors group">
                            <div class="w-12 h-12 bg-primary-500 rounded-sm flex items-center justify-center mb-6 group-hover:bg-primary-600 transition-colors">
                                <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z"></path>
                                </svg>
                            </div>
                            <h3 class="text-xl font-medium text-gray-900 mb-4">Mobile app fake app detection & removal</h3>
                            <p class="text-sm text-gray-600 leading-relaxed mb-6">
                                Continuous monitoring of Apple App Store and Google Play Store for fraudulent apps using your brand. Expert analysts work directly with platform teams to ensure rapid removal.
                            </p>
                            <div class="flex items-center gap-2 text-xs text-primary-600 font-medium">
                                <span>Learn more</span>
                                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
                                </svg>
                            </div>
                        </div>

                        <!-- Service 3: Social Media -->
                        <div class="bg-white border border-gray-200 rounded-sm p-8 hover:border-primary-500 transition-colors group">
                            <div class="w-12 h-12 bg-primary-500 rounded-sm flex items-center justify-center mb-6 group-hover:bg-primary-600 transition-colors">
                                <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8h2a2 2 0 012 2v6a2 2 0 01-2 2h-2v4l-4-4H9a1.994 1.994 0 01-1.414-.586m0 0L11 14h4a2 2 0 002-2V6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2v4l.586-.586z"></path>
                                </svg>
                            </div>
                            <h3 class="text-xl font-medium text-gray-900 mb-4">Social media brand impersonation monitoring</h3>
                            <p class="text-sm text-gray-600 leading-relaxed mb-6">
                                24/7 surveillance across major social platforms detects fake accounts, scam posts, and impersonation attempts. Our team coordinates with platform security to protect your community.
                            </p>
                            <div class="flex items-center gap-2 text-xs text-primary-600 font-medium">
                                <span>Learn more</span>
                                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
                                </svg>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- About PhishFort Section -->
                <section>
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Making the internet safer
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Our Mission</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-3 gap-12 text-sm leading-relaxed text-gray-600 mb-24">
                        <div class="space-y-6">
                            <p>
                                PhishFort's mission is to make the Internet a safer place by protecting brands, users, and communities from phishing and online threats.
                            </p>
                            <p>
                                We operate with a clear mandate for excellence and strive to be a net positive to the world, our partners, and customers.
                            </p>
                        </div>
                        <div class="space-y-6">
                            <p>
                                Starting with crypto brands, we've captured the $8B brand protection market with our industry-leading 98% takedown rate, powered by 24/7 analyst teams working across the globe.
                            </p>
                            <p>
                                Our approach combines research-led investigation, early threat discovery, rapid response, and adaptive learning to stay ahead of evolving phishing techniques.
                            </p>
                        </div>
                        <div class="space-y-6">
                            <p>
                                With team members from over 21 countries, we provide round-the-clock protection for brands and their communities. Our work directly impacts the security of over 400 million users.
                            </p>
                            <p>
                                We've built a horizontal, collaborative culture focused on solving complex problems and making a real difference in digital trust and safety.
                            </p>
                        </div>
                    </div>

                    <!-- Protection Coverage -->
                    <div class="bg-gray-50 rounded-sm p-12">
                        <div class="text-[10px] text-gray-400 uppercase tracking-wider mb-8">Complete Protection Across</div>
                        <div class="grid grid-cols-2 md:grid-cols-5 gap-8">
                            <div class="space-y-2">
                                <div class="w-10 h-10 bg-gray-900 rounded-sm flex items-center justify-center">
                                    <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9"></path></svg>
                                </div>
                                <div class="text-sm font-medium">Phishing Websites</div>
                            </div>
                            <div class="space-y-2">
                                <div class="w-10 h-10 bg-gray-900 rounded-sm flex items-center justify-center">
                                    <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z"></path></svg>
                                </div>
                                <div class="text-sm font-medium">Fake Mobile Apps</div>
                            </div>
                            <div class="space-y-2">
                                <div class="w-10 h-10 bg-gray-900 rounded-sm flex items-center justify-center">
                                    <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8h2a2 2 0 012 2v6a2 2 0 01-2 2h-2v4l-4-4H9a1.994 1.994 0 01-1.414-.586m0 0L11 14h4a2 2 0 002-2V6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2v4l.586-.586z"></path></svg>
                                </div>
                                <div class="text-sm font-medium">Social Media</div>
                            </div>
                            <div class="space-y-2">
                                <div class="w-10 h-10 bg-gray-900 rounded-sm flex items-center justify-center">
                                    <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 13V6a2 2 0 00-2-2H6a2 2 0 00-2 2v7m16 0v5a2 2 0 01-2 2H6a2 2 0 01-2-2v-5m16 0h-2.586a1 1 0 00-.707.293l-2.414 2.414a1 1 0 01-.707.293h-3.172a1 1 0 01-.707-.293l-2.414-2.414A1 1 0 006.586 13H4"></path></svg>
                                </div>
                                <div class="text-sm font-medium">Dark Web</div>
                            </div>
                            <div class="space-y-2">
                                <div class="w-10 h-10 bg-gray-900 rounded-sm flex items-center justify-center">
                                    <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
                                </div>
                                <div class="text-sm font-medium">Email Abuse</div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Platform Features Dark Section -->
                <section class="bg-gray-950 text-white rounded-sm overflow-hidden relative min-h-[500px]">
                    <!-- Background Pattern -->
                    <div class="absolute inset-0 opacity-5">
                        <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, rgba(255,255,255,0.15) 1px, transparent 0); background-size: 40px 40px;"></div>
                    </div>
                    <!-- Gradient Accent -->
                    <div class="absolute top-0 right-0 w-1/2 h-full bg-gradient-to-l from-primary-950/30 to-transparent"></div>

                    <div class="relative z-10 p-16 w-full">
                        <div class="max-w-4xl">
                            <h2 class="text-3xl font-light mb-6">
                                Enterprise-grade threat intelligence platform
                            </h2>
                            <p class="text-lg text-gray-400 mb-12 max-w-2xl">
                                Real-time monitoring, instant alerts, and comprehensive reporting for complete visibility into your brand protection.
                            </p>

                            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
                                <div class="space-y-3">
                                    <div class="flex items-start gap-3">
                                        <div class="w-5 h-5 bg-primary-500 rounded-sm flex items-center justify-center shrink-0 mt-0.5">
                                            <svg class="w-3 h-3 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path></svg>
                                        </div>
                                        <div>
                                            <div class="font-medium text-white">24/7 Private Communication Channel</div>
                                            <div class="text-sm text-gray-400">Direct line to your dedicated operations team</div>
                                        </div>
                                    </div>
                                </div>

                                <div class="space-y-3">
                                    <div class="flex items-start gap-3">
                                        <div class="w-5 h-5 bg-primary-500 rounded-sm flex items-center justify-center shrink-0 mt-0.5">
                                            <svg class="w-3 h-3 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path></svg>
                                        </div>
                                        <div>
                                            <div class="font-medium text-white">Real-Time Dashboard</div>
                                            <div class="text-sm text-gray-400">Live incident tracking and threat intelligence</div>
                                        </div>
                                    </div>
                                </div>

                                <div class="space-y-3">
                                    <div class="flex items-start gap-3">
                                        <div class="w-5 h-5 bg-primary-500 rounded-sm flex items-center justify-center shrink-0 mt-0.5">
                                            <svg class="w-3 h-3 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path></svg>
                                        </div>
                                        <div>
                                            <div class="font-medium text-white">API Integration</div>
                                            <div class="text-sm text-gray-400">Connect to your SIEM/SOC systems</div>
                                        </div>
                                    </div>
                                </div>

                                <div class="space-y-3">
                                    <div class="flex items-start gap-3">
                                        <div class="w-5 h-5 bg-primary-500 rounded-sm flex items-center justify-center shrink-0 mt-0.5">
                                            <svg class="w-3 h-3 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path></svg>
                                        </div>
                                        <div>
                                            <div class="font-medium text-white">Quarterly Business Reviews</div>
                                            <div class="text-sm text-gray-400">Comprehensive reporting and strategic insights</div>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <button class="bg-primary-500 text-white px-6 py-3 text-sm font-medium rounded-sm hover:bg-primary-600 transition-colors">
                                Schedule a Demo
                            </button>
                        </div>
                    </div>
                </section>

                <!-- Testimonials -->
                <section>
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Trusted by security leaders
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Customer Stories</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
                        {#each testimonials as testimonial}
                            <div class="bg-gray-50 p-8 rounded-sm flex flex-col">
                                <blockquote class="text-base font-light leading-relaxed mb-6 flex-grow">
                                    "{testimonial.quote}"
                                </blockquote>
                                <div class="border-t border-gray-200 pt-4">
                                    <div class="font-medium text-gray-900">{testimonial.author}</div>
                                    <div class="text-xs text-gray-500">{testimonial.role}</div>
                                    <div class="text-xs font-semibold text-gray-700 mt-1">{testimonial.company}</div>
                                </div>
                            </div>
                        {/each}
                    </div>

                    <!-- Featured Case Study -->
                    <div class="bg-gradient-to-br from-primary-950 to-gray-950 text-white p-12 rounded-sm">
                        <div class="max-w-3xl">
                            <div class="text-xs uppercase tracking-wider text-primary-300 mb-4">Featured Case Study</div>
                            <h3 class="text-2xl font-light mb-4">Trezor: From 300 to 29,000 Takedowns</h3>
                            <p class="text-gray-300 mb-6 leading-relaxed">
                                "This is something that we could not achieve by ourselves manually managing this process. PhishFort scaled our phishing protection to 29,000 takedowns with a 99.76% success rate and 4-6 hour average takedown time."
                            </p>
                            <div class="flex items-center gap-4">
                                <div class="text-sm font-medium">Jiří Petřík, Head of Information Security at Trezor</div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Resources / Case Studies -->
                <section>
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Resources & insights
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Latest</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                        {#each caseStudies as study}
                            <div class="group cursor-pointer">
                                <div class="relative aspect-square mb-6 overflow-hidden {study.bg} flex items-center justify-center rounded-sm">
                                    <span class="absolute top-4 left-4 text-[10px] uppercase tracking-wider bg-white/90 px-2 py-1 backdrop-blur-sm rounded-sm font-medium">{study.tag}</span>
                                    <div class="text-center p-6">
                                        <div class="w-16 h-16 bg-gray-900/10 rounded-full mx-auto flex items-center justify-center">
                                            <svg class="w-8 h-8 text-gray-700" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>
                                        </div>
                                    </div>
                                </div>
                                <h3 class="text-base font-medium mb-3 leading-tight group-hover:underline decoration-1 underline-offset-4">
                                    {study.title}
                                </h3>
                                <p class="text-xs text-gray-500 mb-4 leading-relaxed">
                                    {study.desc}
                                </p>
                                <a href="#" class="text-xs font-medium text-primary-600 hover:text-primary-700 underline decoration-1 underline-offset-4">Read more →</a>
                            </div>
                        {/each}
                    </div>
                </section>

            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-white pt-32 pb-12 border-t border-gray-100 relative overflow-hidden">
        <!-- Large Background Watermark -->
        <div class="absolute left-0 bottom-0 text-[20vw] font-bold text-gray-50 leading-none select-none pointer-events-none -mb-12 -ml-12">
            PhishFort
        </div>

        <div class="max-w-[1600px] mx-auto px-6 relative z-10">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-24 gap-8">
                <div>
                    <div class="text-2xl font-light mb-2">Making the internet safer</div>
                    <div class="text-sm text-gray-500">24/7 protection against phishing threats</div>
                </div>
                <div>
                    <a href="#" class="bg-primary-500 text-white px-6 py-3 text-sm font-medium rounded-sm hover:bg-primary-600 transition-colors inline-block">
                        Get Started
                    </a>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-12 gap-12 items-start mb-12">
                <div class="md:col-span-4">
                    <!-- Logo -->
                    <div class="mb-6">
                        <div class="text-2xl font-bold tracking-tight mb-3">PhishFort</div>
                        <p class="text-sm text-gray-600 leading-relaxed">
                            Protecting brands, users, and communities from phishing and online threats with AI-powered detection and global takedown networks.
                        </p>
                    </div>
                </div>
                
                <div class="md:col-span-8 grid grid-cols-2 md:grid-cols-4 gap-8">
                    <div>
                        <div class="text-xs font-semibold uppercase tracking-wider text-gray-900 mb-4">Product</div>
                        <div class="flex flex-col gap-2 text-sm text-gray-600">
                            <a href="#" class="hover:text-gray-900">Platform</a>
                            <a href="#" class="hover:text-gray-900">Features</a>
                            <a href="#" class="hover:text-gray-900">Integrations</a>
                            <a href="#" class="hover:text-gray-900">Pricing</a>
                        </div>
                    </div>
                    <div>
                        <div class="text-xs font-semibold uppercase tracking-wider text-gray-900 mb-4">Solutions</div>
                        <div class="flex flex-col gap-2 text-sm text-gray-600">
                            <a href="#" class="hover:text-gray-900">Crypto & Web3</a>
                            <a href="#" class="hover:text-gray-900">Finance</a>
                            <a href="#" class="hover:text-gray-900">Technology</a>
                            <a href="#" class="hover:text-gray-900">Enterprise</a>
                        </div>
                    </div>
                    <div>
                        <div class="text-xs font-semibold uppercase tracking-wider text-gray-900 mb-4">Resources</div>
                        <div class="flex flex-col gap-2 text-sm text-gray-600">
                            <a href="#" class="hover:text-gray-900">Case Studies</a>
                            <a href="#" class="hover:text-gray-900">Blog</a>
                            <a href="#" class="hover:text-gray-900">Documentation</a>
                            <a href="#" class="hover:text-gray-900">Support</a>
                        </div>
                    </div>
                    <div>
                        <div class="text-xs font-semibold uppercase tracking-wider text-gray-900 mb-4">Company</div>
                        <div class="flex flex-col gap-2 text-sm text-gray-600">
                            <a href="#" class="hover:text-gray-900">About</a>
                            <a href="#" class="hover:text-gray-900">Careers</a>
                            <a href="#" class="hover:text-gray-900">Contact</a>
                            <a href="#" class="hover:text-gray-900">Partners</a>
                        </div>
                    </div>
                </div>
            </div>

            <div class="border-t border-gray-200 pt-8 flex flex-col md:flex-row justify-between items-center gap-4">
                <div class="text-xs text-gray-500">
                    © 2025 PhishFort. All rights reserved.
                </div>
                <div class="flex gap-6 text-xs text-gray-500">
                    <a href="#" class="hover:text-gray-900">Privacy Policy</a>
                    <a href="#" class="hover:text-gray-900">Terms of Service</a>
                    <a href="#" class="hover:text-gray-900">Security</a>
                </div>
            </div>
        </div>
    </footer>
</div>

<style>
    /* Custom scrollbar hide for clean look */
    ::-webkit-scrollbar {
        width: 0px;
        background: transparent;
    }
</style>

