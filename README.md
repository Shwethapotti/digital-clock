<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Current Time</title>
<style>
  #time {
    font-size: 150px;
    font-family: Arial, sans-serif;
    margin-top: 50px;
    text-align: center;
  }
</style>
</head>
<body>
<h1 id="time"></h1>
<script>
  function updateTime() {
    var now = new Date();
    var hours = now.getHours();
    var minutes = now.getMinutes();
    var seconds = now.getSeconds();
    var milliseconds = now.getMilliseconds();

    // Add leading zeros if necessary
    hours = (hours < 10 ? "0" : "") + hours;
    minutes = (minutes < 10 ? "0" : "") + minutes;
    seconds = (seconds < 10 ? "0" : "") + seconds;

    // Update the time in the HTML element
    var timeElement = document.getElementById("time");
    timeElement.textContent = hours + ":" + minutes + ":" + seconds + ":" + milliseconds;

    // Update every 100 milliseconds to show milliseconds accurately
    setTimeout(updateTime, 100);
  }

  // Call the function to start updating the time
  updateTime();
</script>
</body>
</html>
