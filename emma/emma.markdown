---
layout: page
title: For Emma
permalink: /emma/
---

## Hey there Emma.

So it's your birthday.

What the heck are you going to do?

It looks like you've got this much time left to figure that out:

<!-- Display the countdown timer in an element -->
<p id="timer" align="center"></p>

It also looks like I have this much time to finish programming this! Keep checking back for updates :)

<script>
// Set the date we're counting down to
var countDownDate = new Date("Jan 25, 2020 23:59:59").getTime();

// Update the count down every 1 second
var x = setInterval(function() {

  // Get today's date and time
  var now = new Date().getTime();

  // Find the distance between now and the count down date
  var distance = countDownDate - now;

  // Time calculations for days, hours, minutes and seconds
  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);

  // Display the result in the element with id="timer"
  document.getElementById("timer").innerHTML = days + "d " + hours + "h "
  + minutes + "m " + seconds + "s ";

  // If the count down is finished, write some text 
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("timer").innerHTML = "EXPIRED";
  }
}, 1000);
</script>

[jekyll-organization]: https://github.com/jekyll
