---
layout: page
---

Welcome to Break Into Data  


<div class="text-align: center">
    <iframe src="https://breakintodata.substack.com/embed" height="320" style="width: 400px; max-width: calc(100vw - 20px); margin: auto; display: block;" frameborder="0" scrolling="no"></iframe>
    <h2>Join Our Discord Server</h2>
    <div id="total-members">Total Members</div>
    <div id="online-members">Online Members</div>
    <a href="#" id="join-button">Join Server</a>
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