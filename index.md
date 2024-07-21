---
layout: page
title: Home
---

<div class="page-hero pt-[25vh]">
    <h1 class="page-hero-title">
        Launch Your <br><span class="rainbow-text-animated">Data Science</span> Career
    </h1>
    <p style="margin-right: 60px;">
    Break Into Data is your launchpad into the world of data science and analytics. We provide hands-on experience, expert guidance, and a supportive community to help you thrive in the data-driven job market.</p>
    <a href="/workshops" class="button primary-button workshops-enroll-button">Explore Workshops</a>
    <a href="https://discord.gg/xP6YaXjd" class="button secondary-button workshops-learnmore-button">Join Discord</a>
</div>

### 👥 Community Hub

Connect with peers, find study buddies, and access job hunting resources in our thriving Discord community. Track your progress with our AI-powered tools. Join 2000+ data enthusiasts on Discord.

<br><br>
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
<br><br>

### 🛠️ Professional Workshops

Build your portfolio with industry-relevant workshops. Immerse yourself in real-world tech environments. From computer vision to machine learning, our workshops give you the hands-on experience employers crave.

<div class="cta-buttons">
  <a href="/workshops" class="button primary-button workshops-enroll-button">Explore Workshops</a>
</div>

### 📺 Weekly Expert Sessions

Learn from industry leaders in weekly live events.Tune in to our live YouTube sessions featuring industry experts sharing insights on the latest trends in data science.

<div class="cta-buttons">
  <a href="https://www.youtube.com/@BreakIntoData" class="button primary-button workshops-enroll-button">Subscribe on YouTube</a>
</div>

<!-- ---

## What Our Members Say

> "It was a really wonderful experience. I enjoy the community because everyone is so friendly and accommodating. It was such a great experience. We participated for the first time, and it was just amazing." - Eman Nisar

> "It was a great experience to tackle a machine learning challenge from inception to solution. Every step of the way, there was a wealth of knowledge to absorb. Working alongside a great team made it even more fun."- Gnanambal Kamakshi Renganathan

--- -->

<h2 class="centered-header">Ready to Break Into Data?</h2>

Join our community and take the first step towards a rewarding career in data science! Subscribe to our newsletter for the latest workshops, job opportunities, and data science tips.

<div class="text-align: center">
    <iframe src="https://breakintodata.substack.com/embed" height="320" style="width: 400px; max-width: calc(100vw - 20px); margin: auto; display: block;" frameborder="0" scrolling="no"></iframe>
</div>
