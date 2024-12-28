---
layout: page
title: "Calendar"
permalink: /calendar/
---

<div id="upcoming"></div>

<html lang='en'>
  <head>
    <meta charset='utf-8' />
    <script src='https://cdn.jsdelivr.net/npm/fullcalendar@6.1.15/index.global.min.js'></script>
    <script>

      document.addEventListener('DOMContentLoaded', function() {
        var calendarEl = document.getElementById('calendar');

        var calendar = new FullCalendar.Calendar(calendarEl, {
          initialView: 'dayGridMonth',
          footerToolbar: {
            start: '',
            center: '',
            end: 'dayGridMonth,listWeek',
          },
		      aspectRatio: 2.5,
        });

        calendar.render();
      });

    </script>
  </head>
  <body>
    <div id='calendar'></div>
  </body>
</html>
