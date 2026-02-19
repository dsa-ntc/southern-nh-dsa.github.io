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
            googleCalendarId: 'c_69d2c2e74816c2787c3848d7b1fa18a34fa6003ca7dd836ce92d8245f59e82b5@group.calendar.google.com'
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
