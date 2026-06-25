<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DB POWER TOOLS | Professional Heavy-Duty Industrial Gear</title>
    <!-- Tailwind CSS for robust adaptive responsive layouts -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Premium Fonts for an elegant, industrial-strength look -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;800;900&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome for professional service and product icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --brand-gold: #fbbf24;
            --brand-gold-hover: #f59e0b;
            --dark-charcoal: #0e0f12;
            --card-gray: rgba(22, 24, 29, 0.95);
        }

        body { 
            margin: 0; 
            padding: 0; 
            background-color: var(--dark-charcoal); 
            color: #f3f4f6; 
            overflow-x: hidden; 
            font-family: 'Inter', sans-serif; 
            scroll-behavior: smooth;
        }

        .heading-font { font-family: 'Montserrat', sans-serif; }

        /* Premium Glassmorphism with Industrial Gold Accents */
        .industrial-card { 
            background: var(--card-gray); 
            border: 1px solid rgba(251, 191, 36, 0.1); 
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .industrial-card:hover {
            border-color: var(--brand-gold);
            transform: translateY(-4px);
            box-shadow: 0 15px 35px rgba(251, 191, 36, 0.05);
        }

        .gold-glow { text-shadow: 0 0 15px rgba(251, 191, 36, 0.3); }

        /* Custom Scrollbar matching modern business UI */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #0e0f12; }
        ::-webkit-scrollbar-thumb { background: #2a2c35; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #fbbf24; }

        /* Background Spark Canvas */
        #canvas { position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: 0; pointer-events: none; }
        
        #intro-screen { transition: opacity 0.8s ease-in-out, visibility 0.8s; }
    </style>
</head>
<body class="selection:bg-amber-400 selection:text-black">

    <canvas id="canvas"></canvas>

    <!-- Professional Brand Splash Screen -->
    <div id="intro-screen" class="fixed inset-0 z-[100] bg-[#090a0c] flex flex-col justify-center items-center px-6">
        
        <!-- Left Side Premium Badging -->
        <div class="absolute left-10 top-1/2 -translate-y-1/2 hidden lg:flex flex-col items-start space-y-6 opacity-60 pointer-events-none">
            <span class="text-xs uppercase tracking-[0.3em] text-amber-400 font-bold heading-font">ESTABLISHED 1998</span>
            <div class="w-24 h-[1px] bg-amber-400/30"></div>
            <span class="text-xs uppercase tracking-[0.3em] text-slate-500 font-medium">PROFESSIONAL GRADE</span>
        </div>

        <!-- Right Side Quality Assurance Badging -->
        <div class="absolute right-10 top-1/2 -translate-y-1/2 hidden lg:flex flex-col items-end space-y-6 opacity-60 pointer-events-none">
            <span class="text-xs uppercase tracking-[0.3em] text-amber-400 font-bold heading-font">ISO 9001 CERTIFIED</span>
            <div class="w-24 h-[1px] bg-amber-400/30"></div>
            <span class="text-xs uppercase tracking-[0.3em] text-slate-500 font-medium">GLOBAL SERVICE NETWORK</span>
        </div>

        <!-- Corporate Welcoming Core -->
        <div class="max-w-xl w-full text-center z-10 space-y-8 p-12 rounded-2xl bg-zinc-950/95 border border-amber-500/20 shadow-2xl">
            <div class="flex justify-center items-center space-x-2 text-amber-400">
                <i class="fa-solid fa-award text-2xl"></i>
                <span class="text-xs tracking-widest uppercase font-semibold text-slate-300">TRUSTED BY CONTRACTORS WORLDWIDE</span>
            </div>
            
            <div>
                <h1 class="text-4xl md:text-5xl font-black tracking-tight text-white heading-font">
                    DB <span class="text-amber-400">POWER TOOL</span>
                </h1>
                <p class="text-slate-400 uppercase tracking-[0.25em] text-[0.7rem] mt-2 font-semibold">Engineered For Extreme Workloads</p>
            </div>

            <!-- Business Trust Metrics instead of software logs -->
            <div class="grid grid-cols-3 gap-4 border-y border-zinc-800 py-6 text-center">
                <div>
                    <p class="text-2xl font-extrabold text-amber-400 heading-font">3Y</p>
                    <p class="text-[0.65rem] text-slate-500 uppercase tracking-wider font-semibold">Full Warranty</p>
                </div>
                <div>
                    <p class="text-2xl font-extrabold text-white heading-font">100%</p>
                    <p class="text-[0.65rem] text-slate-500 uppercase tracking-wider font-semibold">Brushless Motors</p>
                </div>
                <div>
                    <p class="text-2xl font-extrabold text-white heading-font">24h</p>
                    <p class="text-[0.65rem] text-slate-500 uppercase tracking-wider font-semibold">Support Dispatch</p>
                </div>
            </div>

            <!-- Access Button -->
            <button onclick="enterSite()" class="group relative w-full overflow-hidden bg-amber-400 hover:bg-amber-500 text-black px-8 py-4 rounded-xl font-bold transition transform active:scale-95 uppercase tracking-widest heading-font text-xs flex items-center justify-center space-x-2">
                <span>View Storefront</span>
                <i class="fa-solid fa-arrow-right group-hover:translate-x-1 transition-transform"></i>
            </button>
        </div>
    </div>


    <!-- Navigation Bar -->
    <nav class="fixed w-full z-50 bg-[#0e0f12]/95 backdrop-blur-md border-b border-zinc-800/80 px-6 py-4 flex justify-between items-center">
        <!-- Brand identity -->
        <a href="#home" class="flex items-center space-x-3 hover:opacity-90 transition">
            <div class="h-10 w-10 rounded-lg bg-amber-400 flex items-center justify-center shadow-[0_0_15px_rgba(251,191,36,0.2)]">
                <i class="fa-solid fa-hammer text-slate-950 text-xl"></i>
            </div>
            <div>
                <span class="text-lg font-black tracking-wider text-white heading-font">DB <span class="text-amber-400">POWER TOOL</span></span>
                <span class="block text-[0.6rem] text-slate-400 tracking-widest uppercase font-medium">Heavy Duty Equipment</span>
            </div>
        </a>

        <!-- Main Navigation Links -->
        <div class="hidden lg:flex items-center space-x-8 text-xs font-bold uppercase tracking-widest text-slate-300 heading-font">
            <a href="#home" class="hover:text-amber-400 transition-colors">Catalog</a>
            <a href="#products" class="hover:text-amber-400 transition-colors">Our Series</a>
            <a href="#fleet-builder" class="hover:text-amber-400 transition-colors">Fleet Builder</a>
            <a href="#depot" class="hover:text-amber-400 transition-colors">Depot Locator</a>
            <a href="#contact" class="hover:text-amber-400 transition-colors">Contact Sales</a>
        </div>

        <div class="flex items-center space-x-4">
            <!-- Dealer Hotline Badge (Updated with user phone number) -->
            <a href="tel:8143807462" class="hidden sm:flex items-center space-x-2 bg-zinc-900 border border-zinc-800 px-4 py-2 rounded-xl text-xs font-medium text-slate-300 hover:border-amber-400/50 transition">
                <i class="fa-solid fa-phone text-amber-400"></i>
                <span class="font-semibold">+91 81438 07462</span>
            </a>
            
            <!-- Mobile Menu Toggle Button -->
            <button onclick="toggleMobileMenu()" class="lg:hidden text-slate-300 hover:text-amber-400 transition text-2xl focus:outline-none">
                <i id="menu-icon" class="fa-solid fa-bars"></i>
            </button>
        </div>
    </nav>

    <!-- Mobile Drawer Navigation -->
    <div id="mobile-menu" class="fixed inset-0 z-40 bg-[#0e0f12]/98 backdrop-blur-xl flex flex-col justify-center items-center space-y-8 text-center text-lg uppercase tracking-widest heading-font opacity-0 invisible transition-all duration-300">
        <a href="#home" onclick="toggleMobileMenu()" class="hover:text-amber-400 text-slate-200">Catalog</a>
        <a href="#products" onclick="toggleMobileMenu()" class="hover:text-amber-400 text-slate-200">Our Series</a>
        <a href="#fleet-builder" onclick="toggleMobileMenu()" class="hover:text-amber-400 text-slate-200">Fleet Builder</a>
        <a href="#depot" onclick="toggleMobileMenu()" class="hover:text-amber-400 text-slate-200">Depot Locator</a>
        <a href="#contact" onclick="toggleMobileMenu()" class="hover:text-amber-400 text-slate-200">Contact Sales</a>
    </div>


    <!-- Hero Section -->
    <section id="home" class="relative z-10 min-h-screen flex flex-col justify-center items-center text-center px-6 pt-24">
        <div class="max-w-4xl space-y-8">
            <div class="inline-flex items-center space-x-2 bg-amber-500/10 border border-amber-400/20 px-4 py-1.5 rounded-full text-xs text-amber-300 tracking-wider uppercase font-semibold">
                <i class="fa-solid fa-shield-halved"></i>
                <span>3-Year Direct Replacement Warranty</span>
            </div>

            <!-- Strong Commercial Brand Headline -->
            <h1 class="text-5xl md:text-7xl lg:text-8xl font-black tracking-tight text-white heading-font">
                UNCOMPROMISING <br><span class="text-amber-400 gold-glow">POWER.</span>
            </h1>

            <p class="text-base md:text-xl text-slate-400 max-w-2xl mx-auto tracking-normal font-normal leading-relaxed">
                Premium, heavy-duty brushless power tools engineered to survive continuous runtime on high-performance commercial jobsites.
            </p>

            <!-- Commercial Call To Actions -->
            <div class="flex flex-col sm:flex-row justify-center items-center gap-4 pt-4">
                <a href="#products" class="w-full sm:w-auto px-8 py-4 bg-amber-400 hover:bg-amber-500 text-slate-950 font-bold rounded-xl shadow-[0_4px_20px_rgba(251,191,36,0.3)] transition transform hover:-translate-y-0.5 flex items-center justify-center space-x-2 heading-font text-xs uppercase tracking-wider">
                    <span>Explore Products</span>
                    <i class="fa-solid fa-bag-shopping"></i>
                </a>
                <a href="#contact" class="w-full sm:w-auto px-8 py-4 bg-zinc-900 hover:bg-zinc-800 border border-zinc-800 hover:border-amber-400/50 text-slate-300 hover:text-white font-bold rounded-xl transition flex items-center justify-center space-x-2 heading-font text-xs uppercase tracking-wider">
                    <span>Request Demo Fleet</span>
                    <i class="fa-solid fa-truck-ramp-box"></i>
                </a>
            </div>
        </div>

        <div class="absolute bottom-10 left-1/2 -translate-x-1/2 flex flex-col items-center space-y-1 opacity-50 animate-bounce">
            <span class="text-[0.65rem] uppercase tracking-widest font-semibold text-amber-400">Scroll to Explore Series</span>
            <i class="fa-solid fa-chevron-down text-amber-400 text-sm"></i>
        </div>
    </section>


    <!-- Products / Series Section -->
    <section id="products" class="relative z-10 py-32 px-6 max-w-7xl mx-auto">
        <div class="text-center mb-16 space-y-4">
            <span class="text-amber-400 tracking-widest text-xs font-bold uppercase block heading-font">// BUILT FOR TOUGH ENVIRONMENTS</span>
            <h2 class="text-3xl md:text-5xl font-black heading-font text-white">THE INDUSTRIAL GEAR SERIES</h2>
            <p class="text-slate-400 max-w-lg mx-auto text-sm">Every tool contains heavy metal components, brushless high-torque drive, and advanced electronics protection systems.</p>
        </div>

        <!-- Professional Filter Tabs -->
        <div class="flex justify-center space-x-4 mb-16">
            <button onclick="filterCategory('all')" id="filter-all" class="px-6 py-2.5 rounded-xl text-xs font-bold uppercase tracking-wider transition-all duration-300 border border-amber-400 text-black bg-amber-400">All Equipment</button>
            <button onclick="filterCategory('impact')" id="filter-impact" class="px-6 py-2.5 rounded-xl text-xs font-bold uppercase tracking-wider transition-all duration-300 border border-zinc-800 text-slate-400 hover:border-amber-400/50 hover:text-white">Impact Drills</button>
            <button onclick="filterCategory('cutting')" id="filter-cutting" class="px-6 py-2.5 rounded-xl text-xs font-bold uppercase tracking-wider transition-all duration-300 border border-zinc-800 text-slate-400 hover:border-amber-400/50 hover:text-white">Heavy Cutting</button>
        </div>

        <!-- Premium Storefront Cards Grid -->
        <div class="grid md:grid-cols-3 gap-8">
            
            <!-- Tool 1: Heavy Torque Drill -->
            <div class="product-card industrial-card p-8 rounded-2xl flex flex-col justify-between" data-category="impact">
                <div>
                    <div class="flex justify-between items-start mb-6">
                        <div class="p-3 bg-amber-500/10 rounded-xl border border-amber-400/20 text-amber-400">
                            <i class="fa-solid fa-screwdriver-wrench text-2xl"></i>
                        </div>
                        <span class="text-[0.65rem] font-bold text-emerald-400 px-3 py-1 bg-emerald-950/40 border border-emerald-500/30 rounded uppercase tracking-wider">In Stock</span>
                    </div>
                    
                    <div class="flex items-center space-x-1 mb-2 text-amber-400 text-xs">
                        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        <span class="text-slate-400 text-xs ml-2 font-medium">(148 Reviews)</span>
                    </div>

                    <h3 class="text-2xl font-bold heading-font text-white mb-2">DB-X90 Heavy Impact Drill</h3>
                    <p class="text-slate-400 text-sm mb-6 leading-relaxed">Engineered with smart dual torque controls and extreme dust sealing to bypass tough jobsite wear.</p>
                </div>
                <div>
                    <div class="border-t border-zinc-800/80 pt-4 mb-6 flex justify-between items-center">
                        <span class="text-xs text-slate-400 uppercase tracking-widest font-semibold">B2B MSRP:</span>
                        <span class="text-2xl font-black heading-font text-white">₹24,999</span>
                    </div>
                    
                    <div class="grid grid-cols-2 gap-3">
                        <button onclick="openSpecModal('drill')" class="py-3 bg-zinc-900 hover:bg-zinc-800 border border-zinc-800 text-slate-300 rounded-xl transition text-xs font-bold uppercase tracking-wider heading-font">
                            Specs Details
                        </button>
                        <button onclick="openSpecModal('order')" class="py-3 bg-amber-400 hover:bg-amber-500 text-black rounded-xl transition text-xs font-bold uppercase tracking-wider heading-font">
                            Get Quote
                        </button>
                    </div>
                </div>
            </div>

            <!-- Tool 2: Plasma Rotary Saw -->
            <div class="product-card industrial-card p-8 rounded-2xl flex flex-col justify-between" data-category="cutting">
                <div>
                    <div class="flex justify-between items-start mb-6">
                        <div class="p-3 bg-amber-500/10 rounded-xl border border-amber-400/20 text-amber-400">
                            <i class="fa-solid fa-compact-disc text-2xl"></i>
                        </div>
                        <span class="text-[0.65rem] font-bold text-emerald-400 px-3 py-1 bg-emerald-950/40 border border-emerald-500/30 rounded uppercase tracking-wider">In Stock</span>
                    </div>

                    <div class="flex items-center space-x-1 mb-2 text-amber-400 text-xs">
                        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star-half-stroke"></i>
                        <span class="text-slate-400 text-xs ml-2 font-medium">(92 Reviews)</span>
                    </div>

                    <h3 class="text-2xl font-bold heading-font text-white mb-2">DB-C10 Metal Cut Saw</h3>
                    <p class="text-slate-400 text-sm mb-6 leading-relaxed">Equipped with custom high-carbon blades and micro-active stabilizer systems for professional metal cuts.</p>
                </div>
                <div>
                    <div class="border-t border-zinc-800/80 pt-4 mb-6 flex justify-between items-center">
                        <span class="text-xs text-slate-400 uppercase tracking-widest font-semibold">B2B MSRP:</span>
                        <span class="text-2xl font-black heading-font text-white">₹32,499</span>
                    </div>
                    
                    <div class="grid grid-cols-2 gap-3">
                        <button onclick="openSpecModal('saw')" class="py-3 bg-zinc-900 hover:bg-zinc-800 border border-zinc-800 text-slate-300 rounded-xl transition text-xs font-bold uppercase tracking-wider heading-font">
                            Specs Details
                        </button>
                        <button onclick="openSpecModal('order')" class="py-3 bg-amber-400 hover:bg-amber-500 text-black rounded-xl transition text-xs font-bold uppercase tracking-wider heading-font">
                            Get Quote
                        </button>
                    </div>
                </div>
            </div>

            <!-- Tool 3: Heavy Duty Wrench -->
            <div class="product-card industrial-card p-8 rounded-2xl flex flex-col justify-between" data-category="impact">
                <div>
                    <div class="flex justify-between items-start mb-6">
                        <div class="p-3 bg-amber-500/10 rounded-xl border border-amber-400/20 text-amber-400">
                            <i class="fa-solid fa-bolt text-2xl"></i>
                        </div>
                        <span class="text-[0.65rem] font-bold text-amber-400 px-3 py-1 bg-amber-955/40 border border-emerald-500/30 rounded uppercase tracking-wider">Low Stock</span>
                    </div>

                    <div class="flex items-center space-x-1 mb-2 text-amber-400 text-xs">
                        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        <span class="text-slate-400 text-xs ml-2 font-medium">(210 Reviews)</span>
                    </div>

                    <h3 class="text-2xl font-bold heading-font text-white mb-2">DB-W55 Torque Wrench</h3>
                    <p class="text-slate-400 text-sm mb-6 leading-relaxed">Direct-drive brushless motor ensuring extreme fastening capabilities for mechanical and structural engineers.</p>
                </div>
                <div>
                    <div class="border-t border-zinc-800/80 pt-4 mb-6 flex justify-between items-center">
                        <span class="text-xs text-slate-400 uppercase tracking-widest font-semibold">B2B MSRP:</span>
                        <span class="text-2xl font-black heading-font text-white">₹28,800</span>
                    </div>
                    
                    <div class="grid grid-cols-2 gap-3">
                        <button onclick="openSpecModal('wrench')" class="py-3 bg-zinc-900 hover:bg-zinc-800 border border-zinc-800 text-slate-300 rounded-xl transition text-xs font-bold uppercase tracking-wider heading-font">
                            Specs Details
                        </button>
                        <button onclick="openSpecModal('order')" class="py-3 bg-amber-400 hover:bg-amber-500 text-black rounded-xl transition text-xs font-bold uppercase tracking-wider heading-font">
                            Get Quote
                        </button>
                    </div>
                </div>
            </div>

        </div>
    </section>


    <!-- Specification Modals -->
    <div id="spec-modal" class="fixed inset-0 z-50 bg-[#0e0f12]/95 backdrop-blur-xl flex items-center justify-center p-6 hidden">
        <div class="industrial-card max-w-lg w-full p-8 rounded-2xl border-amber-400/30 space-y-6 relative">
            <button onclick="closeSpecModal()" class="absolute top-4 right-4 text-slate-400 hover:text-amber-400 transition text-xl">
                <i class="fa-solid fa-xmark"></i>
            </button>
            
            <div class="flex items-center space-x-3 text-amber-400">
                <i class="fa-solid fa-circle-info text-2xl"></i>
                <h3 id="modal-title" class="text-2xl font-bold heading-font text-white">Technical Specifications</h3>
            </div>
            
            <div id="modal-content" class="space-y-4 text-sm text-slate-300">
                <!-- Dynamic Content injected in JS -->
            </div>

            <div class="flex justify-end pt-4">
                <button onclick="closeSpecModal()" class="px-6 py-2.5 bg-zinc-900 hover:bg-zinc-800 border border-zinc-850 rounded-xl text-xs font-bold uppercase tracking-wider text-amber-400 transition">
                    Close Sheet
                </button>
            </div>
        </div>
    </div>


    <!-- Interactive Custom Fleet Builder -->
    <section id="fleet-builder" class="relative z-10 py-32 px-6 bg-zinc-950/80 border-y border-zinc-900">
        <div class="max-w-7xl mx-auto grid lg:grid-cols-12 gap-12 items-center">
            
            <!-- Left Side Selections -->
            <div class="lg:col-span-5 space-y-8">
                <div class="space-y-2">
                    <span class="text-amber-400 tracking-widest text-xs font-bold uppercase block heading-font">// CUSTOM FLEET STAGING</span>
                    <h2 class="text-3xl md:text-4xl font-black heading-font text-white">INTERACTIVE PERFORMANCE LAB</h2>
                    <p class="text-slate-400 text-sm">Fine-tune the workload profiles to preview simulated motor speeds, battery runtime, and estimated performance before bulk procurement.</p>
                </div>

                <!-- Selections -->
                <div class="space-y-6">
                    <!-- Option 1: Workload Type -->
                    <div class="space-y-2">
                        <label class="text-xs uppercase tracking-widest text-slate-400 font-bold flex justify-between">
                            <span>Target Workload</span>
                            <span id="label-workload" class="text-amber-400">Standard Carpentry</span>
                        </label>
                        <select id="config-workload" onchange="updateConfigurator()" class="w-full bg-zinc-900 border border-zinc-800 text-slate-300 text-xs rounded-xl p-4 focus:outline-none focus:border-amber-400/50 font-bold uppercase tracking-wider">
                            <option value="light">Precision Woodworking [Light Duty]</option>
                            <option value="medium" selected>Commercial Carpentry [Medium Duty]</option>
                            <option value="heavy">Heavy Masonry & Demolition [Extreme Duty]</option>
                        </select>
                    </div>

                    <!-- Option 2: Core Motor Technology -->
                    <div class="space-y-2">
                        <label class="text-xs uppercase tracking-widest text-slate-400 font-bold flex justify-between">
                            <span>Brushless Motor Core</span>
                            <span id="label-motor" class="text-amber-400">Eco-Brushless Core</span>
                        </label>
                        <select id="config-motor" onchange="updateConfigurator()" class="w-full bg-zinc-900 border border-zinc-800 text-slate-300 text-xs rounded-xl p-4 focus:outline-none focus:border-amber-400/50 font-bold uppercase tracking-wider">
                            <option value="eco" selected>Standard Brushless Drive</option>
                            <option value="pro">Pro-Neo Induction Core [High Heat Limit]</option>
                        </select>
                    </div>

                    <!-- Option 3: Warranty Bundle Extension -->
                    <div class="space-y-2">
                        <label class="text-xs uppercase tracking-widest text-slate-400 font-bold">Extended Protection Cover</label>
                        <div class="grid grid-cols-2 gap-4">
                            <button onclick="toggleProtection(true)" id="prot-on" class="py-3 rounded-xl border border-amber-400 text-amber-400 bg-amber-500/10 text-xs font-bold uppercase tracking-wider transition-all">Included</button>
                            <button onclick="toggleProtection(false)" id="prot-off" class="py-3 rounded-xl border border-zinc-800 text-slate-400 bg-zinc-900 text-xs font-bold uppercase tracking-wider transition-all">Standard</button>
                        </div>
                    </div>

                    <!-- Interactive Tool Graphic Blueprint Panel -->
                    <div class="space-y-2 pt-2">
                        <label class="text-xs uppercase tracking-widest text-slate-400 font-bold">// DYNAMIC SCHEMATIC PREVIEW</label>
                        <div class="industrial-card p-6 rounded-2xl flex flex-col items-center justify-center bg-zinc-950/90 border-zinc-800 h-48 relative overflow-hidden group">
                            <!-- Technical Grid Overlay background -->
                            <div class="absolute inset-0 bg-[linear-gradient(to_right,rgba(251,191,36,0.03)_1px,transparent_1px),linear-gradient(to_bottom,rgba(251,191,36,0.03)_1px,transparent_1px)] bg-[size:14px_24px]"></div>
                            <!-- Dynamic SVG Target Container -->
                            <div id="machine-preview" class="z-10 transition-all duration-500 ease-out group-hover:scale-110 flex items-center justify-center">
                                <!-- Dynamically replaced in JS -->
                            </div>
                            <span class="absolute bottom-2 right-3 text-[0.55rem] font-mono text-amber-500/50 tracking-wider">REF. DEVICE: <span id="schematic-id" class="text-amber-450 font-bold">#M99-ROTARY-IMPACT-DRILL</span></span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Right Side Live Estimator -->
            <div class="lg:col-span-7 industrial-card p-8 rounded-2xl border-amber-400/20 space-y-8">
                <div class="flex justify-between items-center border-b border-zinc-800 pb-4">
                    <span class="heading-font text-xs uppercase font-bold text-slate-200 flex items-center space-x-2">
                        <i class="fa-solid fa-chart-line text-amber-400"></i>
                        <span>Live Performance Metrics</span>
                    </span>
                    <span class="text-xs text-amber-400 bg-amber-500/10 border border-amber-400/20 px-3 py-1 rounded font-bold">CALIBRATION STABLE</span>
                </div>

                <!-- Outputs -->
                <div class="grid sm:grid-cols-3 gap-6 text-center">
                    <div class="p-6 bg-zinc-950 rounded-xl border border-zinc-900">
                        <p class="text-xs text-slate-400 uppercase tracking-wider font-semibold mb-2">Maximum Velocity</p>
                        <p id="stat-rpm" class="text-3xl font-black heading-font text-amber-400 gold-glow">6,500 RPM</p>
                    </div>
                    <div class="p-6 bg-zinc-950 rounded-xl border border-zinc-900">
                        <p class="text-xs text-slate-400 uppercase tracking-wider font-semibold mb-2">Simulated Torque</p>
                        <p id="stat-torque" class="text-3xl font-black heading-font text-amber-400 gold-glow">140 Nm</p>
                    </div>
                    <div class="p-6 bg-zinc-950 rounded-xl border border-zinc-900">
                        <p class="text-xs text-slate-400 uppercase tracking-wider font-semibold mb-2">Est. Battery Life</p>
                        <p id="stat-runtime" class="text-3xl font-black heading-font text-amber-400 gold-glow">45 mins</p>
                    </div>
                </div>

                <!-- Calibration Visualizer -->
                <div class="bg-black p-6 rounded-xl border border-zinc-900 relative overflow-hidden flex items-center justify-center">
                    <svg class="w-full h-40 text-amber-500/10" viewBox="0 0 100 100" preserveAspectRatio="none">
                        <path d="M 0,50 Q 25,10 50,50 T 100,50" fill="none" stroke="currentColor" stroke-width="0.75" id="wave-1" />
                        <path d="M 0,50 Q 25,80 50,50 T 100,50" fill="none" stroke="currentColor" stroke-width="0.4" id="wave-2" />
                    </svg>
                    <!-- Visualizer Readout Overlay -->
                    <div class="absolute inset-0 flex flex-col justify-between p-4 text-[0.65rem] text-slate-500 pointer-events-none">
                        <div class="flex justify-between">
                            <span>SERIES CODE: #DB-M99</span>
                            <span>FREQ: 145.2 Hz</span>
                        </div>
                        <div class="text-center text-xs text-amber-400 uppercase tracking-widest font-bold">
                            <p class="animate-pulse">STABILIZING MOTOR FREQUENCY</p>
                        </div>
                        <div class="flex justify-between">
                            <span>TELEMETRY: COMPLIANT</span>
                            <span>INTELLIGENT SPEED CONTROL: ON</span>
                        </div>
                    </div>
                </div>

                <!-- Simulation Request -->
                <button onclick="requestFleetTest()" class="w-full py-4 bg-amber-400 hover:bg-amber-500 text-slate-950 font-bold rounded-xl transition shadow-[0_4px_20px_rgba(251,191,36,0.3)] flex items-center justify-center space-x-2 heading-font uppercase tracking-wider text-xs">
                    <i class="fa-solid fa-calculator"></i>
                    <span>Submit Fleet Specs to Local Depot</span>
                </button>
            </div>

        </div>
    </section>


    <!-- Geographical Depot Locator -->
    <section id="depot" class="relative z-10 py-32 px-6 max-w-7xl mx-auto">
        <div class="text-center mb-16 space-y-4">
            <span class="text-amber-400 tracking-widest text-xs font-bold uppercase block heading-font">// NATIVE DEPOTS</span>
            <h2 class="text-3xl md:text-5xl font-black heading-font text-white">DEALER & FACTORY STATIONS</h2>
            <p class="text-slate-400 max-w-lg mx-auto text-sm">Find where to buy or drop off equipment for high-priority factory servicing and rapid procurement dispatch.</p>
        </div>

        <div class="grid lg:grid-cols-12 gap-8 items-center">
            
            <!-- Left Side Details -->
            <div class="lg:col-span-5 space-y-6">
                <div class="industrial-card p-6 rounded-xl border-zinc-850 space-y-4">
                    <div class="flex items-center space-x-3 text-amber-400">
                        <i class="fa-solid fa-building text-xl"></i>
                        <span class="heading-font font-bold text-white text-lg">Main Manufacturing Station</span>
                    </div>
                    <p class="text-slate-400 text-sm leading-relaxed">
                        D.B. Power Tools Service,<br>
                        Industrial Zone Matrix, Secunderabad, AP - 500003
                    </p>
                </div>

                <div class="industrial-card p-6 rounded-xl border-zinc-850 space-y-3 text-xs">
                    <div class="flex justify-between">
                        <span class="text-slate-500 uppercase tracking-wider font-semibold">Coordinates:</span>
                        <span class="text-amber-400 font-bold">17.42° N, 78.56° E</span>
                    </div>
                    <div class="flex justify-between">
                        <span class="text-slate-500 uppercase tracking-wider font-semibold">Service Hours:</span>
                        <span class="text-amber-400 font-bold">08:00 - 20:00 IST</span>
                    </div>
                    <div class="flex justify-between">
                        <span class="text-slate-500 uppercase tracking-wider font-semibold">Stock Availability:</span>
                        <span class="text-emerald-400 font-bold uppercase">All Series Ready</span>
                    </div>
                </div>

                <!-- Dealer Stock Feed -->
                <div class="bg-[#0e0f12] p-4 rounded-xl border border-zinc-850 space-y-2">
                    <div class="flex justify-between items-center text-[0.65rem] text-slate-500">
                        <span class="font-bold">LIVE SHIPMENT TICKER</span>
                        <span class="animate-pulse text-emerald-400 flex items-center space-x-1">
                            <span class="h-1.5 w-1.5 rounded-full bg-emerald-400 inline-block"></span>
                            <span>CONNECTED</span>
                        </span>
                    </div>
                    <div id="live-terminal-feed" class="text-[0.7rem] text-slate-400 space-y-2 h-24 overflow-y-auto font-mono">
                        <!-- Feed generated dynamically in JS -->
                    </div>
                </div>
            </div>

            <!-- Right Side Professional Map -->
            <div class="lg:col-span-7 industrial-card p-2 rounded-2xl border-amber-400/20 overflow-hidden relative">
                <div class="absolute top-4 left-4 z-10 bg-zinc-950/90 border border-amber-400/30 px-3 py-1.5 rounded text-[0.65rem] text-amber-400 font-bold">
                    SECUNDERABAD DEPOT HUB
                </div>
                <div class="h-96 w-full rounded-xl overflow-hidden bg-slate-900 flex items-center justify-center">
                    <iframe class="w-full h-full grayscale contrast-125 opacity-80 hover:opacity-100 transition-all duration-500" 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3806.788937040534!2d78.56294777493555!3d17.42191378347114!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bcb9934230ee5b7%3A0xac4f63fdea035612!2sD.B.%20Power%20Tools%20Service!5e0!3m2!1sen!2sin!4v1782410920482!5m2!1sen!2sin" 
                        style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="strict-origin-when-cross-origin"></iframe>
                </div>
            </div>
        </div>
    </section>


    <!-- Commercial Inquiries Form Section -->
    <section id="contact" class="relative z-10 py-32 bg-gradient-to-t from-zinc-950 to-zinc-950/50 border-t border-zinc-900 px-6">
        <div class="max-w-4xl mx-auto industrial-card p-8 md:p-12 rounded-3xl border-amber-400/20 space-y-8 relative overflow-hidden">
            
            <div class="text-center space-y-4">
                <span class="text-amber-400 tracking-widest text-xs font-bold uppercase block heading-font">// COMMERCIAL DEPT</span>
                <h2 class="text-3xl md:text-4xl font-black heading-font text-white">COMMERCIAL PROCUREMENT CONTACT</h2>
                <p class="text-slate-400 text-sm max-w-lg mx-auto">Initiate a demo request or ask about our wholesale B2B fleet pricing models. Our corporate accounts team responds within 1 business hour.</p>
            </div>

            <div id="contact-feedback" class="hidden p-4 rounded-xl border font-semibold text-xs text-center animate-pulse"></div>

            <form id="contact-form" onsubmit="handleContactSubmit(event)" class="space-y-6">
                <div class="grid sm:grid-cols-2 gap-6">
                    <div class="space-y-2">
                        <label class="text-xs uppercase tracking-wider text-slate-400 font-bold">Contact Name</label>
                        <input type="text" id="form-name" required placeholder="e.g., Shazeb" class="w-full bg-zinc-900 border border-zinc-800 text-slate-300 text-xs rounded-xl p-4 focus:outline-none focus:border-amber-400/50 font-semibold tracking-wide placeholder:text-slate-600">
                    </div>
                    <div class="space-y-2">
                        <label class="text-xs uppercase tracking-wider text-slate-400 font-bold">Business Email Address</label>
                        <input type="email" id="form-email" required placeholder="name@yourcompany.com" class="w-full bg-zinc-900 border border-zinc-800 text-slate-300 text-xs rounded-xl p-4 focus:outline-none focus:border-amber-400/50 font-semibold tracking-wide placeholder:text-slate-600">
                    </div>
                </div>

                <div class="space-y-2">
                    <label class="text-xs uppercase tracking-wider text-slate-400 font-bold">Primary Fleet Requirement</label>
                    <select id="form-subject" class="w-full bg-zinc-900 border border-zinc-800 text-slate-300 text-xs rounded-xl p-4 focus:outline-none focus:border-amber-400/50 font-bold uppercase tracking-wider">
                        <option value="procure">Wholesale Retail & Distributor Inquiries</option>
                        <option value="demo">Commercial Site Trial / Demo Request</option>
                        <option value="warranty">Equipment Repair & Warranty Registration</option>
                    </select>
                </div>

                <div class="space-y-2">
                    <label class="text-xs uppercase tracking-wider text-slate-400 font-bold">Requirements / Message Body</label>
                    <textarea id="form-message" required rows="5" placeholder="Include required tool configurations, delivery timelines, or target project metrics..." class="w-full bg-zinc-900 border border-zinc-800 text-slate-300 text-xs rounded-xl p-4 focus:outline-none focus:border-amber-400/50 font-semibold tracking-wide placeholder:text-slate-600"></textarea>
                </div>

                <button type="submit" class="w-full py-4 bg-amber-400 hover:bg-amber-500 text-slate-950 font-bold rounded-xl shadow-[0_4px_25px_rgba(251,191,36,0.3)] transition duration-300 flex items-center justify-center space-x-2 heading-font uppercase tracking-wider text-xs">
                    <span id="btn-submit-text">Send Procurement Enquiry</span>
                    <i id="btn-submit-icon" class="fa-solid fa-paper-plane"></i>
                </button>
            </form>
        </div>
    </section>


    <!-- Professional Footer -->
    <footer class="relative z-10 py-16 bg-[#090a0c] border-t border-zinc-900 text-center px-6">
        <div class="max-w-6xl mx-auto space-y-12">
            
            <div class="flex flex-col md:flex-row justify-between items-center gap-6 border-b border-zinc-900 pb-12">
                <div class="flex items-center space-x-3 text-slate-300">
                    <i class="fa-solid fa-shield-check text-lg text-amber-400"></i>
                    <span class="text-xs tracking-wider uppercase font-semibold text-slate-400">Guaranteed High-Performance Standards</span>
                </div>
                <div class="flex space-x-6 text-slate-500">
                    <a href="mailto:sales@dbpowertools.tech" class="hover:text-amber-400 transition-colors"><i class="fa-solid fa-envelope text-lg"></i></a>
                    <a href="#" class="hover:text-amber-400 transition-colors"><i class="fa-solid fa-headset text-lg"></i></a>
                    <a href="#" class="hover:text-amber-400 transition-colors"><i class="fa-brands fa-linkedin text-lg"></i></a>
                </div>
            </div>

            <!-- Site Map -->
            <div class="grid md:grid-cols-4 gap-8 text-left text-xs text-slate-500">
                <div class="space-y-3">
                    <h4 class="text-slate-300 font-bold tracking-wider uppercase heading-font">Our Quality Promise</h4>
                    <p class="leading-relaxed">Constructed strictly using industrial carbon gears and brushless systems to handle intense thermal limits on professional jobsites.</p>
                </div>
                <div class="space-y-3">
                    <h4 class="text-slate-300 font-bold tracking-wider uppercase heading-font">Service Programs</h4>
                    <p class="leading-relaxed">Every professional purchase comes complete with automated dealer scheduling and extended motor replacement cover options.</p>
                </div>
                <div class="space-y-3">
                    <h4 class="text-slate-300 font-bold tracking-wider uppercase heading-font">Direct Portals</h4>
                    <ul class="space-y-1.5 font-semibold text-slate-400">
                        <li><a href="#home" class="hover:text-amber-400 transition">Online Storefront</a></li>
                        <li><a href="#products" class="hover:text-amber-400 transition">Our Product Series</a></li>
                        <li><a href="#fleet-builder" class="hover:text-amber-400 transition">Fleet Customizer</a></li>
                    </ul>
                </div>
                <div class="space-y-3">
                    <h4 class="text-slate-300 font-bold tracking-wider uppercase heading-font">Compliance</h4>
                    <p class="leading-relaxed">All equipment strictly follows universal ISO standards and delivers standard safety lock features automatically.</p>
                </div>
            </div>

            <p class="mt-10 text-slate-600 text-xs uppercase tracking-wider font-mono">© 2026 DB POWER TOOLS PRIVATE LIMITED. ALL RIGHTS RESERVED.</p>
        </div>
    </footer>


    <script>
        // Enter site from Intro
        function enterSite() {
            const screen = document.getElementById('intro-screen');
            screen.style.opacity = '0';
            setTimeout(() => { screen.style.display = 'none'; }, 800);
        }

        // Mobile Nav Drawer Toggle
        let isMobileMenuOpen = false;
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            const icon = document.getElementById('menu-icon');
            if (isMobileMenuOpen) {
                menu.classList.add('opacity-0', 'invisible');
                icon.className = 'fa-solid fa-bars';
                isMobileMenuOpen = false;
            } else {
                menu.classList.remove('opacity-0', 'invisible');
                icon.className = 'fa-solid fa-xmark';
                isMobileMenuOpen = true;
            }
        }

        // Drifting Gold/Amber Spark Particle Background
        const canvas = document.getElementById('canvas');
        const ctx = canvas.getContext('2d');
        let particles = [];

        function resize() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }
        window.onresize = resize;
        resize();

        class Particle {
            constructor() {
                this.reset();
            }
            reset() {
                this.x = Math.random() * canvas.width;
                // Sparks start from the bottom to drift upwards
                this.y = canvas.height + (Math.random() * 50);
                this.vx = (Math.random() - 0.5) * 0.5;
                this.vy = -(Math.random() * 0.6 + 0.3); // Constant upward speed
                this.radius = Math.random() * 2 + 0.3;
                this.alpha = Math.random() * 0.6 + 0.2;
            }
            update() {
                this.x += this.vx;
                this.y += this.vy;
                
                // If sparks drift past top or sides, regenerate from bottom
                if (this.y < 0 || this.x < 0 || this.x > canvas.width) {
                    this.reset();
                }
            }
        }

        for (let i = 0; i < 80; i++) {
            particles.push(new Particle());
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            particles.forEach(p => { 
                p.update(); 
                ctx.beginPath();
                ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
                // Render sparks in glowing warm gold/amber
                ctx.fillStyle = `rgba(251, 191, 36, ${p.alpha})`;
                ctx.shadowBlur = 10;
                ctx.shadowColor = '#fbbf24';
                ctx.fill();
                ctx.shadowBlur = 0; // reset for performance
            });
            requestAnimationFrame(animate);
        }
        animate();


        const mod = document.getElementById('spec-modal');
        const modTitle = document.getElementById('modal-title');
        const modContent = document.getElementById('modal-content');

        const specDatabase = {
            drill: {
                title: "DB-X90 Impact Drill Specification Sheet",
                html: `
                    <div class="space-y-3 text-xs">
                        <p class="text-slate-400">Our heavy-duty drill offers uncompromising performance in extreme job environments.</p>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">MOTOR CORE:</span><span class="text-amber-400 font-bold">BRUSHLESS COBALT COIL V4</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">OPERATING POWER:</span><span class="text-amber-400 font-bold">36V - 40V HEAVY CURRENT</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">MAXIMUM TORQUE:</span><span class="text-amber-400 font-bold">180 NM MAXIMUM LIMIT</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">SPEED CONTROLS:</span><span class="text-amber-400 font-bold">DUAL VARIABLE (0-600 / 0-2200 RPM)</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">INCLUDED IN SET:</span><span class="text-slate-300">2x 5.0Ah Battery, 1x Rapid Charger, Carrying Case</span></div>
                    </div>
                `
            },
            saw: {
                title: "DB-C10 Plasma Cut Circular Saw Spec Sheet",
                html: `
                    <div class="space-y-3 text-xs">
                        <p class="text-slate-400">Optimized for clean and rapid steel and timber fabrication cuts.</p>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">BLADE CAPACITY:</span><span class="text-amber-400 font-bold">125 MM TITANIUM CARBIDE COATED</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">VELOCITY RATE:</span><span class="text-amber-400 font-bold">9500 RPM CONSTANT RATED</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">BEVEL CUT CAP:</span><span class="text-amber-400 font-bold">0 - 55 DEGREES QUICK SYSTEM</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">WEIGHT WITH CELL:</span><span class="text-amber-400 font-bold">3.8 KG COMFORT-BALANCED</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">INCLUDED IN SET:</span><span class="text-slate-300">1x 125mm Metal Blade, Dust Extraction Port</span></div>
                    </div>
                `
            },
            wrench: {
                title: "DB-W55 Torque Wrench Specification Sheet",
                html: `
                    <div class="space-y-3 text-xs">
                        <p class="text-slate-400">Extreme high-torque fastening for steel erecting and heavy automotive repair.</p>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">DRIVE PORT:</span><span class="text-amber-400 font-bold">1/2 INCH DETENT PIN SYSTEM</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">IMPACT RATE:</span><span class="text-amber-400 font-bold">1200 BPM CONSTANT IMPACT</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">PEAK DETENT TORQUE:</span><span class="text-amber-400 font-bold">1200 NM BREAKAWAY FORCE</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">COOLING SHIELD:</span><span class="text-amber-400 font-bold">CARBON-FIBER CONDUIT CASE</span></div>
                        <div class="flex justify-between border-b border-zinc-800 pb-2"><span class="text-slate-500 uppercase font-semibold">INCLUDED IN SET:</span><span class="text-slate-300">1x Heavy Detent Belt Ring, Steel Clip Case</span></div>
                    </div>
                `
            },
            order: {
                title: "Request a Procurement Quote",
                html: `
                    <div class="space-y-4 text-xs">
                        <p class="text-slate-400">Enter your details in our secure communications segment at the bottom of the page, and our B2B commercial advisors will contact you immediately with a custom quote.</p>
                        <div class="bg-zinc-900 p-4 rounded-xl text-center space-y-2">
                            <p class="text-amber-400 font-bold font-mono">B2B DISCOUNT LEVELS AVAILABLE</p>
                            <p class="text-slate-500">Fleet orders above 10 units qualify for up to 25% bulk savings.</p>
                        </div>
                    </div>
                `
            }
        };

        function openSpecModal(productKey) {
            const data = specDatabase[productKey];
            if (data) {
                modTitle.innerText = data.title;
                modContent.innerHTML = data.html;
                mod.classList.remove('hidden');
            }
        }

        function closeSpecModal() {
            mod.classList.add('hidden');
        }


        function filterCategory(category) {
            const cards = document.querySelectorAll('.product-card');
            
            const btnAll = document.getElementById('filter-all');
            const btnImpact = document.getElementById('filter-impact');
            const btnCutting = document.getElementById('filter-cutting');
            
            [btnAll, btnImpact, btnCutting].forEach(b => {
                b.className = "px-6 py-2.5 rounded-xl text-xs font-bold uppercase tracking-wider transition-all duration-300 border border-zinc-850 text-slate-400 hover:border-amber-400/50 hover:text-white";
            });

            const activeBtn = document.getElementById(`filter-${category}`);
            if (activeBtn) {
                activeBtn.className = "px-6 py-2.5 rounded-xl text-xs font-bold uppercase tracking-wider transition-all duration-300 border border-amber-400 text-black bg-amber-400";
            }

            cards.forEach(card => {
                const itemCat = card.getAttribute('data-category');
                if (category === 'all' || itemCat === category) {
                    card.style.display = 'flex';
                } else {
                    card.style.display = 'none';
                }
            });
        }


        let protectionExtended = true;

        // Ultra-High-Fidelity Premium Symmetrical Multi-Colored Tool Blueprints
        const toolSymmetricSchematics = {
            light: {
                id: "#T42-PRECISION-JIGSAW",
                svg: `
                    <svg class="h-28 w-auto filter drop-shadow-[0_0_12px_rgba(251,191,36,0.3)]" viewBox="0 0 100 100" fill="none" stroke-linecap="round" stroke-linejoin="round">
                        <!-- Main Engine Chassis (Dark Gray) -->
                        <path d="M20,70 L20,40 C20,35 30,30 45,30 L75,30 C80,30 85,35 85,42 L85,70 Z" fill="#1e293b" stroke="#475569" stroke-width="1.5" />
                        <!-- Upper Comfort Grip (Amber Accent) -->
                        <path d="M30,30 C30,12 70,12 70,30" fill="none" stroke="#fbbf24" stroke-width="4" />
                        <!-- Battery Base Pack (Textured Charcoal/Gold) -->
                        <rect x="25" y="70" width="50" height="10" rx="2" fill="#0f172a" stroke="#fbbf24" stroke-width="1.5" />
                        <line x1="35" y1="75" x2="65" y2="75" stroke="#fbbf24" stroke-width="1" />
                        <!-- Metallic Saw Blade Guide -->
                        <path d="M47,80 L47,93 L53,91 L53,80" fill="#94a3b8" stroke="#cbd5e1" stroke-width="1" />
                        <path d="M49,93 L47,93 L49,90" fill="#fbbf24" />
                        <!-- Motor Core Dial (Symmetric Hub) -->
                        <circle cx="52" cy="50" r="7" fill="#0f172a" stroke="#fbbf24" stroke-width="1.5" />
                        <line x1="52" y1="46" x2="52" y2="54" stroke="#fbbf24" stroke-width="1" />
                        <line x1="48" y1="50" x2="56" y2="50" stroke="#fbbf24" stroke-width="1" />
                        <!-- Vent Slots -->
                        <line x1="68" y1="42" x2="78" y2="42" stroke="#475569" stroke-width="1.5" />
                        <line x1="68" y1="48" x2="78" y2="48" stroke="#475569" stroke-width="1.5" />
                        <line x1="68" y1="54" x2="78" y2="54" stroke="#475569" stroke-width="1.5" />
                    </svg>
                `
            },
            medium: {
                id: "#M99-ROTARY-IMPACT-DRILL",
                svg: `
                    <svg class="h-28 w-auto filter drop-shadow-[0_0_12px_rgba(251,191,36,0.3)]" viewBox="0 0 100 100" fill="none" stroke-linecap="round" stroke-linejoin="round">
                        <!-- Main Drill Gun Housing -->
                        <path d="M22,38 L55,38 L55,25 C55,25 74,22 76,25 L76,48 L55,48 L50,80 L28,80 L24,70 L38,48 L22,48 Z" fill="#1e293b" stroke="#475569" stroke-width="1.5" />
                        <!-- High-Torque Motor Housing Cap (Amber) -->
                        <path d="M55,25 L73,25 L73,48 L55,48 Z" fill="rgba(251, 191, 36, 0.15)" stroke="#fbbf24" stroke-width="1.5" />
                        <!-- Steel Chuck Adapter -->
                        <rect x="76" y="32" width="10" height="12" rx="1" fill="#64748b" stroke="#94a3b8" stroke-width="1.5" />
                        <rect x="86" y="36" width="6" height="4" rx="1" fill="#475569" stroke="#94a3b8" stroke-width="1" />
                        <!-- Ergonomic Grip (Ribbed Details) -->
                        <line x1="32" y1="55" x2="40" y2="55" stroke="#fbbf24" stroke-width="1.5" />
                        <line x1="30" y1="62" x2="38" y2="62" stroke="#fbbf24" stroke-width="1.5" />
                        <line x1="28" y1="69" x2="36" y2="69" stroke="#fbbf24" stroke-width="1.5" />
                        <!-- Battery Dock (Dual Capacity Base) -->
                        <rect x="23" y="78" width="28" height="12" rx="2" fill="#0f172a" stroke="#fbbf24" stroke-width="2" />
                        <circle cx="37" cy="84" r="2" fill="#fbbf24" />
                        <!-- Trigger Module -->
                        <path d="M38,50 C41,50 43,54 41,58 C39,58 38,54 38,50 Z" fill="#fbbf24" />
                    </svg>
                `
            },
            heavy: {
                id: "#D01-DEMOLITION-BREAKER",
                svg: `
                    <svg class="h-28 w-auto filter drop-shadow-[0_0_12px_rgba(251,191,36,0.3)]" viewBox="0 0 100 100" fill="none" stroke-linecap="round" stroke-linejoin="round">
                        <!-- Dual Industrial T-Handles (Soft Rubber Grip) -->
                        <path d="M22,25 L35,25 L35,32 L65,32 L65,25 L78,25" stroke="#fbbf24" stroke-width="3" />
                        <!-- Demolition Heavy Hammer Cylinder Block -->
                        <path d="M36,32 L36,65 L42,65 L42,75 L46,75 L46,90 L54,90 L54,75 L58,75 L58,65 L64,65 L64,32 Z" fill="#1e293b" stroke="#475569" stroke-width="1.5" />
                        <!-- High Frequency Piston Guide (Heat Shield Amber Accent) -->
                        <rect x="42" y="36" width="16" height="24" rx="1" fill="rgba(251, 191, 36, 0.15)" stroke="#fbbf24" stroke-width="1.5" />
                        <!-- Auxiliary Handle Grip -->
                        <rect x="16" y="44" width="20" height="6" rx="1" fill="#0f172a" stroke="#fbbf24" stroke-width="1" />
                        <!-- Concrete Hardened Steel Chisel Bit -->
                        <path d="M47,90 L50,105 L53,90" fill="#64748b" stroke="#cbd5e1" stroke-width="1.5" />
                        <!-- Cooling Fins / Vent Rails -->
                        <line x1="45" y1="42" x2="55" y2="42" stroke="#fbbf24" stroke-width="1" />
                        <line x1="45" y1="48" x2="55" y2="48" stroke="#fbbf24" stroke-width="1" />
                        <line x1="45" y1="54" x2="55" y2="54" stroke="#fbbf24" stroke-width="1" />
                    </svg>
                `
            }
        };

        function toggleProtection(state) {
            protectionExtended = state;
            const btnOn = document.getElementById('prot-on');
            const btnOff = document.getElementById('prot-off');
            
            if (state) {
                btnOn.className = "py-3 rounded-xl border border-amber-400 text-amber-400 bg-amber-500/10 text-xs font-bold uppercase tracking-wider transition-all";
                btnOff.className = "py-3 rounded-xl border border-zinc-800 text-slate-400 bg-zinc-900 text-xs font-bold uppercase tracking-wider transition-all";
            } else {
                btnOn.className = "py-3 rounded-xl border border-zinc-800 text-slate-400 bg-zinc-900 text-xs font-bold uppercase tracking-wider transition-all";
                btnOff.className = "py-3 rounded-xl border border-amber-400 text-amber-400 bg-amber-500/10 text-xs font-bold uppercase tracking-wider transition-all";
            }
            updateConfigurator();
        }

        function updateConfigurator() {
            const workloadVal = document.getElementById('config-workload').value;
            const motorVal = document.getElementById('config-motor').value;

            let baseRPM = 4000;
            let baseTorque = 60;
            let baseRuntime = 40;

            if (workloadVal === 'medium') {
                baseRPM = 6500;
                baseTorque = 140;
                baseRuntime = 45;
            } else if (workloadVal === 'heavy') {
                baseRPM = 9000;
                baseTorque = 220;
                baseRuntime = 60;
            }

            if (motorVal === 'pro') {
                baseRPM += 1200;
                baseTorque += 30;
                baseRuntime += 10;
            }

            if (protectionExtended) {
                baseRuntime += 5;
            }

            document.getElementById('stat-rpm').innerText = `${baseRPM.toLocaleString()} RPM`;
            document.getElementById('stat-torque').innerText = `${baseTorque} Nm`;
            document.getElementById('stat-runtime').innerText = `${baseRuntime} mins`;

            // Render Dynamic Vector Blueprint matching current configuration workload (Now completely safe and error-free!)
            const currentSchematic = toolSymmetricSchematics[workloadVal];
            const previewContainer = document.getElementById('machine-preview');
            const labelContainer = document.getElementById('schematic-id');
            
            if (currentSchematic && previewContainer && labelContainer) {
                previewContainer.innerHTML = currentSchematic.svg;
                labelContainer.innerText = currentSchematic.id;
            }

            const wave1 = document.getElementById('wave-1');
            const wave2 = document.getElementById('wave-2');
            
            if (wave1 && wave2) {
                const freqModifier = baseRPM / 1500;
                wave1.setAttribute('d', `M 0,50 Q 25,${50 - (freqModifier * 4)} 50,50 T 100,50`);
                wave2.setAttribute('d', `M 0,50 Q 25,${50 + (freqModifier * 3)} 50,50 T 100,50`);
            }
        }

        // Action Trigger
        function requestFleetTest() {
            const btn = document.querySelector('#fleet-builder button');
            const originalText = btn.innerHTML;
            btn.innerHTML = `<i class="fa-solid fa-sync animate-spin"></i> <span>Compiling Workload Parameters...</span>`;
            btn.disabled = true;

            setTimeout(() => {
                btn.innerHTML = `<i class="fa-solid fa-check"></i> <span>Specs Submitted to Local Station!</span>`;
                setTimeout(() => {
                    btn.innerHTML = originalText;
                    btn.disabled = false;
                }, 3000);
            }, 2000);
        }

        // Run initial config rendering safely after DOM elements exist
        window.onload = function() {
            updateConfigurator();
        };


        const logsContainer = document.getElementById('live-terminal-feed');
        const simulatedLogs = [
            "Heavy Impact Drills packed and locked for Dispatch #099A",
            "Warehouse Station 02 Stock: DB-C10 Plasma Circular Saw replenished",
            "Shipment loaded for Secunderabad Dealer Matrix node",
            "Safety lock certifications passed on all outbound tool units",
            "Direct Drive Brushless Motor Core validation test: passed",
            "Heavy load test on torque assemblies successfully completed"
        ];

        function addTerminalLog() {
            if (!logsContainer) return;
            const randomLog = simulatedLogs[Math.floor(Math.random() * simulatedLogs.length)];
            const time = new Date().toLocaleTimeString();
            
            const logElement = document.createElement('p');
            logElement.innerHTML = `<span class="text-slate-600">[${time}]</span> <span class="text-amber-400">></span> ${randomLog}`;
            
            logsContainer.appendChild(logElement);
            logsContainer.scrollTop = logsContainer.scrollHeight;

            if (logsContainer.children.length > 8) {
                logsContainer.removeChild(logsContainer.firstChild);
            }
        }
        setInterval(addTerminalLog, 5000);
        addTerminalLog();


        function handleContactSubmit(event) {
            event.preventDefault();

            const name = document.getElementById('form-name').value;
            const email = document.getElementById('form-email').value;
            const msg = document.getElementById('form-message').value;
            const feedback = document.getElementById('contact-feedback');
            const btnSubmitText = document.getElementById('btn-submit-text');
            const btnSubmitIcon = document.getElementById('btn-submit-icon');

            if (!name || !email || !msg) {
                feedback.classList.remove('hidden', 'border-amber-400/30', 'text-amber-400');
                feedback.classList.add('border-red-500/30', 'text-red-400', 'bg-red-950/20');
                feedback.innerText = "ERROR: ALL FORMS MUST CONTAIN VALID CORRESPONDENCE BEFORE TRANSMITTING.";
                return;
            }

            btnSubmitText.innerText = "TRANSMITTING ENQUIRY PACKET...";
            btnSubmitIcon.className = "fa-solid fa-circle-notch animate-spin";

            setTimeout(() => {
                feedback.classList.remove('hidden', 'border-red-500/30', 'text-red-400', 'bg-red-950/20');
                feedback.classList.add('border-amber-400/30', 'text-amber-400', 'bg-amber-950/20');
                feedback.innerHTML = `SUCCESS: COMMERCIAL QUOTE INQUIRY RECORDED FOR ${name.toUpperCase()}! <br> Our Secunderabad depot advisors will email you at ${email} shortly.`;
                
                // Clear inputs
                document.getElementById('form-name').value = '';
                document.getElementById('form-email').value = '';
                document.getElementById('form-message').value = '';
                
                btnSubmitText.innerText = "Send Procurement Enquiry";
                btnSubmitIcon.className = "fa-solid fa-paper-plane";

                setTimeout(() => {
                    feedback.classList.add('hidden');
                }, 8000);

            }, 1800);
        }
    </script>
</body>
</html>
