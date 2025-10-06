<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>NYCRP Staff Hub — Custom (Tabs)</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
      :root{--bg:#f7f8fb;--card:#ffffff;--accent:#1a73e8;--muted:#6b7280}
      *{box-sizing:border-box}
      body{margin:0;font-family:Inter,system-ui,-apple-system,'Segoe UI',Roboto,Arial;background:var(--bg);color:#0f172a}
      header{display:flex;align-items:center;justify-content:space-between;padding:14px 20px;background:var(--card);border-bottom:1px solid #e6eefc;position:sticky;top:0;z-index:60}
      .brand{display:flex;align-items:center;gap:12px}
      .logo{width:44px;height:44px;border-radius:8px;background:linear-gradient(45deg,var(--accent),#6ea8ff);display:flex;align-items:center;justify-content:center;color:white;font-weight:800}
      nav{display:flex;gap:8px}
      nav button{background:transparent;border:0;padding:8px 12px;border-radius:8px;font-weight:700;cursor:pointer;color:var(--muted)}
      nav button.active{background:#eaf2ff;color:var(--accent)}
      main{max-width:1100px;margin:28px auto;padding:0 18px}
      .card{background:var(--card);padding:26px;border-radius:12px;box-shadow:0 8px 30px rgba(16,24,40,0.04)}
      h1{margin:0 0 8px 0;font-size:22px}
      h2{margin-top:20px}
      section{display:none}
      section.active{display:block}
      pre{white-space:pre-wrap;font-family:inherit}
      footer{max-width:1100px;margin:18px auto;padding:12px 18px;color:var(--muted);font-size:13px}
      @media (max-width:800px){nav{overflow:auto}}
    </style>
  </head>
  <body>
    <header>
      <div class="brand">
        <div class="logo">NY</div>
        <div>
          <div style="font-weight:800">NYCRP Staff Hub</div>
          <div style="font-size:12px;color:var(--muted)">Staff Training and Docs</div>
        </div>
      </div>
      <nav aria-label="Main Navigation">
        <button data-tab="home" class="active">Home</button>
        <button data-tab="chain">Chain of Command</button>
        <button data-tab="regs">Regulations/Conduct</button>
        <button data-tab="resources">Resources</button>
      </nav>
    </header>

    <main>
      <div class="card">
        <section id="home" class="active">
          <h1>Staff Training and Education</h1>
          <h2>Welcome!</h2>
          <p>Welcome to the New York City Roleplay Staff Hub! Listed above you can find information ranging from the Chain of Command to guides you should follow to be the perfect moderator.</p>
        </section>

        <section id="chain">
          <h1>Chain of Command</h1>
          <p><strong>Director Team -</strong> Directors oversee the entire server and make voted decisions. Do not DM or ping them; use tickets or staff chat.</p>
          <p><strong>Management Team -</strong> Handle large reports, monitor performance, and oversee IA and lower staff.</p>
          <p><strong>Internal Affairs Team -</strong> Handle tickets, strikes, amd staff infractions. Go to them before upper management.</p>
          <p><strong>Administrative Team -</strong> Oversee moderators, manage bans, and resolve serious in-game issues.</p>
          <p><strong>Moderation Team -</strong> Issue warnings and kicks, and ensure fair rule enforcement in-game.</p>
        </section>

        <section id="regs">
          <h1>Staff Regulations and Conduct</h1>
          <p>Staff are not permitted to perform law enforcement duties while on duty. This includes speeding, running red lights, and running stop signs.</p>
          <p>Roleplaying of any sort while on duty is prohibited and will result in punishment.</p>
          <p>If a player asks to heal, always check for roleplay context first, to avoid ruining roleplays.</p>
          <p><strong>Rank Uniforms:</strong> Staff members must wear their designated rank uniforms while on duty to ensure they are easily identifiable. (Currently Unavaliable)</p>
          <p>If you are wearing the staff uniform, nothing should be covering it, so that the community members can identify your rank.</p>
          <p><strong>Staff Cars Only:</strong> Use only designated staff cars while on duty. Personal or roleplay vehicles are not allowed for staff use during shifts.</p>
          <p><strong>Professionalism:</strong> Maintain a professional and respectful demeanor with players and fellow staff members at all times.</p>
          <p><strong>Impartiality:</strong> Enforce rules fairly and without bias. Treat all players equally, regardless of their rank or status on the server.</p>
          <p>You must use 4+ letters at all times for all commands.</p>
          <p><strong>Chain of Command:</strong> Follow the chain of command by pinging the lowest rank online that can assist you. (Mod → Admin → IA → Mgmt → BoD)</p>
          <p><strong>Communication:</strong> Keep open lines of communication with other staff members. Report any serious issues or incidents promptly.</p>
          <p>In any mod and all mod calls, the user MUST have video evidence. We do NOT take witnesses or logs as proof.</p>
          <p>Avoid arguing with members; you have the final say, and incidents can be reported through a ticket.</p>
          <p>If a user asks for a supervisor, finish the scene and guide them to open a ticket in our communication server.</p>
          <p>You may NOT ping or TP to HRs without permission. PM them instead.</p>
          <p>If you’re unresponsive for 5+ minutes in-game, it will be considered shift grinding.</p>
          <p>GTA driving includes recklessly driving in opposite lanes, crashing into poles, or driving medians.</p>
          <p>Do not park at medians or islands. Continuous patrolling ensures good RP.</p>
        </section>

        <section id="resources">
          <h1>Resources</h1>
          <h2>Guides</h2>
          <h3>Discord Checks Guide</h3>
          <p>Always do a voice channel check with all players and a text channel check.</p>
          <ul>
            <li>Make sure all members have their account linked and verified.</li>
            <li>Check if the user has read and accepted all server rules.</li>
            <li>Ensure no inappropriate content in usernames or profiles.</li>
            <li>Respond politely and professionally to questions or issues.</li>
          </ul>
          <p><strong>Are They in the Discord Server & VC?</strong></p>
          <p>Use the command <code>/erlc membercheck</code>. This will pull up all players in-game and show their Discord status.</p>
          <ul>
            <li>If they are in the Discord</li>
            <li>If they are in a Voice Channel (VC)</li>
          </ul>
          <p>This works through Central or Melonly.</p>
          <ul>
            <li>Use Melonly as the main tool.</li>
            <li>If Melonly is down, switch to Central to complete the check.</li>
          </ul>
          <p><strong>If Melonly or Central Are Down Completely:</strong></p>
          <ul>
            <li>You may teleport to the player ONLY to bring them to the Staff Base.</li>
            <li>Ask them if they are in the Discord and in a VC (if required by rules).</li>
            <li>If they aren’t, or they lie/refuse to answer, you may jail them if under 39/40. If it’s 39/40, you may kick them.</li>
          </ul>
          <p>Stay professional and consistent.These checks are for staff use only; no abuse will be tolerated.</p>

          <h3>H/M Guide</h3>
          <p>All :h's listed below can be used freely by staff with the Moderator rank or higher.</p>
          <ul>
            <li>:h Family Jewls is now open! Come get something for yourself or a friend!</li>
            <li>:h HRP is now open! Come see the views or get a cabin!</li>
            <li>:h Three Guys: :h Three guys is now open! Come get a quick bite!</li>
            <li>:h La Mesa: :h La mesa is now open! See you there!</li>
          </ul>

          <h2>Requirements and Policies</h2>
          <p><strong>Minimum Hours:</strong> You are expected to complete 4 hours every week on shift with Melonly. You have a week to complete this quota.</p>
          <p><strong>Leave of Absence:</strong> If you cannot complete this, we have a system called Leave of Absence (LOA). This is the system we use if you are not able to go on duty. Reasons you can take LOA include mental/health issues, school exams, holidays, and many other reasons.</p>
          <p><strong>Promotions:</strong> A single promotion lasts 6 hours and requires 2 logs per hour. A double promotion lasts 14 hours and requires 2 logs per hour. A triple promotion lasts 30 hours and requires 2 logs per hour.</p>
          <p><strong>Strike Policy:</strong> If you receive 2 or more strikes within a promotion work, you will not be eligible for a promotion for that week.</p>
          <p><strong>Infraction Policy:</strong> All infractions cannot be appealed until after the expiry timer is up.</p>
          <p><strong>Staff of the Week:</strong> To be named staff of the week, you must have the most hours out of the whole staff team.</p>
          <p><strong>Retiring Policy:</strong> Users below the rank of JA will not receive "Retired Staff". All users above the rank of TIA are eligible for the "Retired High Rank" role.</p>
          <p><strong>Reinstatement Policy:</strong> Prior TIA+ members can return as "Junior Mod Rank" max. "Retired Staff" role members (JA+) can return as "Trial Staff".</p>

          <h2>Staff Outposts</h2>
          <p>Outposts are numbered in order from most to least important; go to the most important ones. The staff outposts are numbered from most important (1) to least important (4) on the image below.</p>
          <p>You must be doing discord checks or mod calls while your car is at an outpost.</p>
          <p>There will be a maximum of 2 on duty staff members per outpost.</p>
          <p>Don’t make it obvious that it is a staff base, all you should have with you is your car. People may come up to you, but you are permitted to load them if they harass or interfere with you.</p>
          <p>Make sure you are surveilling the post and the areas nearby in order to maintain smooth roleplay and order around the server. You must also conduct discord & voice chat checks at these staff outposts.</p>
          <ol>
            <li>Supervise River City Civilian Spawn, and surrounding areas.</li>
            <li>Supervise Gun Store, Fire Department, and surrounding areas.</li>
            <li>Supervise Mod Shop, the intersections nearby, the Bank, the Fire department, and surrounding areas.</li>
            <li>Supervise the City Center, the City itself, the Shopping Plaza, and Three Guys.</li>
          </ol>
          <ol>
            <li>You should NEVER just be standing still, you should either be conducting discord checks or handling rule-breaking near your outpost.</li>
            <li>You should NEVER interfere with roleplay. You should remain at your outpost unless you witness any rule-breaking near your outpost.</li>
            <li>You should NEVER help with police chases. In a police chase, there really aren't any instances of GTA-Driving, so lay low on that unless there is any rule-breaking involved.</li>
          </ol>
          <p><strong>Staff Outposts Images and Locations:</strong></p>
          <p>Outpost 1: Spawn — The most crime-filled area and should be closely supervised, this is our main priority for moderation as it is where most trolling and other rule-breaking happens. (expect to get VDMed)</p>
          <p>Outpost 2: Gun Store — Typically where the most RDM happens because of the quick access to guns and people to fight, expect a lot of RDM logs.</p>
          <p>Outpost 3: Mod Shop — Supervises the intersection, FD station, and bank to ensure RDM and other fail roleplay is not happening. Always on alert for gunshots to investigate.</p>
          <p>Outpost 4: Three Guys — The least active of the 4, supervise the city center, jewelry, and nearby city area. Prioritize discord checks and VC checks.</p>
          <p>Please remember for all of these locations that your priorities should be supervising and doing discord/VC checks. Always make sure you are doing mod calls when they appear and to come back when finished.</p>
        </section>
      </div>
    </main>

    <footer>
      <div style="max-width:1100px;margin:8px auto;padding:0 18px;color:var(--muted)">© 2025 New York City Roleplay — Staff Hub</div>
    </footer>

    <script>
      const tabs = document.querySelectorAll('nav button');
      const sections = document.querySelectorAll('main section');
      tabs.forEach(t => t.addEventListener('click', () => {
        tabs.forEach(b=>b.classList.remove('active'));
        t.classList.add('active');
        const id = t.getAttribute('data-tab');
        sections.forEach(s=>{
          if(s.id===id) s.classList.add('active'); else s.classList.remove('active');
        });
        window.location.hash = id;
      }));
      const hash = window.location.hash.replace('#','');
      if(hash){
        const target = document.querySelector('nav button[data-tab="'+hash+'"]');
        if(target) target.click();
      }
    </script>
  </body>
</html>
