<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>New York City Roleplay</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Tailwind -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Icons -->
  <script src="https://unpkg.com/lucide@latest"></script>

  <style>
    :root {
      --nyc-blue: #3bb6ff;
      --nyc-blue-dark: #1e90d4;
      --nyc-light: #ffffff;
      --nyc-dark: #000000;
      --nyc-grey: #222222;
    }

    body {
      scroll-behavior: smooth;
      background-color: var(--nyc-dark);
      color: var(--nyc-light);
      font-family: 'Montserrat', sans-serif;
    }

    /* GLASS CARDS */
    .glass {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(15px);
      -webkit-backdrop-filter: blur(15px);
      border: 1px solid rgba(255, 255, 255, 0.1);
      transition: all 0.4s ease;
      cursor: pointer;
    }

    .glass:hover {
      transform: translateY(-4px) scale(1.02);
      background: rgba(255, 255, 255, 0.1);
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.4);
    }

    /* NAVBAR */
    .nav-link {
      cursor: pointer;
      position: relative;
      transition: color 0.3s ease;
      font-weight: 500;
    }

    .nav-link::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -3px;
      width: 0;
      height: 2px;
      background: var(--nyc-blue);
      transition: width 0.3s ease;
    }

    .nav-link:hover {
      color: var(--nyc-blue);
    }

    .nav-link:hover::after {
      width: 100%;
    }

    /* BUTTONS */
    .btn-primary {
      background: var(--nyc-blue);
      color: var(--nyc-light);
      font-weight: 700;
      transition: all 0.3s ease;
    }

    .btn-primary:hover {
      background: var(--nyc-blue-dark);
      transform: scale(1.06);
      box-shadow: 0 0 20px rgba(59, 182, 255, 0.5);
    }

    /* PAGE ANIMATIONS */
    .page {
      animation: fadeSlide 0.6s ease forwards;
    }

    @keyframes fadeSlide {
      from {
        opacity: 0;
        transform: translateY(12px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* Apply subtle animation on all elements */
    .glass, h1, h2, h3, p, ul, li, .btn-primary {
      transition: transform 0.35s ease, opacity 0.35s ease;
    }

    h1, h2, h3 {
      color: var(--nyc-light);
    }

    /* Logo styling */
    .logo-img {
      height: 50px;
      width: auto;
    }
  </style>
</head>
<body>

<!-- NAVBAR -->
<nav class="glass mx-4 mt-4 rounded-2xl p-4 flex items-center justify-between">
  <div class="flex items-center gap-4">
    <img src="https://i.imgur.com/p591Cmz.png" alt="NYC Roleplay Logo" class="logo-img">
    <h1 class="font-bold text-xl">New York City Roleplay</h1>
  </div>

  <div class="flex items-center gap-6 text-sm">
    <span class="nav-link" onclick="showPage('home')">Home</span>
    <span class="nav-link" onclick="showPage('about')">About</span>
    <span class="nav-link" onclick="showPage('media')">Media</span>
    <span class="nav-link" onclick="showPage('shop')">Shop</span>
    <span class="nav-link" onclick="showPage('game')">Game</span>
    <span class="nav-link" onclick="showPage('rules')">Rules</span>

    <a href="https://discord.gg/nycrole" target="_blank"
       class="ml-4 px-6 py-2 rounded-xl btn-primary transition">
      Join Discord
    </a>
  </div>
</nav>

<!-- PAGES -->
<main class="p-8 max-w-7xl mx-auto">

  <!-- HOME -->
  <section id="home" class="page">
    <h2 class="text-4xl font-bold mb-4">Welcome to New York City Roleplay</h2>
    <p class="text-zinc-400 max-w-2xl">A professional ER:LC roleplay community focused on realism, structure, and immersive gameplay.</p>

    <div class="grid md:grid-cols-3 gap-6 mt-10">
      <div class="glass rounded-2xl p-6">Active Staff Team</div>
      <div class="glass rounded-2xl p-6">Daily Roleplays</div>
      <div class="glass rounded-2xl p-6">Custom Systems</div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about" class="page hidden">
    <h2 class="text-3xl font-bold mb-4">About Us</h2>
    <p class="text-zinc-400 max-w-3xl">New York City Roleplay (NYCRP) is an ER:LC-based roleplay server offering structured sessions, trained staff, and a welcoming community.</p>
  </section>

  <!-- MEDIA -->
  <section id="media" class="page hidden">
    <h2 class="text-3xl font-bold mb-4">Media</h2>
    <div class="grid md:grid-cols-3 gap-6">
      <div class="glass rounded-2xl p-6">Image / Video</div>
      <div class="glass rounded-2xl p-6">Image / Video</div>
      <div class="glass rounded-2xl p-6">Image / Video</div>
    </div>
  </section>

  <!-- SHOP -->
  <section id="shop" class="page hidden">
    <h2 class="text-3xl font-bold mb-4">Shop</h2>
    <p class="text-zinc-400">Coming soon: game passes, perks, and donations.</p>
  </section>

  <!-- GAME -->
  <section id="game" class="page hidden">
    <h2 class="text-3xl font-bold mb-6">Game Status</h2>

    <div class="grid md:grid-cols-3 gap-6">
      <div class="glass rounded-2xl p-6">
        <h3 class="font-semibold">ER:LC Server</h3>
        <p class="text-sm text-zinc-400">Live server data</p>
        <p class="mt-3">Status: <span class="text-green-400">Online</span></p>
        <p>Players: <span id="playerCount">24</span> / 50</p>
      </div>

      <div class="glass rounded-2xl p-6">
        <h3 class="font-semibold">Discord</h3>
        <p class="text-sm text-zinc-400">Community size</p>
        <p class="mt-3">Members: <span id="discordCount">312</span></p>
      </div>

      <div class="glass rounded-2xl p-6">
        <h3 class="font-semibold">Session Info</h3>
        <p class="text-sm text-zinc-400">Live roleplay status</p>
        <p class="mt-3">Session: Active</p>
      </div>
    </div>
  </section>

  <!-- RULES -->
  <section id="rules" class="page hidden">
    <h2 class="text-3xl font-bold mb-4">Rules</h2>

    <!-- In-Game Rules Dropdown -->
    <div class="glass rounded-2xl p-4 mb-4 cursor-pointer" onclick="toggleDropdown('inGameRules')">
      <h3 class="text-xl font-semibold flex justify-between items-center">
        In-Game Rules
        <span id="inGameRulesIcon">▼</span>
      </h3>
    </div>
    <div id="inGameRules" class="glass rounded-2xl p-4 mb-6 hidden max-h-96 overflow-y-auto">
      <ul class="list-disc ml-6 space-y-3">
        <li><strong>Random Deathmatch:</strong> Full kills are not allowed unless properly justified. Excessive or mass killings are prohibited, and harming any member of the Fire Department is strictly forbidden.</li>
        <li><strong>Vehicle Deathmatch:</strong> Random vehicle collisions and unrealistic driving are not allowed. Shooting at other vehicles without a valid roleplay reason is strictly prohibited.</li>
        <li><strong>Cuff Rushing:</strong> Do not randomly arrest or cuff other players. Handcuffs must only be used with proper roleplay justification.</li>
        <li><strong>Interfering with Scenes:</strong> Do not interfere with active roleplay scenes unless you are directly involved. Avoid disrupting or altering ongoing scenarios.</li>
        <li><strong>Uniforms & Liveries:</strong> You must wear the correct uniform and vehicle livery for your department or rank. Failure to follow this rule may result in punishment.</li>
        <li><strong>Terms of Service:</strong> All players are required to follow Roblox’s Terms of Service at all times.</li>
        <li><strong>Unrealistic Avatars:</strong> Avoid using avatars that block vision, provide invisibility, or exploit glitches. Additional details can be found in the related announcement.</li>
        <li><strong>New Life Rule:</strong> You may not remember events from a previous life or return to past scenes after respawning.</li>
        <li><strong>Fail Roleplay:</strong> Unrealistic, disruptive, or inaccurate roleplay behavior is not allowed.</li>
        <li><strong>Safe Zones:</strong> Crimes are not permitted in designated safe zones. These areas must remain roleplay-safe at all times.</li>
        <li><strong>Booster Perks:</strong> Do not use booster perks unless you are an active server booster.</li>
        <li><strong>Grapplers:</strong> Grapplers may only be used if you are certified within your whitelisted department.</li>
        <li><strong>No Intention to Roleplay:</strong> Avoid actions such as standing on moving vehicles, shooting while driving, or ignoring active roleplay scenarios.</li>
        <li><strong>VC Only:</strong> This server is voice-chat only, meaning you must be connected to voice chat during roleplay. You are not required to speak.</li>
      </ul>
    </div>

    <!-- Discord Rules Dropdown -->
    <div class="glass rounded-2xl p-4 mb-4 cursor-pointer" onclick="toggleDropdown('discordRules')">
      <h3 class="text-xl font-semibold flex justify-between items-center">
        Discord Rules
        <span id="discordRulesIcon">▼</span>
      </h3>
    </div>
    <div id="discordRules" class="glass rounded-2xl p-4 hidden max-h-96 overflow-y-auto">
      <ul class="list-disc ml-6 space-y-3">
        <li><strong>Respect:</strong> Treat everyone with kindness and respect. Harassment, hate speech, or personal attacks of any kind are strictly prohibited.</li>
        <li><strong>Pinging:</strong> Do not ping members unnecessarily. Pinging High Rank+ staff without permission is not allowed.</li>
        <li><strong>Language:</strong> Keep language appropriate at all times. Profanity and harmful or offensive content are not permitted.</li>
        <li><strong>Common Sense:</strong> Use good judgment and contribute positively. Keep posts relevant, respectful, and beneficial to the community.</li>
        <li><strong>Channel Usage:</strong> Use channels only for their intended purpose and keep discussions on-topic.</li>
        <li><strong>Advertising:</strong> Approval is required before promoting servers, products, or services. All advertisements must be brief and relevant.</li>
        <li><strong>Terms of Service:</strong> All members must follow Discord’s Terms of Service at all times.</li>
        <li><strong>Bot Usage:</strong> Bots should only be used for their intended functions and in an appropriate manner.</li>
        <li><strong>Feedback:</strong> Provide constructive and respectful suggestions. Troll or disruptive feedback may result in punishment. Honest feedback about staff is encouraged.</li>
        <li><strong>Alt Accounts:</strong> The use of alternate accounts is strictly prohibited.</li>
      </ul>
    </div>
  </section>

</main>

<script>
  lucide.createIcons();

  function showPage(id) {
    document.querySelectorAll('.page').forEach(p => p.classList.add('hidden'));
    document.getElementById(id).classList.remove('hidden');
  }

  function toggleDropdown(id) {
    const el = document.getElementById(id);
    const icon = document.getElementById(id + 'Icon');
    if (el.classList.contains('hidden')) {
      el.classList.remove('hidden');
      icon.textContent = '▲';
    } else {
      el.classList.add('hidden');
      icon.textContent = '▼';
    }
  }
</script>

</body>
<div class="glass rounded-2xl p-6">
  <h3 class="font-semibold">Discord Members</h3>
  <p class="text-sm text-zinc-400">Total people in server</p>
  <p id="discordCount" class="mt-2">Loading...</p>
</div>

<script>
async function updateDiscordCount() {
  try {
    const response = await fetch('https://your-bot-server.com/membercount');
    const data = await response.json();
    document.getElementById('discordCount').textContent = data.count;
  } catch(err) {
    document.getElementById('discordCount').textContent = 'Error';
  }
}

// Update immediately and optionally every 60 seconds
updateDiscordCount();
setInterval(updateDiscordCount, 60000);
</script>
<iframe src="https://discord.com/widget?id=1404148304333246599&theme=dark" width="350" height="500" allowtransparency="true" frameborder="0"></iframe>
