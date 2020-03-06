---
layout: page
title: Submit
---

<div align="center">
<h1>Please complete the form below</h1>
</div>

<div style="--aspect-ratio: 16/9;">
  <iframe
    id="tripetto"
    width="720"
    height="720"
    frameborder="0"
    marginheight="0"
    marginwidth="0"
  >
  </iframe>
</div>

<script>
var tripettoElement = document.getElementById("tripetto");
var tripettoDoc = tripettoElement.contentWindow || tripettoElement.contentDocument.document || tripettoElement.contentDocument;
tripettoDoc.document.open();
tripettoDoc.document.write(decodeURI("%3Cbody%3E%3Cscript%20src=%22https://unpkg.com/tripetto-collector%22%3E%3C/script%3E%0A%3Cscript%20src=%22https://unpkg.com/tripetto-collector-rolling%22%3E%3C/script%3E%0A%3Cscript%20src=%22https://unpkg.com/tripetto-services%22%3E%3C/script%3E%0A%3Cscript%3E%0ATripettoServices.init(%7B%20token:%20%22eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjoiMVhoNkFIMmVBU2JuV2JqeGE5dk1pT04yMnpxYnE3cjh3TnhuNlZlb01aVT0iLCJkZWZpbml0aW9uIjoiZ283UCtaaVc1QVVKWE8zRDNuRjlpbEg0RlNaZFhmK3IyMzRTM3JRUTZuUT0iLCJ0eXBlIjoiY29sbGVjdCJ9.UN6b6JZc4-W80oznWvYijXwm9HPMGhd2NSY8xVqYhVo%22%20%7D);%0A%0ATripettoCollectorRolling.run(%7B%0A%20%20%20%20element:%20document.body,%0A%20%20%20%20definition:%20TripettoServices.definition,%0A%20%20%20%20style:%20TripettoServices.style,%0A%20%20%20%20onFinish:%20TripettoServices.onFinish,%0A%20%20%20%20onAttachment:%20TripettoServices.onAttachment%0A%7D);%0A%3C/script%3E%3C/body%3E"));
tripettoDoc.document.close();
</script>
