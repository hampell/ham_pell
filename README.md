# ham_pell
자놀 보관용
# ham_pell
자놀 보관용

<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="robots" content="noindex">
<title>Character Archive</title>

<style>
body {
  font-family: sans-serif;
}

/* 썸네일 정렬 */
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

/* 모달 */
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

/* 모달 내용 박스 */
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

  <!-- 캐릭터 1 -->
  <img src="https://cdn.discordapp.com/attachments/1445779726781124812/1445783319613538354/MD1.png?ex=699bbae4&is=699a6964&hm=7b963882f7883bdb27e579a93ec98222ab460dad2ea64f92fd0f40b1b9f33329&" 
       class="thumbnail"
       onclick="openModal('https://cdn.discordapp.com/attachments/1445779726781124812/1445783319613538354/MD1.png?ex=699bbae4&is=699a6964&hm=7b963882f7883bdb27e579a93ec98222ab460dad2ea64f92fd0f40b1b9f33329&', '캐릭터 1 설명입니다!')">

  <!-- 캐릭터 2 -->
  <img src="https://cdn.discordapp.com/attachments/1445779726781124812/1445783319613538354/MD1.png?ex=699bbae4&is=699a6964&hm=7b963882f7883bdb27e579a93ec98222ab460dad2ea64f92fd0f40b1b9f33329&" 
       class="thumbnail"
       onclick="openModal('https://cdn.discordapp.com/attachments/1445779726781124812/1445783319613538354/MD1.png?ex=699bbae4&is=699a6964&hm=7b963882f7883bdb27e579a93ec98222ab460dad2ea64f92fd0f40b1b9f33329&', '캐릭터 2 설정 설명입니다.')">

</div>


<!-- 모달 영역 -->
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
