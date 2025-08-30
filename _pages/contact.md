---
layout: archive
title: "Contact"
permalink: /contact/
---

### 📍 Map
<img src="/images/image3.png" alt="Map to office" style="max-width:400px; border-radius:8px; box-shadow:0 2px 8px rgba(0,0,0,0.15);">

---

### 🏢 Address
<canvas id="addressCanvas" width="450" height="40"></canvas>

---

### ☎ Office Phone
<canvas id="phoneCanvas" width="280" height="40"></canvas>

---

<script>
// 绘制地址
(function() {
  const canvas = document.getElementById('addressCanvas');
  if (canvas.getContext) {
    const ctx = canvas.getContext('2d');
    ctx.font = '16px Arial';
    ctx.fillStyle = '#000';
    ctx.fillText('Rm 312, Academic Building, HKUST(GZ), Guangzhou, China', 10, 25);
  }
})();

// 绘制电话
(function() {
  const canvas = document.getElementById('phoneCanvas');
  if (canvas.getContext) {
    const ctx = canvas.getContext('2d');
    ctx.font = '16px Arial';
    ctx.fillStyle = '#000';
    ctx.fillText('Tel: 020-88336690', 10, 25);
  }
})();
</script>
