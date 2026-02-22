# ham_pell
자놀 보관용
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="robots" content="noindex">
<title>Character Archive</title>

<style>
body { font-family: sans-serif; }

.gallery {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

.thumbnail {
  width: 200px;
  cursor: pointer;
  transition: 0.3s;
}

.thumbnail:hover {
  transform: scale(1.05);
}

.modal {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.8);
}

.modal-box {
  background: white;
  width: 80%;
  max-width: 600px;
  margin: 5% auto;
  padding: 20px;
  text-align: center;
  border-radius: 10px;
}

.modal-box img {
  max-width: 100%;
}

.close {
  position: absolute;
  right: 30px;
  top: 20px;
  font-size: 30px;
  color: white;
  cursor: pointer;
}
</style>
</head>

<body>

<h1>Character Archive</h1>

<div class="gallery">
  <img src="https://cdn.discordapp.com/attachments/1445779726781124812/1445783319613538354/MD1.png?ex=699bbae4&is=699a6964&hm=7b963882f7883bdb27e579a93ec98222ab460dad2ea64f92fd0f40b1b9f33329&"
       class="thumbnail"
       onclick="openModal('https://cdn.discordapp.com/attachments/1445779726781124812/1445783319613538354/MD1.png?ex=699bbae4&is=699a6964&hm=7b963882f7883bdb27e579a93ec98222ab460dad2ea64f92fd0f40b1b9f33329&','캐릭터 설명입니다')">
</div>

<div id="myModal" class="modal">
  <span class="close" onclick="closeModal()">&times;</span>

  <div class="modal-box">
    <img id="modalImg">
    <p id="modalDesc"></p>
    <a id="downloadBtn" download>이미지 다운로드</a>
  </div>
</div>

<script>
function openModal(imgSrc, description) {
  document.getElementById("myModal").style.display = "block";
  document.getElementById("modalImg").src = imgSrc;
  document.getElementById("modalDesc").innerText = description;
  document.getElementById("downloadBtn").href = imgSrc;
}

function closeModal() {
  document.getElementById("myModal").style.display = "none";
}
</script>

</body>
</html>
