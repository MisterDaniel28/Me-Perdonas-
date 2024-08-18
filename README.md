# Me-Perdonas-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MENSAJE</title>
<style>
body {
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
font-family: Calibri, sans-serif;
}

.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 50px;
}

#buttonContainer,
#buttonContainer2 {
    width: 300px;
    height: 100px;
    position: relative;
    text-align: center;
    padding: 10px 50px;
   
    
}


#title {
font-size: 24px;
  font-weight: bold;
  margin-bottom: 10px;
}



.button {
padding: 10px 50px;
font-size: 16px;
border-radius: 5px;
cursor: pointer;
transition: font-size 0.3s ease;
}

.green {
background-color: #4CAF50;
color: white;
border: none;
}

.red {
background-color: #f44336;
color: white;
border: none;
}

.green:hover {
transform: scale(1.1);
}

.red:active {
animation: grow 1s infinite alternate;
}

@keyframes grow {
to {
font-size: 1000px;
}
}

#gif {
position: absolute;
top: -150px;
left: 50%;
transform: translateX(-50%);
z-index: -1;
width: 200px;
}
</style>
</head>
<body>
    
    <div class="container">
     
      <div id="buttonContainer2">
          
        <img id="gif" src="https://elvatoquecodea.com/mensajestiktok/ositotierno.gif" alt="Corazón latiendo">
        <br>
        <br>
        <div id="title">¿Me perdonas?</div> 
        <div id="textoDiferente"></div>
        <br>
    </div>
    
    
    <div id="buttonContainer">
        <button id="yesButton" class="button green" style="margin-bottom: 10px;">Si</button>
        
       
        <button id="noButton" class="button red">No</button>
        <br>
        <br>
        <div id="title2">Atte: Tu Novio "Daniel"</div>
         <br>
        <br>
         <br>
        
    </div>
       
  </div>



<script>
document.getElementById("yesButton").addEventListener("click", function() {
showAlertWithGif();
hideButtons();
});

document.getElementById("noButton").addEventListener("click", function() {
    var currentSize = parseInt(window.getComputedStyle(document.getElementById("yesButton")).fontSize);
    var newSize = currentSize + 30;
    if (newSize <= 1000) {
        document.getElementById("yesButton").style.fontSize = newSize + "px";
        var messages = ["¿Estás segura?", "Estas completamente segura?..", "Le daré like a tus videos", "Por favor?", "Me encantas", "Andale perdoname", "Deja de darle click ahí", "Te mandaré un león", "Ya perdoname!!", "Te compraré pollito", "Tu mandas bb", "Deja de dar click ahí", "Sere mas obediente :(","Ya perdoname", "Estaré siempre para ti", "Me perdonaste?", "Por Favor :(", "Ya me perdonaste?"];
        var index = parseInt(document.getElementById("noButton").getAttribute("data-index")) || 0;
        if (index < messages.length) {
            document.getElementById("textoDiferente").innerText = messages[index];
            document.getElementById("noButton").setAttribute("data-index", index + 1);
        } else {
            document.getElementById("textoDiferente").innerText = "Porfis";
        }
    }
});

function showAlertWithGif(){
   var gifUrl1 = "https://elvatoquecodea.com/mensajestiktok/muchoscorazones.gif";
    var gifUrl2 = "https://elvatoquecodea.com/mensajestiktok/vidaamor.gif";

    var img1 = document.createElement("img");
  img1.src = gifUrl1;
  img1.style.width = "200px";
  img1.style.height = "200px";
  img1.style.position = "fixed";
  img1.style.top = "30%";
  img1.style.left = "50%";
  img1.style.transform = "translate(-50%,-50%)";
  img1.style.zIndex = "9999";
  img1.style.borderRadius = "0";
  img1.style.boxShadow = "0 0 20px rgba(0, 0, 0, 0.3)";
  document.body.appendChild(img1);
    
    var title = document.createElement("div");
  title.textContent = "Gracias mi reina";
  title.style.position = "fixed";
  title.style.top = "51%";
  title.style.left = "50%";
  title.style.transform = "translate(-50%, -50%)";
  title.style.zIndex = "9999";
  title.style.fontSize = "24px";
  title.style.fontFamily = "Calibri, sans-serif";
  title.style.fontWeight = "bold";
  document.body.appendChild(title);

  var img2 = document.createElement("img");
  img2.src = gifUrl2;
  img2.style.width = "200px";
  img2.style.height = "200px";
  img2.style.position = "fixed";
  img2.style.top = "72%";
  img2.style.left = "50%";
  img2.style.transform = "translate(-50%, -50%)";
  img2.style.zIndex = "9999";
  img2.style.borderRadius = "0";
  img2.style.boxShadow = "0 0 20px rgba(0, 0, 0, 0.3)";
  document.body.appendChild(img2);

  setTimeout(function() {
    document.body.removeChild(img1);
    document.body.removeChild(title);
    document.body.removeChild(img2);
    alert("Te amo bebe");
  }, 3000);
}

function hideButtons() {
  document.getElementById("buttonContainer2").style.display = "none";
  document.getElementById("buttonContainer").style.display = "none";
  
}

</script>

</body>
</html>
