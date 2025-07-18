<!DOCTYPE html>
<html>
<head>
  <title>Bus Seat Layout</title>
  <style>
    .seat {
      width: 40px;
      height: 40px;
      margin: 5px;
      background-color: #4CAF50;
      display: inline-block;
      text-align: center;
      line-height: 40px;
      cursor: pointer;
    }
    .booked { background-color: red; cursor: not-allowed; }
    .selected { background-color: blue; }
  </style>
</head>
<body>
  <h2>Bus Seat Layout</h2>
  <div id="seat-panel">
    <!-- 4x10 সিট -->
    <script>
      for(let i=1; i<=40; i++) {
        document.write(`<div class="seat" onclick="selectSeat(this)">${i}</div>`);
        if(i % 4 === 0) document.write("<br>");
      }
    </script>
  </div>

  <script>
    function selectSeat(el) {
      if(el.classList.contains("booked")) return;
      el.classList.toggle("selected");
    }
  </script>
</body>
</html>
