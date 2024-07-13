---
layout: page
---

Welcome to Break Into Data  


<div class="text-align: center">
    <iframe src="https://breakintodata.substack.com/embed" height="320" style="width: 400px; max-width: calc(100vw - 20px); margin: auto; display: block;" frameborder="0" scrolling="no"></iframe>
</div>

<div class="discord-widget container">
    <h1>Join Our Discord Server</h1>
    <div class="server-stats">
        <div class="stat-box">
            <span id="total-members">0</span>
            <span class="stat-label">Total Members</span>
        </div>
        <div class="stat-box">
            <span id="online-members">0</span>
            <span class="stat-label">Online Now</span>
        </div>
    </div>
    <a href="#" id="join-button" class="join-button btn-subscribe">Join Server</a>
</div>


<script>
    const apiUrl = `https://discord.com/api/guilds/1168693434572345346/widget.json`; 
    
    fetch(apiUrl)
      .then(response => response.json())
      .then(data => {
        document.getElementById('total-members').textContent = data.members.length;
        document.getElementById('online-members').textContent = data.presence_count;
        
        document.getElementById('join-button').href = data.instant_invite;
      });
</script>