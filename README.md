# Weather Event Planner

Pulls a live weather forecast for any city and flags which days are good for
an outdoor event.

## What it does
Type in any city, and it pulls a 7-day forecast from a free public API, then
flags each day as "Good to go," "Too hot," "Rain risk," or "Too windy" based
on the temperature, chance of rain, and wind speed. Instead of just showing
raw weather numbers, it turns them into a straight answer: is this a good day
to be outside or not.

## How I built it
- Google Colab (Python in the browser, nothing to install)
- Python with the requests library to call two Open-Meteo APIs — one turns a
  typed city name into coordinates, the other returns the actual forecast
- pandas to build the results into a clean table
- I used Claude to help write the code, but made the judgment calls myself —
  like what counts as "too hot," "too windy," or too much rain risk for an
  outdoor event.

## Who it helps
Anyone deciding whether a day is good for something outdoors — for example, a
volunteer coordinator picking a date for an outdoor event, so they're not
guessing or checking the weather app day by day.

## What I'd add next
Right now it only looks at the next 7 days. I'd add the ability to pick a
specific date range or a full month ahead, so someone planning further out
could see more options instead of just this week.

## Files
- `weather_event_planner.ipynb` — the notebook
- `[city]_event_forecast.csv` — a sample saved forecast
