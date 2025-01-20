---
layout: page
title: "Calendar"
permalink: /calendar/
---

<div id="upcoming"></div>

<html lang='en'>
  <head>
    <meta charset='utf-8' />
    <script src='/assets/fullcalendar-6.1.15/dist/index.global.js'></script>
    <script src='/assets/fullcalendar-6.1.15/packages/google-calendar/index.global.js'></script>
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
          height: "auto",
          googleCalendarApiKey: "{{ site.google.calendar.api_key }}",
          events: {
            googleCalendarId: '23a7d9803d27c7e98215e420fd4f8e5e62f4a017673c1a3d3b940801b0c27ec7@group.calendar.google.com'
          },
          eventColor: '#F4797E',
        });

        calendar.render();
      });

    </script>

  </head>
  <body>
    <div id='calendar'></div>
  </body>
</html>
