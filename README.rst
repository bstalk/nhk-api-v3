=======
nhk-api
=======

Python client for NHK API V3.

Requirements
============

- Python 3.10

Installation
============

::

Usage
=====

::

   from datetime import date
   from nhk import ProgramGuideV3
   
   client = ProgramGuideV3(api_key='YOUR_API_KEY')
   
   # Get radio program list
   program_list = client.pg_date_radio('130', 'r3', date.today())
   
   # Get radio program list by genre
   program_list_by_genre = client.pg_genre_radio('130', 'r3', '0402', date.today())
   
   # Get radio broadcast event information
   program_info = client.broadcast_event_radio('r3-130-2026011374258')
   
   # Get information of radio program that is broadcasting now
   program_now = client.pg_now_radio('130', 'r3')
