
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>Jasmin Babariya | AI Engineer & Data Scientist</title>

  <meta name="description" content="Jasmin Babariya - AI Engineer and Data Scientist specializing in Machine Learning, Generative AI, LLMs, RAG, and intelligent applications." />

  <meta name="theme-color" content="#080b12" />

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet" />

  <!-- Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css" />

  <style>
    :root {
      --bg: #080b12;
      --surface: #101620;
      --border: rgba(255,255,255,0.09);
      --text: #f1f5f9;
      --muted: #94a3b8;
      --accent: #67e8f9;
      --accent2: #818cf8;
    }

    * {
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      overflow-x: hidden;
    }

    h1, h2, h3, .brand {
      font-family: 'Space Grotesk', sans-serif;
    }

    /* Background effects */
    .ambient {
      position: fixed;
      inset: 0;
      z-index: -2;
      pointer-events: none;
      overflow: hidden;
    }

    .ambient::before {
      content: "";
      position: absolute;
      width: 650px;
      height: 650px;
      top: -250px;
      left: -200px;
      background: radial-gradient(circle, rgba(34,211,238,0.12), transparent 70%);
      filter: blur(35px);
    }

    .ambient::after {
      content: "";
      position: absolute;
      width: 700px;
      height: 700px;
      bottom: -350px;
      right: -200px;
      background: radial-gradient(circle, rgba(99,102,241,0.13), transparent 70%);
      filter: blur(35px);
    }

    .grid-bg {
      position: fixed;
      inset: 0;
      z-index: -1;
      pointer-events: none;
      opacity: 0.17;
      background-image:
        linear-gradient(rgba(148,163,184,0.08) 1px, transparent 1px),
        linear-gradient(90deg, rgba(148,163,184,0.08) 1px, transparent 1px);
      background-size: 65px 65px;
      mask-image: linear-gradient(to bottom, black, transparent 85%);
    }

    /* Glass surfaces */
    .glass {
      background: rgba(15, 23, 36, 0.72);
      border: 1px solid var(--border);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
    }

    /* Gradient text */
    .gradient-text {
      background: linear-gradient(110deg, #67e8f9 10%, #818cf8 55%, #c084fc 100%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    /* Gradient border */
    .gradient-border {
      position: relative;
      background: rgba(13, 18, 30, 0.92);
      border: 1px solid transparent;
      background-clip: padding-box;
    }

    .gradient-border::before {
      content: "";
      position: absolute;
      inset: -1px;
      z-index: -1;
      border-radius: inherit;
      background: linear-gradient(135deg, rgba(103,232,249,0.45), rgba(129,140,248,0.15), rgba(192,132,252,0.4));
    }

    /* Buttons */
    .btn-primary {
      background: linear-gradient(110deg, #67e8f9, #818cf8);
      color: #080b12;
      transition: all 0.3s ease;
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 35px rgba(103,232,249,0.2);
    }

    .btn-secondary {
      border: 1px solid rgba(255,255,255,0.13);
      background: rgba(255,255,255,0.03);
      transition: all 0.3s ease;
    }

    .btn-secondary:hover {
      border-color: rgba(103,232,249,0.5);
      background: rgba(103,232,249,0.06);
      transform: translateY(-3px);
    }

    /* Project cards */
    .project-card {
      transition: transform 0.35s ease, border-color 0.35s ease, box-shadow 0.35s ease;
    }

    .project-card:hover {
      transform: translateY(-7px);
      border-color: rgba(103,232,249,0.35);
      box-shadow: 0 20px 60px rgba(0,0,0,0.25);
    }

    .project-icon {
      transition: transform 0.35s ease;
    }

    .project-card:hover .project-icon {
      transform: scale(1.08) rotate(-3deg);
    }

    /* Reveal animation */
    .reveal {
      opacity: 0;
      transform: translateY(25px);
      transition: opacity 0.7s ease, transform 0.7s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* Navbar */
    .nav-link {
      position: relative;
      transition: color 0.2s ease;
    }

    .nav-link::after {
      content: "";
      position: absolute;
      bottom: -7px;
      left: 0;
      width: 0;
      height: 2px;
      background: var(--accent);
      transition: width 0.25s ease;
    }

    .nav-link:hover {
      color: white;
    }

    .nav-link:hover::after {
      width: 100%;
    }

    /* Floating animation */
    .float {
      animation: floating 6s ease-in-out infinite;
    }

    @keyframes floating {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    /* Status indicator */
    .status-dot {
      box-shadow: 0 0 12px rgba(74,222,128,0.65);
    }

    /* Timeline */
    .timeline-line {
      background: linear-gradient(to bottom, #67e8f9, #818cf8, transparent);
    }

    /* Scrollbar */
    ::-webkit-scrollbar {
      width: 7px;
    }

    ::-webkit-scrollbar-track {
      background: #080b12;
    }

    ::-webkit-scrollbar-thumb {
      background: #263244;
      border-radius: 10px;
    }

    ::-webkit-scrollbar-thumb:hover {
      background: #67e8f9;
    }

    /* Selection */
    ::selection {
      background: rgba(103,232,249,0.25);
      color: white;
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
        scroll-behavior: auto !important;
      }

      .reveal {
        opacity: 1;
        transform: none;
      }
    }
  </style>
</head>

<body class="antialiased">

  <!-- Background -->
  <div class="ambient"></div>
  <div class="grid-bg"></div>

  <!-- ================= NAVBAR ================= -->
  <nav class="fixed top-0 w-full z-50 glass border-b border-white/5">
    <div class="max-w-7xl mx-auto px-6 lg:px-10 h-[76px] flex items-center justify-between">

      <a href="#home" class="brand text-lg sm:text-xl font-bold tracking-tight">
        <span class="text-cyan-400">&lt;</span>jasmin<span class="gradient-text">.ai</span><span class="text-cyan-400">/&gt;</span>
      </a>

      <!-- Desktop menu -->
      <div class="hidden md:flex items-center gap-8 text-sm text-gray-400 font-medium">
        <a href="#about" class="nav-link">About</a>
        <a href="#experience" class="nav-link">Experience</a>
        <a href="#projects" class="nav-link">Projects</a>
        <a href="#skills" class="nav-link">Skills</a>
        <a href="#contact" class="btn-primary px-5 py-2.5 rounded-lg font-semibold">
          Let's Connect <i class="fa-solid fa-arrow-up-right-from-square ml-1 text-xs"></i>
        </a>
      </div>

      <!-- Mobile menu button -->
      <button id="menu-btn" class="md:hidden text-gray-300 text-xl p-2" aria-label="Open navigation menu" aria-expanded="false">
        <i class="fa-solid fa-bars"></i>
      </button>
    </div>

    <!-- Mobile menu -->
    <div id="mobile-menu" class="hidden md:hidden glass border-t border-white/5 px-6 py-5">
      <div class="flex flex-col gap-5 text-sm text-gray-300">
        <a href="#about" class="mobile-link">About</a>
        <a href="#experience" class="mobile-link">Experience</a>
        <a href="#projects" class="mobile-link">Projects</a>
        <a href="#skills" class="mobile-link">Skills</a>
        <a href="#contact" class="mobile-link text-cyan-400">Let's Connect ↗</a>
      </div>
    </div>
  </nav>


  <!-- ================= HERO ================= -->
  <section id="home" class="min-h-screen flex items-center pt-28 pb-20 px-6">
    <div class="max-w-7xl mx-auto w-full grid lg:grid-cols-[1.3fr_0.7fr] gap-16 items-center">

      <!-- Hero content -->
      <div class="reveal">

        <div class="inline-flex items-center gap-2.5 px-3.5 py-2 rounded-full border border-emerald-400/20 bg-emerald-400/5 text-emerald-300 text-xs font-medium mb-8">
          <span class="w-2 h-2 rounded-full bg-emerald-400 status-dot"></span>
          Open to AI / ML Opportunities
        </div>

        <p class="text-sm text-gray-400 font-medium tracking-wide mb-4">
          HELLO, I'M JASMIN BABARIYA
        </p>

        <h1 class="text-5xl sm:text-6xl lg:text-[76px] font-bold leading-[1.08] tracking-tight mb-7">
          Turning Ideas Into
          <span class="gradient-text block mt-2">Intelligent Systems.</span>
        </h1>

        <p class="text-gray-400 text-base sm:text-lg leading-8 max-w-2xl">
          Data Scientist & AI Engineer building practical solutions with
          Machine Learning, Generative AI, LLMs, and intelligent automation.
          I enjoy turning complex problems into scalable, impactful products.
        </p>

        <!-- CTA buttons -->
        <div class="flex flex-wrap gap-4 mt-9">
          <a href="#projects" class="btn-primary px-6 py-3.5 rounded-xl text-sm font-bold">
            Explore My Work <i class="fa-solid fa-arrow-right ml-2"></i>
          </a>

          <a href="https://github.com/Jasminbabariya48" target="_blank" rel="noopener noreferrer" class="btn-secondary px-6 py-3.5 rounded-xl text-sm font-semibold text-gray-200">
            <i class="fa-brands fa-github mr-2"></i> GitHub
          </a>

          <a href="https://www.linkedin.com/" target="_blank" rel="noopener noreferrer" class="btn-secondary px-6 py-3.5 rounded-xl text-sm font-semibold text-gray-200">
            <i class="fa-brands fa-linkedin mr-2"></i> LinkedIn
          </a>
        </div>

        <!-- Social links -->
        <div class="flex items-center gap-5 mt-10 text-gray-500 text-sm">
          <span>Connect with me</span>
          <span class="h-px w-10 bg-gray-700"></span>
          <a href="https://github.com/Jasminbabariya48" target="_blank" rel="noopener noreferrer" aria-label="GitHub" class="hover:text-cyan-400 transition text-lg">
            <i class="fa-brands fa-github"></i>
          </a>
          <a href="https://www.linkedin.com/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn" class="hover:text-cyan-400 transition text-lg">
            <i class="fa-brands fa-linkedin"></i>
          </a>
          <a href="mailto:jasminbabariya04@gmail.com" aria-label="Email" class="hover:text-cyan-400 transition text-lg">
            <i class="fa-regular fa-envelope"></i>
          </a>
        </div>
      </div>

      <!-- Hero visual -->
      <div class="hidden lg:flex justify-center items-center reveal">
        <div class="relative float">

          <div class="absolute inset-0 bg-cyan-400/10 blur-[90px] rounded-full"></div>

          <div class="relative gradient-border rounded-[32px] p-8 w-[360px]">

            <div class="flex items-center gap-3 mb-8">
              <div class="w-3 h-3 rounded-full bg-red-400"></div>
              <div class="w-3 h-3 rounded-full bg-yellow-400"></div>
              <div class="w-3 h-3 rounded-full bg-green-400"></div>
              <span class="ml-auto text-xs text-gray-500 font-mono">ai_engineer.py</span>
            </div>

            <div class="font-mono text-sm leading-8">
              <p class="text-gray-500"># Building the future</p>
              <p><span class="text-purple-400">class</span> <span class="text-cyan-300">AIEngineer</span>:</p>
              <p class="pl-5 text-purple-400">def <span class="text-yellow-300">__init__</span>(self):</p>
              <p class="pl-10">self.name = <span class="text-emerald-300">"Jasmin"</span></p>
              <p class="pl-10">self.focus = [</p>
              <p class="pl-14 text-emerald-300">"Machine Learning",</p>
              <p class="pl-14 text-emerald-300">"Generative AI",</p>
              <p class="pl-14 text-emerald-300">"LLMs & RAG",</p>
              <p class="pl-14 text-emerald-300">"AI Agents"</p>
              <p class="pl-10">]</p>
              <p class="pl-5 mt-3 text-purple-400">def <span class="text-yellow-300">build</span>(self):</p>
              <p class="pl-10 text-gray-400">return <span class="text-cyan-300">"Something amazing"</span></p>
            </div>

            <div class="mt-8 pt-5 border-t border-white/10 flex items-center justify-between">
              <span class="text-xs text-gray-500">Always learning. Always building.</span>
              <i class="fa-solid fa-code text-cyan-400"></i>
            </div>
          </div>

          <!-- Floating badge -->
          <div class="absolute -bottom-5 -left-10 glass rounded-xl px-4 py-3 flex items-center gap-3 shadow-xl">
            <div class="w-9 h-9 rounded-lg bg-purple-400/10 flex items-center justify-center">
              <i class="fa-solid fa-brain text-purple-300"></i>
            </div>
            <div>
              <p class="text-xs text-gray-400">Specialization</p>
              <p class="text-sm font-semibold text-white">Applied AI & GenAI</p>
            </div>
          </div>

        </div>
      </div>

    </div>
  </section>


  <!-- ================= TECH HIGHLIGHTS ================= -->
  <section class="max-w-7xl mx-auto px-6 lg:px-10 pb-20">
    <div class="reveal grid grid-cols-2 md:grid-cols-4 gap-4">

      <div class="glass rounded-2xl p-5 sm:p-7">
        <i class="fa-solid fa-brain text-cyan-400 text-xl mb-4"></i>
        <h3 class="text-2xl font-bold text-white">AI / ML</h3>
        <p class="text-xs text-gray-500 mt-2">Intelligent modeling</p>
      </div>

      <div class="glass rounded-2xl p-5 sm:p-7">
        <i class="fa-solid fa-wand-magic-sparkles text-purple-400 text-xl mb-4"></i>
        <h3 class="text-2xl font-bold text-white">GenAI</h3>
        <p class="text-xs text-gray-500 mt-2">LLMs & RAG systems</p>
      </div>

      <div class="glass rounded-2xl p-5 sm:p-7">
        <i class="fa-solid fa-code text-blue-400 text-xl mb-4"></i>
        <h3 class="text-2xl font-bold text-white">Python</h3>
        <p class="text-xs text-gray-500 mt-2">Development & deployment</p>
      </div>

      <div class="glass rounded-2xl p-5 sm:p-7">
        <i class="fa-solid fa-gears text-emerald-400 text-xl mb-4"></i>
        <h3 class="text-2xl font-bold text-white">AI Agents</h3>
        <p class="text-xs text-gray-500 mt-2">Workflows & automation</p>
      </div>

    </div>
  </section>


  <!-- ================= ABOUT ================= -->
  <section id="about" class="py-24 px-6 lg:px-10 border-t border-white/5">
    <div class="max-w-7xl mx-auto">

      <div class="reveal mb-14">
        <p class="text-cyan-400 text-xs font-bold tracking-[0.2em] uppercase mb-3">Get to know me</p>
        <h2 class="text-4xl sm:text-5xl font-bold tracking-tight">
          About <span class="gradient-text">Me.</span>
        </h2>
      </div>

      <div class="grid md:grid-cols-2 gap-12 lg:gap-20 items-start">

        <div class="reveal">
          <p class="text-gray-400 leading-8 text-base">
            I'm a Data Scientist and AI Engineer passionate about building
            intelligent applications that solve real-world problems.
            My work spans Machine Learning, Deep Learning, NLP,
            and Generative AI.
          </p>

          <p class="text-gray-400 leading-8 text-base mt-5">
            I have hands-on experience developing end-to-end ML pipelines,
            building LLM-powered applications, implementing Retrieval-Augmented
            Generation (RAG), and deploying models through APIs.
            I enjoy experimenting with emerging technologies and turning
            ideas into useful, production-oriented solutions.
          </p>

          <p class="text-gray-400 leading-8 text-base mt-5">
            My goal is to continuously grow as an AI professional while
            creating impactful products at the intersection of data,
            intelligence, and engineering.
          </p>
        </div>

        <div class="reveal grid grid-cols-1 sm:grid-cols-2 gap-4">

          <div class="glass rounded-2xl p-6">
            <i class="fa-solid fa-graduation-cap text-cyan-400 text-xl mb-4"></i>
            <h3 class="font-semibold text-white mb-2">Education</h3>
            <p class="text-sm text-gray-400 leading-6">
              Master's in Data Analytics<br />
              DAIICT
            </p>
          </div>

          <div class="glass rounded-2xl p-6">
            <i class="fa-solid fa-lightbulb text-purple-400 text-xl mb-4"></i>
            <h3 class="font-semibold text-white mb-2">What I enjoy</h3>
            <p class="text-sm text-gray-400 leading-6">
              Problem solving, research, building AI products, and continuous learning.
            </p>
          </div>

          <div class="glass rounded-2xl p-6 sm:col-span-2">
            <i class="fa-solid fa-rocket text-emerald-400 text-xl mb-4"></i>
            <h3 class="font-semibold text-white mb-2">Current Focus</h3>
            <p class="text-sm text-gray-400 leading-6">
              Agentic AI, LLM applications, RAG architectures, model evaluation,
              backend development, and production-ready AI systems.
            </p>
          </div>

        </div>
      </div>

    </div>
  </section>


  <!-- ================= EXPERIENCE ================= -->
  <section id="experience" class="py-24 px-6 lg:px-10 border-t border-white/5">
    <div class="max-w-7xl mx-auto">

      <div class="reveal mb-14">
        <p class="text-cyan-400 text-xs font-bold tracking-[0.2em] uppercase mb-3">My professional journey</p>
        <h2 class="text-4xl sm:text-5xl font-bold tracking-tight">
          Experience<span class="gradient-text">.</span>
        </h2>
      </div>

      <div class="max-w-3xl">

        <!-- Experience 1 -->
        <div class="reveal relative pl-8 pb-12 border-l border-gray-800">

          <div class="absolute -left-[5px] top-1 w-[9px] h-[9px] rounded-full bg-cyan-400 ring-4 ring-cyan-400/10"></div>

          <div class="glass rounded-2xl p-6 sm:p-8">
            <div class="flex flex-wrap items-center justify-between gap-3 mb-4">
              <span class="text-xs font-semibold text-cyan-300 bg-cyan-400/10 border border-cyan-400/20 px-3 py-1 rounded-full">
                Full-time
              </span>
              <span class="text-xs text-gray-500">May 2024 – Present</span>
            </div>

            <h3 class="text-xl font-bold text-white">Junior Data Scientist</h3>
            <p class="text-sm text-gray-400 mt-1">Semantic Technologies · Pune, India</p>

            <ul class="mt-5 space-y-3 text-sm text-gray-400 leading-6 list-disc pl-5">
              <li>Developed and optimized Machine Learning and Deep Learning models for classification, prediction, and intelligent data analysis.</li>
              <li>Built end-to-end data processing and model development pipelines using Python, Pandas, Scikit-learn, and TensorFlow.</li>
              <li>Developed and integrated REST APIs using FastAPI and Flask to deploy ML solutions.</li>
              <li>Worked on NLP, model experimentation, evaluation, and AI-driven research initiatives.</li>
              <li>Collaborated with cross-functional teams to translate business requirements into technical solutions.</li>
            </ul>

            <div class="flex flex-wrap gap-2 mt-6">
              <span class="text-xs px-2.5 py-1 rounded-md bg-white/5 text-gray-400">Python</span>
              <span class="text-xs px-2.5 py-1 rounded-md bg-white/5 text-gray-400">Machine Learning</span>
              <span class="text-xs px-2.5 py-1 rounded-md bg-white/5 text-gray-400">Deep Learning</span>
              <span class="text-xs px-2.5 py-1 rounded-md bg-white/5 text-gray-400">FastAPI</span>
              <span class="text-xs px-2.5 py-1 rounded-md bg-white/5 text-gray-400">NLP</span>
            </div>
          </div>
        </div>

        <!-- Experience 2 -->
        <div class="reveal relative pl-8 pb-4 border-l border-gray-800">

          <div class="absolute -left-[5px] top-1 w-[9px] h-[9px] rounded-full bg-purple-400 ring-4 ring-purple-400/10"></div>

          <div class="glass rounded-2xl p-6 sm:p-8">
            <div class="flex flex-wrap items-center justify-between gap-3 mb-4">
              <span class="text-xs font-semibold text-purple-300 bg-purple-400/10 border border-purple-400/20 px-3 py-1 rounded-full">
                Internship
              </span>
              <span class="text-xs text-gray-500">Mar 2024 – Apr 2024</span>
            </div>

            <h3 class="text-xl font-bold text-white">Data Analyst Intern</h3>
            <p class="text-sm text-gray-400 mt-1">Unified Mentor & Tech · Remote</p>

            <ul class="mt-5 space-y-3 text-sm text-gray-400 leading-6 list-disc pl-5">
              <li>Performed exploratory data analysis and statistical analysis to identify patterns and actionable insights.</li>
              <li>Applied NLP techniques to extract topics and meaningful insights from textual data.</li>
              <li>Created visualizations and analytical dashboards to communicate results and support data-driven decisions.</li>
            </ul>

            <div class="flex flex-wrap gap-2 mt-6">
              <span class="text-xs px-2.5 py-1 rounded-md bg-white/5 text-gray-400">Python</span>
              <span class="text-xs px-2.5 py-1 rounded-md bg-white/5 text-gray-400">NLP</span>
              <span class="text-xs px-2.5 py-1 rounded-md bg-white/5 text-gray-400">Power BI</span>
              <span class="text-xs px-2.5 py-1 rounded-md bg-white/5 text-gray-400">EDA</span>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>


  <!-- ================= PROJECTS ================= -->
  <section id="projects" class="py-24 px-6 lg:px-10 border-t border-white/5">
    <div class="max-w-7xl mx-auto">

      <div class="reveal mb-14 flex flex-wrap justify-between items-end gap-5">
        <div>
          <p class="text-cyan-400 text-xs font-bold tracking-[0.2em] uppercase mb-3">Things I've built</p>
          <h2 class="text-4xl sm:text-5xl font-bold tracking-tight">
            Featured <span class="gradient-text">Projects.</span>
          </h2>
        </div>

        <a href="https://github.com/Jasminbabariya48" target="_blank" rel="noopener noreferrer" class="text-sm text-gray-400 hover:text-cyan-400 transition">
          Explore all repositories <i class="fa-solid fa-arrow-up-right-from-square ml-1"></i>
        </a>
      </div>


      <div class="grid md:grid-cols-2 xl:grid-cols-3 gap-6">

        <!-- Project 1 -->
        <article class="project-card glass rounded-2xl p-7 flex flex-col reveal">
          <div class="flex items-center justify-between mb-6">
            <div class="project-icon w-12 h-12 rounded-xl bg-cyan-400/10 flex items-center justify-center">
              <i class="fa-solid fa-shield-halved text-cyan-300 text-xl"></i>
            </div>
            <a href="https://github.com/Jasminbabariya48/Enterprise-Risk-Management-ERM-Platform" target="_blank" rel="noopener noreferrer" aria-label="View ERM project on GitHub" class="text-gray-500 hover:text-white transition">
              <i class="fa-brands fa-github text-xl"></i>
            </a>
          </div>

          <span class="text-xs text-cyan-300 font-semibold mb-3">GENERATIVE AI · ENTERPRISE</span>

          <h3 class="text-lg font-bold text-white mb-3">
            Enterprise Risk Management Platform
          </h3>

          <p class="text-sm text-gray-400 leading-7 flex-grow">
            An intelligent enterprise risk management platform featuring an AI Copilot,
            dynamic risk scoring, Maker-Checker approval workflows, and checkpoint-based
            state recovery.
          </p>

          <div class="flex flex-wrap gap-2 mt-6 pt-5 border-t border-white/5">
            <span class="tech-tag">FastAPI</span>
            <span class="tech-tag">LangGraph</span>
            <span class="tech-tag">Groq</span>
            <span class="tech-tag">PostgreSQL</span>
          </div>
        </article>


        <!-- Project 2 -->
        <article class="project-card glass rounded-2xl p-7 flex flex-col reveal">
          <div class="flex items-center justify-between mb-6">
            <div class="project-icon w-12 h-12 rounded-xl bg-emerald-400/10 flex items-center justify-center">
              <i class="fa-solid fa-chart-line text-emerald-300 text-xl"></i>
            </div>
            <a href="https://github.com/Jasminbabariya48/cotton-yield-prediction-gujarat" target="_blank" rel="noopener noreferrer" aria-label="View yield prediction project on GitHub" class="text-gray-500 hover:text-white transition">
              <i class="fa-brands fa-github text-xl"></i>
            </a>
          </div>

          <span class="text-xs text-emerald-300 font-semibold mb-3">MACHINE LEARNING</span>

          <h3 class="text-lg font-bold text-white mb-3">
            Cotton Yield Prediction
          </h3>

          <p class="text-sm text-gray-400 leading-7 flex-grow">
            A predictive ML application for estimating cotton yield using historical
            agricultural data, weather parameters, rainfall, and soil-related
            features.
          </p>

          <div class="flex flex-wrap gap-2 mt-6 pt-5 border-t border-white/5">
            <span class="tech-tag">Python</span>
            <span class="tech-tag">Scikit-learn</span>
            <span class="tech-tag">Pandas</span>
            <span class="tech-tag">Regression</span>
          </div>
        </article>


        <!-- Project 3 -->
        <article class="project-card glass rounded-2xl p-7 flex flex-col reveal">
          <div class="flex items-center justify-between mb-6">
            <div class="project-icon w-12 h-12 rounded-xl bg-purple-400/10 flex items-center justify-center">
              <i class="fa-solid fa-book-open text-purple-300 text-xl"></i>
            </div>
            <a href="https://github.com/Jasminbabariya48" target="_blank" rel="noopener noreferrer" aria-label="View repositories on GitHub" class="text-gray-500 hover:text-white transition">
              <i class="fa-brands fa-github text-xl"></i>
            </a>
          </div>

          <span class="text-xs text-purple-300 font-semibold mb-3">GENERATIVE AI · RAG</span>

          <h3 class="text-lg font-bold text-white mb-3">
            Intelligent Document Q&A
          </h3>

          <p class="text-sm text-gray-400 leading-7 flex-grow">
            A Retrieval-Augmented Generation application that allows users to
            interact with documents and retrieve context-aware answers using
            semantic search and LLMs.
          </p>

          <div class="flex flex-wrap gap-2 mt-6 pt-5 border-t border-white/5">
            <span class="tech-tag">LangChain</span>
            <span class="tech-tag">LLMs</span>
            <span class="tech-tag">Embeddings</span>
            <span class="tech-tag">Streamlit</span>
          </div>
        </article>


        <!-- Project 4 -->
        <article class="project-card glass rounded-2xl p-7 flex flex-col reveal">
          <div class="flex items-center justify-between mb-6">
            <div class="project-icon w-12 h-12 rounded-xl bg-blue-400/10 flex items-center justify-center">
              <i class="fa-solid fa-comments text-blue-300 text-xl"></i>
            </div>
            <a href="https://github.com/Jasminbabariya48" target="_blank" rel="noopener noreferrer" aria-label="View repositories on GitHub" class="text-gray-500 hover:text-white transition">
              <i class="fa-brands fa-github text-xl"></i>
            </a>
          </div>

          <span class="text-xs text-blue-300 font-semibold mb-3">LLM APPLICATION</span>

          <h3 class="text-lg font-bold text-white mb-3">
            SQL & PDF Conversational Assistant
          </h3>

          <p class="text-sm text-gray-400 leading-7 flex-grow">
            A conversational AI application for querying structured databases
            through natural language and answering questions from uploaded
            PDF documents.
          </p>

          <div class="flex flex-wrap gap-2 mt-6 pt-5 border-t border-white/5">
            <span class="tech-tag">Python</span>
            <span class="tech-tag">LangChain</span>
            <span class="tech-tag">MySQL</span>
            <span class="tech-tag">RAG</span>
          </div>
        </article>


        <!-- Project 5 -->
        <article class="project-card glass rounded-2xl p-7 flex flex-col reveal">
          <div class="flex items-center justify-between mb-6">
            <div class="project-icon w-12 h-12 rounded-xl bg-pink-400/10 flex items-center justify-center">
              <i class="fa-solid fa-face-smile text-pink-300 text-xl"></i>
            </div>
            <a href="https://github.com/Jasminbabariya48" target="_blank" rel="noopener noreferrer" aria-label="View repositories on GitHub" class="text-gray-500 hover:text-white transition">
              <i class="fa-brands fa-github text-xl"></i>
            </a>
          </div>

          <span class="text-xs text-pink-300 font-semibold mb-3">DEEP LEARNING · COMPUTER VISION</span>

          <h3 class="text-lg font-bold text-white mb-3">
            Facial Emotion Recognition
          </h3>

          <p class="text-sm text-gray-400 leading-7 flex-grow">
            A deep learning-based computer vision application for facial emotion
            classification, integrated with a real-time webcam interface.
          </p>

          <div class="flex flex-wrap gap-2 mt-6 pt-5 border-t border-white/5">
            <span class="tech-tag">TensorFlow</span>
            <span class="tech-tag">CNN</span>
            <span class="tech-tag">OpenCV</span>
            <span class="tech-tag">DeepFace</span>
          </div>
        </article>


        <!-- Project 6 -->
        <article class="project-card glass rounded-2xl p-7 flex flex-col reveal">
          <div class="flex items-center justify-between mb-6">
            <div class="project-icon w-12 h-12 rounded-xl bg-orange-400/10 flex items-center justify-center">
              <i class="fa-solid fa-flask text-orange-300 text-xl"></i>
            </div>
            <a href="https://github.com/Jasminbabariya48" target="_blank" rel="noopener noreferrer" aria-label="View repositories on GitHub" class="text-gray-500 hover:text-white transition">
              <i class="fa-brands fa-github text-xl"></i>
            </a>
          </div>

          <span class="text-xs text-orange-300 font-semibold mb-3">ML · API DEVELOPMENT</span>

          <h3 class="text-lg font-bold text-white mb-3">
            ML Model Deployment & APIs
          </h3>

          <p class="text-sm text-gray-400 leading-7 flex-grow">
            Deploying machine learning models as REST APIs to enable seamless
            integration with web applications and external services.
          </p>

          <div class="flex flex-wrap gap-2 mt-6 pt-5 border-t border-white/5">
            <span class="tech-tag">FastAPI</span>
            <span class="tech-tag">Flask</span>
            <span class="tech-tag">Python</span>
            <span class="tech-tag">REST APIs</span>
          </div>
        </article>

      </div>
    </div>
  </section>


  <!-- ================= SKILLS ================= -->
  <section id="skills" class="py-24 px-6 lg:px-10 border-t border-white/5">
    <div class="max-w-7xl mx-auto">

      <div class="reveal mb-14">
        <p class="text-cyan-400 text-xs font-bold tracking-[0.2em] uppercase mb-3">My technical toolkit</p>
        <h2 class="text-4xl sm:text-5xl font-bold tracking-tight">
          Skills & <span class="gradient-text">Technologies.</span>
        </h2>
      </div>

      <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-5">

        <!-- AI / GenAI -->
        <div class="reveal glass rounded-2xl p-7">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-xl bg-purple-400/10 flex items-center justify-center">
              <i class="fa-solid fa-wand-magic-sparkles text-purple-300"></i>
            </div>
            <h3 class="font-bold text-white">Generative AI</h3>
          </div>
          <div class="flex flex-wrap gap-2">
            <span class="skill-tag">LLMs</span>
            <span class="skill-tag">RAG</span>
            <span class="skill-tag">LangChain</span>
            <span class="skill-tag">LangGraph</span>
            <span class="skill-tag">AI Agents</span>
            <span class="skill-tag">Prompt Engineering</span>
            <span class="skill-tag">Hugging Face</span>
          </div>
        </div>

        <!-- ML -->
        <div class="reveal glass rounded-2xl p-7">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-xl bg-cyan-400/10 flex items-center justify-center">
              <i class="fa-solid fa-brain text-cyan-300"></i>
            </div>
            <h3 class="font-bold text-white">Machine Learning</h3>
          </div>
          <div class="flex flex-wrap gap-2">
            <span class="skill-tag">Scikit-learn</span>
            <span class="skill-tag">XGBoost</span>
            <span class="skill-tag">CatBoost</span>
            <span class="skill-tag">Regression</span>
            <span class="skill-tag">Classification</span>
            <span class="skill-tag">Feature Engineering</span>
          </div>
        </div>

        <!-- Deep Learning -->
        <div class="reveal glass rounded-2xl p-7">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-xl bg-pink-400/10 flex items-center justify-center">
              <i class="fa-solid fa-network-wired text-pink-300"></i>
            </div>
            <h3 class="font-bold text-white">Deep Learning & NLP</h3>
          </div>
          <div class="flex flex-wrap gap-2">
            <span class="skill-tag">TensorFlow</span>
            <span class="skill-tag">PyTorch</span>
            <span class="skill-tag">Keras</span>
            <span class="skill-tag">CNN</span>
            <span class="skill-tag">Transformers</span>
            <span class="skill-tag">NLP</span>
          </div>
        </div>

        <!-- Programming -->
        <div class="reveal glass rounded-2xl p-7">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-xl bg-blue-400/10 flex items-center justify-center">
              <i class="fa-solid fa-code text-blue-300"></i>
            </div>
            <h3 class="font-bold text-white">Programming & Data</h3>
          </div>
          <div class="flex flex-wrap gap-2">
            <span class="skill-tag">Python</span>
            <span class="skill-tag">SQL</span>
            <span class="skill-tag">Pandas</span>
            <span class="skill-tag">NumPy</span>
            <span class="skill-tag">Statistics</span>
            <span class="skill-tag">EDA</span>
          </div>
        </div>

        <!-- Deployment -->
        <div class="reveal glass rounded-2xl p-7">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-xl bg-emerald-400/10 flex items-center justify-center">
              <i class="fa-solid fa-cloud-arrow-up text-emerald-300"></i>
            </div>
            <h3 class="font-bold text-white">Backend & Deployment</h3>
          </div>
          <div class="flex flex-wrap gap-2">
            <span class="skill-tag">FastAPI</span>
            <span class="skill-tag">Flask</span>
            <span class="skill-tag">Streamlit</span>
            <span class="skill-tag">REST APIs</span>
            <span class="skill-tag">Docker</span>
            <span class="skill-tag">Git</span>
          </div>
        </div>

        <!-- Database / BI -->
        <div class="reveal glass rounded-2xl p-7">
          <div class="flex items-center gap-3 mb-6">
            <div class="w-10 h-10 rounded-xl bg-orange-400/10 flex items-center justify-center">
              <i class="fa-solid fa-database text-orange-300"></i>
            </div>
            <h3 class="font-bold text-white">Database & Visualization</h3>
          </div>
          <div class="flex flex-wrap gap-2">
            <span class="skill-tag">PostgreSQL</span>
            <span class="skill-tag">MySQL</span>
            <span class="skill-tag">Qdrant</span>
            <span class="skill-tag">Power BI</span>
            <span class="skill-tag">Tableau</span>
            <span class="skill-tag">Matplotlib</span>
          </div>
        </div>

      </div>
    </div>
  </section>


  <!-- ================= CONTACT ================= -->
  <section id="contact" class="py-24 px-6 lg:px-10 border-t border-white/5">
    <div class="max-w-5xl mx-auto">

      <div class="reveal gradient-border rounded-3xl p-8 sm:p-14 text-center">

        <div class="inline-flex items-center justify-center w-14 h-14 rounded-2xl bg-cyan-400/10 mb-7">
          <i class="fa-regular fa-paper-plane text-cyan-300 text-xl"></i>
        </div>

        <p class="text-cyan-400 text-xs font-bold tracking-[0.2em] uppercase mb-4">
          Have an interesting opportunity?
        </p>

        <h2 class="text-4xl sm:text-6xl font-bold tracking-tight mb-6">
          Let's Build Something
          <span class="gradient-text">Amazing.</span>
        </h2>

        <p class="text-gray-400 max-w-xl mx-auto leading-7 text-sm sm:text-base">
          I'm always excited to connect with people working on innovative
          AI solutions, meaningful products, and challenging problems.
          Feel free to reach out!
        </p>

        <a href="mailto:jasminbabariya04@gmail.com" class="btn-primary inline-flex items-center gap-3 px-7 py-4 rounded-xl font-bold text-sm mt-9">
          <i class="fa-regular fa-envelope"></i>
          jasminbabariya04@gmail.com
        </a>

        <div class="flex justify-center gap-6 mt-10 text-gray-500 text-xl">
          <a href="https://github.com/Jasminbabariya48" target="_blank" rel="noopener noreferrer" aria-label="GitHub" class="hover:text-cyan-400 transition">
            <i class="fa-brands fa-github"></i>
          </a>
          <a href="https://www.linkedin.com/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn" class="hover:text-cyan-400 transition">
            <i class="fa-brands fa-linkedin"></i>
          </a>
          <a href="mailto:jasminbabariya04@gmail.com" aria-label="Email" class="hover:text-cyan-400 transition">
            <i class="fa-regular fa-envelope"></i>
          </a>
        </div>

      </div>
    </div>
  </section>


  <!-- ================= FOOTER ================= -->
  <footer class="border-t border-white/5 py-7 px-6">
    <div class="max-w-7xl mx-auto flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-gray-500">

      <p>
        © <span id="year"></span> Jasmin Babariya. Crafted with passion & Python mindset.
      </p>

      <a href="#home" class="hover:text-cyan-400 transition">
        Back to top <i class="fa-solid fa-arrow-up ml-1"></i>
      </a>

    </div>
  </footer>


  <!-- ================= JAVASCRIPT ================= -->
  <script>
    // Dynamic copyright year
    document.getElementById("year").textContent = new Date().getFullYear();

    // Mobile navigation
    const menuBtn = document.getElementById("menu-btn");
    const mobileMenu = document.getElementById("mobile-menu");

    menuBtn.addEventListener("click", () => {
      const isOpen = !mobileMenu.classList.contains("hidden");

      mobileMenu.classList.toggle("hidden");
      menuBtn.setAttribute("aria-expanded", String(!isOpen));

      menuBtn.innerHTML = isOpen
        ? '<i class="fa-solid fa-bars"></i>'
        : '<i class="fa-solid fa-xmark"></i>';
    });

    // Close mobile menu after navigation
    document.querySelectorAll(".mobile-link").forEach(link => {
      link.addEventListener("click", () => {
        mobileMenu.classList.add("hidden");
        menuBtn.setAttribute("aria-expanded", "false");
        menuBtn.innerHTML = '<i class="fa-solid fa-bars"></i>';
      });
    });

    // Reveal elements on scroll
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add("visible");
            observer.unobserve(entry.target);
          }
        });
      },
      {
        threshold: 0.12
      }
    );

    document.querySelectorAll(".reveal").forEach(element => {
      observer.observe(element);
    });

    // Add reusable tag styles
    document.querySelectorAll(".tech-tag").forEach(tag => {
      tag.classList.add(
        "text-xs",
        "px-2.5",
        "py-1",
        "rounded-md",
        "bg-white/5",
        "text-gray-400"
      );
    });

    document.querySelectorAll(".skill-tag").forEach(tag => {
      tag.classList.add(
        "text-xs",
        "px-3",
        "py-1.5",
        "rounded-lg",
        "bg-white/5",
        "border",
        "border-white/5",
        "text-gray-400",
        "hover:text-cyan-300",
        "hover:border-cyan-400/20",
        "transition"
      );
    });
  </script>

</body>
</html>
