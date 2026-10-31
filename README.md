<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jasmin Babariya | Data Scientist & Enterprise AI Engineer</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    .glow-cyan { text-shadow: 0 0 20px rgba(6, 182, 212, 0.5); }
    .glass {
      background: rgba(17, 24, 39, 0.7);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(255, 255, 255, 0.08);
    }
  </style>
</head>
<body class="bg-gray-950 text-gray-100 font-sans antialiased selection:bg-cyan-500 selection:text-black">

  <!-- Navbar -->
  <nav class="fixed top-0 w-full z-50 glass border-b border-gray-800">
    <div class="max-w-6xl mx-auto px-6 h-16 flex items-center justify-between">
      <span class="text-xl font-bold tracking-tight text-white flex items-center gap-2">
        <span class="text-cyan-400">&lt;</span>Jasmin Babariya<span class="text-cyan-400">/&gt;</span>
      </span>
      <div class="space-x-8 text-sm font-medium text-gray-300">
        <a href="#about" class="hover:text-cyan-400 transition">About</a>
        <a href="#projects" class="hover:text-cyan-400 transition">Projects</a>
        <a href="#skills" class="hover:text-cyan-400 transition">Skills</a>
        <a href="#contact" class="px-4 py-2 bg-cyan-500 text-black font-semibold rounded-lg hover:bg-cyan-400 transition">Contact</a>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <section class="min-h-screen flex items-center justify-center pt-20 px-6">
    <div class="max-w-4xl text-center space-y-6">
      <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full text-xs font-semibold bg-cyan-500/10 text-cyan-400 border border-cyan-500/20">
        <span class="w-2 h-2 rounded-full bg-cyan-400 animate-pulse"></span> Available for AI & Data Science Roles
      </div>
      <h1 class="text-5xl md:text-7xl font-extrabold tracking-tight text-white leading-tight">
        Building Intelligent, <br>
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500 glow-cyan">Deterministic AI Systems</span>
      </h1>
      <p class="text-lg md:text-xl text-gray-400 max-w-2xl mx-auto">
        Data Scientist & Machine Learning Engineer specializing in Agentic Workflows, Enterprise Governance, and Predictive Modeling for industrial applications.
      </p>
      <div class="flex justify-center gap-4 pt-4">
        <a href="#projects" class="px-6 py-3 bg-cyan-500 text-black font-semibold rounded-lg hover:bg-cyan-400 transition shadow-lg shadow-cyan-500/20">
          View Flagship Work
        </a>
        <a href="https://github.com/Jasminbabariya48" target="_blank" class="px-6 py-3 glass rounded-lg hover:bg-gray-800 transition flex items-center gap-2">
          <i class="fab fa-github"></i> GitHub Profile
        </a>
      </div>
    </div>
  </section>

  <!-- Key Metrics / Stats -->
  <section class="max-w-6xl mx-auto px-6 py-12">
    <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
      <div class="glass p-6 rounded-2xl text-center">
        <div class="text-3xl font-extrabold text-cyan-400">180+</div>
        <div class="text-xs text-gray-400 uppercase tracking-wider mt-1">Passing Unit & E2E Tests</div>
      </div>
      <div class="glass p-6 rounded-2xl text-center">
        <div class="text-3xl font-extrabold text-blue-400">100%</div>
        <div class="text-xs text-gray-400 uppercase tracking-wider mt-1">RBAC Security Defense</div>
      </div>
      <div class="glass p-6 rounded-2xl text-center">
        <div class="text-3xl font-extrabold text-teal-400">&lt; 48h</div>
        <div class="text-xs text-gray-400 uppercase tracking-wider mt-1">Risk Triage Cycle Time</div>
      </div>
      <div class="glass p-6 rounded-2xl text-center">
        <div class="text-3xl font-extrabold text-indigo-400">90+</div>
        <div class="text-xs text-gray-400 uppercase tracking-wider mt-1">Benchmark Eval Vectors</div>
      </div>
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projects" class="max-w-6xl mx-auto px-6 py-20">
    <div class="mb-12">
      <h2 class="text-3xl font-bold text-white">Flagship Projects</h2>
      <p class="text-gray-400 mt-2">Enterprise-grade AI solutions and predictive modeling systems.</p>
    </div>
    
    <div class="grid md:grid-cols-2 gap-8">
      <!-- Project 1 -->
      <div class="glass p-8 rounded-2xl hover:border-cyan-500/40 transition flex flex-col justify-between">
        <div>
          <div class="flex items-center justify-between mb-4">
            <span class="text-xs font-semibold px-2.5 py-1 rounded bg-cyan-500/10 text-cyan-400 border border-cyan-500/20">Enterprise AI</span>
            <a href="https://github.com/Jasminbabariya48/Enterprise-Risk-Management-ERM-Platform" class="text-gray-400 hover:text-white"><i class="fas fa-external-link-alt"></i></a>
          </div>
          <h3 class="text-xl font-bold text-white mb-2">Enterprise Risk Management (ERM) Platform</h3>
          <p class="text-sm text-gray-400 leading-relaxed">
            Industrial plant risk intelligence platform featuring an autonomous AI Copilot, 5x5 dynamic risk scoring matrix, multi-stage Maker-Checker approvals, and state machine checkpoint recovery.
          </p>
        </div>
        <div class="flex flex-wrap gap-2 mt-6 pt-6 border-t border-gray-800 text-xs text-cyan-300 font-mono">
          <span>FastAPI</span> • <span>PostgreSQL</span> • <span>LangGraph</span> • <span>Groq</span> • <span>Pytest</span>
        </div>
      </div>

      <!-- Project 2 -->
      <div class="glass p-8 rounded-2xl hover:border-cyan-500/40 transition flex flex-col justify-between">
        <div>
          <div class="flex items-center justify-between mb-4">
            <span class="text-xs font-semibold px-2.5 py-1 rounded bg-emerald-500/10 text-emerald-400 border border-emerald-500/20">Machine Learning</span>
            <a href="https://github.com/Jasminbabariya48/cotton-yield-prediction-gujarat" class="text-gray-400 hover:text-white"><i class="fas fa-external-link-alt"></i></a>
          </div>
          <h3 class="text-xl font-bold text-white mb-2">Predictive Agricultural Yield Model</h3>
          <p class="text-sm text-gray-400 leading-relaxed">
            Supervised machine learning framework forecasting crop yields across Gujarat districts using weather telemetry, rainfall data, and soil nutrient indicators.
          </p>
        </div>
        <div class="flex flex-wrap gap-2 mt-6 pt-6 border-t border-gray-800 text-xs text-emerald-300 font-mono">
          <span>Python</span> • <span>Scikit-Learn</span> • <span>Pandas</span> • <span>Regression</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="glass border-t border-gray-800 py-8 text-center text-sm text-gray-500">
    <p>© 2026 Jasmin Babariya • Built with Tailwind CSS & Hosted on GitHub Pages</p>
  </footer>

</body>
</html>
