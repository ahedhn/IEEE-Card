<!DOCTYPE html>
<html>
<head>
  <style>
    #card_container {
      position: relative;
      display: inline-block;
    }
    #card_image {
      display: block;
      width: 100%; /* Ensure the image scales properly */
      height: auto; /* Maintain the aspect ratio */
    }
    #text_overlay {
      position: absolute;
      top: 80%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 30px;
      color: white;
      text-shadow: 2px 2px 4px #000000;
      pointer-events: none;
    }
  </style>
</head>
<body onload="load_ready()">

<div id="card_container">
  <img id="card_image" src="/mnt/data/WhatsApp Image 2024-06-15 at 7.55.35 PM.jpeg" alt="Card Image">
  <div id="text_overlay"></div>
</div>

<input type="text" id="user_name" placeholder="Enter your name" oninput="update_text()">
<button onclick="download_image()">Download Image</button>

<script>
  function load_ready() {
    // Initial load, setting the image source and preparing the canvas
    update_text();
  }

  function update_text() {
    const userName = document.getElementById('user_name').value;
    const textOverlay = document.getElementById('text_overlay');
    textOverlay.innerHTML = userName;
  }

  function download_image() {
    const cardContainer = document.getElementById('card_container');
    const cardImage = document.getElementById('card_image');
    const textOverlay = document.getElementById('text_overlay');

    const canvas = document.createElement('canvas');
    const context = canvas.getContext('2d');

    canvas.width = cardImage.width;
    canvas.height = cardImage.height;

    context.drawImage(cardImage, 0, 0);
    context.font = `${window.getComputedStyle(textOverlay).fontSize} ${window.getComputedStyle(textOverlay).fontFamily}`;
    context.fillStyle = window.getComputedStyle(textOverlay).color;
    context.textAlign = 'center';
    context.textBaseline = 'middle';
    context.fillText(textOverlay.innerHTML, canvas.width / 2, canvas.height * 0.8); // Adjusted position to 80% height

    const link = document.createElement('a');
    link.download = 'card.png';
    link.href = canvas.toDataURL();
    link.click();
  }
</script>

</body>
</html>
