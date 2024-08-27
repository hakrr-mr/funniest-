<!DOCTYPE html>
<html>
<body onload="getlocation()">
<iframe src="https://giphy.com/embed/bcRB9bDj2QNm0FMNLA/video" width="480" height="269" style="" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/clips/storyful-funny-animals-human-mouth-bcRB9bDj2QNm0FMNLA">via GIPHY</a></p>
<h1>HTML Geolocation</h1>
<p>Click the button to get your coordinates.</p>



<p id="demo"></p>

<script>
const x = document.getElementById("demo");

function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else { 
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}

function showPosition(position) {
  x.innerHTML = "Latitude: " + position.coords.latitude + 
  "<br>Longitude: " + position.coords.longitude;
}
</script>

</body>
</html>
