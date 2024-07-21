---
layout: page
title: About Us
permalink: /about/
---

Break Into Data is a thriving community dedicated to empowering the next generation of data professionals. Our mission is to bridge the gap between theoretical knowledge and practical, industry-relevant skills, helping you launch and advance your career in the exciting world of data science and analytics.

## Our Offerings

### 🛠️ Professional Workshops

Our hands-on, cohort-based workshops that simulate real-world tech environments, giving you the practical experience employers are looking for. From applied computer vision to machine learning projects, our workshops are designed to build your portfolio and enhance your problem-solving skills.

<br><br>
<div class="discord-widget container">
    <h1>Check Out Our Workshops</h1>
    <p class="subtitle">Learn to build data-driven solutions with real-world tech projects.</p>
    <a href="/workshops" class="button primary-button">Enroll Now</a>
</div>
<br><br>

### 🎙️ Weekly Expert Sessions

We host regular live events featuring industry experts who share invaluable insights, career advice, and the latest trends in data science. These sessions are streamed live on YouTube and archived for on-demand viewing.

### 📚 Rich Learning Resources

Our YouTube channel is a treasure trove of tutorials covering cutting-edge topics like LangChain, Retrieval-Augmented Generation (RAG), and other essential data science tools and techniques.

### 🤝 Community

At the heart of Break Into Data is our dynamic Discord community of 2000+ data enthusiasts, professionals, and job seekers. Here, you'll find:

- 🤖 An AI-powered accountability bot to keep you on track with your goals
- 📊 Automated LeetCode tracking and leaderboards to gamify your coding practice
- 💼 Dedicated channels for job hunting, interview prep, and finding study buddies
- 🌐 A supportive network for sharing experiences and advice

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

At Break Into Data, we believe in learning by doing, growing through community, and staying at the forefront of data science innovations. Join us, and take the first step towards a rewarding career in data!

**Ready to break into data?** Explore our workshops, join our community, and subscribe to our YouTube channel to start your journey today!

<div class="cta-buttons">
  <a href="/workshops" class="cta-button">Explore Workshops</a>
  <a href="#" id="discord-link" class="cta-button">Join Our Discord</a>
  <a href="https://www.youtube.com/@BreakIntoData" class="cta-button">Subscribe on YouTube</a>
</div>
