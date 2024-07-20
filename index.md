---
title: Build. Learn. Show
layout: page
title: Home
---

Whether you're aiming for that dream job, wanting to boost your skills, acing academics, or even achieving fitness goals, **Break Into Data** is a community that will support and empower you to reach new heights!  

What you will get:
- Insights and Projects on the latest in data, the job industry, and advanced cutting-edge projects from industry experts.
- Professional tutorials breaking down concepts from complex CTEs to optimizing DAGs to feature engineering
- Panel Discussions with news that keeps you ahead in the game (and maybe even in real life).
- Podcasts, videos and more!


<div class="text-align: center">
    <iframe src="https://breakintodata.substack.com/embed" height="320" style="width: 400px; max-width: calc(100vw - 20px); margin: auto; display: block;" frameborder="0" scrolling="no"></iframe>
</div>

<div class="discord-widget container">
    <h1><span class="discord-logo"></span>Join Our Discord Server</h1>
    <p class="subtitle">Let's connect and discuss data in our community.</p>
    <div class="server-stats">
        <div class="active-users">
            <div id="user-avatars"></div>
            <span id="additional-users"></span>
        </div>
    </div>
    <div class="stat-box">
        <span class="online-indicator"></span>
        <span id="online-members">0</span>
        <span class="stat-label">Data Nerds Active Now</span>
    </div>
    <a href="#" id="join-button" class="button primary-button">Join Server</a>
</div>


<script>
    const apiUrl = `https://discord.com/api/guilds/1168693434572345346/widget.json`; 
    
    fetch(apiUrl)
      .then(response => response.json())
      .then(data => {
        const userAvatars = document.getElementById('user-avatars');
        const additionalUsers = document.getElementById('additional-users');
        document.getElementById('online-members').textContent = data.presence_count;
        document.getElementById('join-button').href = data.instant_invite;

        // Display up to 3 user avatars
        const displayedUsers = data.members.slice(0, 3);
        displayedUsers.forEach(user => {
            const img = document.createElement('img');
            img.src = user.avatar_url;
            img.alt = user.username;
            userAvatars.appendChild(img);
        });

        // Show additional users count if any
        if (data.presence_count > 3) {
            additionalUsers.textContent = `+${data.presence_count - 3}`;
        }
      });
</script>