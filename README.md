
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Proposal</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
  }
  .proposal {
    margin-top: 100px;
  }
  button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    border: none;
    border-radius: 5px;
    margin-top: 20px;
  }
  #yesBtn {
    background-color: #4CAF50;
    color: white;
    margin-right: 20px;
  }
  #noBtn {
    background-color: #f44336;
    color: white;
  }
  
  /* Modal styles */
  .modal {
    display: none;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.5);
  }
  .modal-content {
    background-color: #fefefe;
    margin: 10% auto;
    padding: 20px;
    border: 1px solid #888;
    width: 80%;
    max-width: 600px;
    border-radius: 5px;
  }
  .close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
  }
</style>
</head>
<body>
<div class="proposal">
  <h2>Will you be my queen?</h2>
  <button id="yesBtn" onclick="handleResponse(true)">Yes</button>
  <button id="noBtn" onclick="handleResponse(false)">No</button>
</div>

<!-- Modal HTML -->
<div id="gifModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal()">&times;</span>
    <img src="https://media.tenor.com/images/3e1ff44c90e52ff1defe6b5dbaf225ca/tenor.gif%22%20alt=%22HABIBTI%22%20id=%22my-gif" alt="Proposal GIF" style="max-width: 100%;">
  </div>
</div>

<script>
  function handleResponse(response) {
    if (response) {
      // Display modal with GIF
      document.getElementById('gifModal').style.display = "block";
    } else {
      alert("I will wait for your decision.");
      while (true) {
        var newResponse = confirm("Have you changed your mind? Will you be my queen?");
        if (newResponse) {
          alert("Congratulations! You said yes! You are now my queen!");
          break;
        }
      }
    }
  }

  function closeModal() {
    document.getElementById('gifModal').style.display = "none";
  }
</script>
</body>
</html>
